# ACL

správa práv je realizovaná pomocou `acl` príkazov.

Všetky príkazy opísané na tejto strane sú postkytné `base.acl` modulom.

## Ako to funguje

Všetky príkazy majú predvolený `ACLevel`, ktorého hodnota môže byť: `BOT_OWNER`, `GUILD_OWNER`, `MOD`, `SUBMOD`, `MEMBER` alebo `EVERYONE`.
Táto hodnota určuje, či používateľ môže používať konkrétny príkaz alebo nie.
`BOT_OWNER` môže vždy zavolať akýkoľvek príkaz.

## Nastavenie priradenia rolí

Ktorejkoľvek roli na tvojom serveri môže byť priradená ACLevel hodnota.
`BOT_OWNER` a `GUILD_OWNER` sú priradené automaticky majiteľom a nemôžu byť pridelené nikomu inému.

Predpokladajme, že máš na serveri dve role (**Administrator**, **Helper**), môžeš ich priradiť botovým dvom ACLevelom

```
!acl mapping add Administrator MOD
!acl mapping add Helper SUBMOD
```

Týmto im budú altomaticky pridelené práva na používanie privilegovaných príkazov.

## Altering the defaults

To display all commands with their ACLevels, run

```
!acl default audit
# You can use filters to limit the list
!acl default audit acl
```

This will list all the commands the bot knows.

Use the `default` subcommand if you want to increase or decrease command's required ACLevel.
For example, to ensure only MODs can run the `ping` command, run

```
!acl default add <command> <level>
# for example:
!acl default add ping MOD
```

Please note that in order to run some subcommand successfully, whole path has to be allowed:

```
!acl default add "acl" MEMBER
!acl default add "acl default" MEMBER
!acl default add "acl default list" MEMBER
```

Each command may have more specific overwrite, specified by role, channel or user. That can be done by `acl overwrite` commands.

## Recommended server setup

1. Perform `acl default audit` to see all the defaults.
2. Use `acl default add` command to alter ACLevels of commands you would like to be different.
3. Map roles to ACLevels with `acl mapping add` command.
4. Add user, role and channel overwrites with `acl overwrite` commands: both positive (*allow this*) and negative (*deny this*) are supported.

## Command overview

Main characteristics have been outlined above.

Use `!help <command>` to see more details or ask through GitHub issues -- either on
[docs](https://github.com/pumpkin-py/docs/issues) or
[bot](https://github.com/pumpkin-py/pumpkin-py/issues) repository page.
