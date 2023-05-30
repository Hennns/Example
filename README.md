# Example

This example works in ansible-lint 6.14.4

This example does not work in ansible-lint 6.15 and later


# To reproduce:

cd code/production/

/code/production # ansible-lint -v



Output on 6.15.0:

    /code/code/production # ansible-lint -vvv
    DEBUG    Logging initialized to level 10
    INFO     Identified /code/code as project root due config file /code/code/.config/ansible-lint.yml.
    DEBUG    Options: Namespace(cache_dir='/root/.cache/ansible-compat/5694d0', colored=True, configured=True, cwd=PosixPath('/code/code/production'), display_relative_path=True, exclude_paths=['.cache', '.git', '.hg', '.svn', '.tox'], format=None, lintables=[], list_rules=False, list_tags=False, write_list=[], parseable=False, quiet=False, rulesdirs=['/app/lib/python3.11/site-packages/ansiblelint/rules'], skip_list=[], tags=[], verbosity=3, warn_list=['experimental', 'jinja'], kinds=[{'jinja2': '**/*.j2'}, {'jinja2': '**/*.j2.*'}, {'yaml': '.github/**/*.{yaml,yml}'}, {'text': '**/templates/**/*.*'}, {'execution-environment': '**/execution-environment.yml'}, {'ansible-lint-config': '**/.ansible-lint'}, {'ansible-lint-config': '**/.config/ansible-lint.yml'}, {'ansible-navigator-config': '**/ansible-navigator.{yaml,yml}'}, {'inventory': '**/inventory/**.{yaml,yml}'}, {'requirements': '**/meta/requirements.{yaml,yml}'}, {'galaxy': '**/galaxy.yml'}, {'reno': '**/releasenotes/*/*.{yaml,yml}'}, {'vars': '**/{host_vars,group_vars,vars,defaults}/**/*.{yaml,yml}'}, {'tasks': '**/tasks/**/*.{yaml,yml}'}, {'rulebook': '**/rulebooks/*.{yml,yaml'}, {'playbook': '**/playbooks/*.{yml,yaml}'}, {'playbook': '**/*playbook*.{yml,yaml}'}, {'role': '**/roles/*/'}, {'handlers': '**/handlers/*.{yaml,yml}'}, {'test-meta': '**/tests/integration/targets/*/meta/main.{yaml,yml}'}, {'meta': '**/meta/main.{yaml,yml}'}, {'meta-runtime': '**/meta/runtime.{yaml,yml}'}, {'role-arg-spec': '**/meta/argument_specs.{yaml,yml}'}, {'yaml': '.config/molecule/config.{yaml,yml}'}, {'requirements': '**/molecule/*/{collections,requirements}.{yaml,yml}'}, {'yaml': '**/molecule/*/{base,molecule}.{yaml,yml}'}, {'requirements': '**/requirements.{yaml,yml}'}, {'playbook': '**/molecule/*/*.{yaml,yml}'}, {'yaml': '**/{.ansible-lint,.yamllint}'}, {'changelog': '**/changelogs/changelog.yaml'}, {'yaml': '**/*.{yaml,yml}'}, {'yaml': '**/.*.{yaml,yml}'}, {'sanity-ignore-file': '**/tests/sanity/ignore-*.txt'}], mock_filters=[], mock_modules=[], mock_roles=[], loop_var_prefix=None, only_builtins_allow_collections=[], only_builtins_allow_modules=[], var_naming_pattern=None, offline=False, project_dir='..', extra_vars=None, enable_list=[], skip_action_validation=True, strict=False, rules={}, profile='production', task_name_prefix='{stem} | ', sarif_file=None, list_profiles=False, progressive=False, rulesdir=[], use_default_rules=False, generate_ignore=False, config_file='/code/code/.config/ansible-lint.yml', ignore_file=None, version=False, cache_dir_lock=<filelock._unix.UnixFileLock object at 0x7f6ef7b739d0>)
    DEBUG    /code/code/production
    DEBUG    Effective yamllint rules used: {'anchors': {'level': 'error', 'forbid-undeclared-aliases': True, 'forbid-duplicated-anchors': False}, 'braces': {'level': 'error', 'forbid': False, 'min-spaces-inside': 0, 'max-spaces-inside': 1, 'min-spaces-inside-empty': -1, 'max-spaces-inside-empty': -1}, 'brackets': {'level': 'error', 'forbid': False, 'min-spaces-inside': 0, 'max-spaces-inside': 0, 'min-spaces-inside-empty': -1, 'max-spaces-inside-empty': -1}, 'colons': {'level': 'error', 'max-spaces-before': 0, 'max-spaces-after': 1}, 'commas': {'level': 'error', 'max-spaces-before': 0, 'min-spaces-after': 1, 'max-spaces-after': 1}, 'comments': {'level': 'warning', 'require-starting-space': True, 'ignore-shebangs': True, 'min-spaces-from-content': 1}, 'comments-indentation': False, 'document-end': False, 'document-start': False, 'empty-lines': {'level': 'error', 'max': 2, 'max-start': 0, 'max-end': 0}, 'empty-values': False, 'float-values': False, 'hyphens': {'level': 'error', 'max-spaces-after': 1}, 'indentation': {'level': 'error', 'spaces': 'consistent', 'indent-sequences': True, 'check-multi-line-strings': False}, 'key-duplicates': {'level': 'error'}, 'key-ordering': False, 'line-length': {'level': 'error', 'max': 160, 'allow-non-breakable-words': True, 'allow-non-breakable-inline-mappings': False}, 'new-line-at-end-of-file': {'level': 'error'}, 'new-lines': {'level': 'error', 'type': 'unix'}, 'octal-values': {'forbid-implicit-octal': True, 'forbid-explicit-octal': True, 'level': 'error'}, 'quoted-strings': False, 'trailing-spaces': {'level': 'error'}, 'truthy': {'level': 'warning', 'allowed-values': ['true', 'false'], 'check-keys': True}}
    DEBUG    Activating rule `avoid-dot-notation` due to profile `production`
    DEBUG    Activating rule `sanity` due to profile `production`
    DEBUG    Activating rule `fqcn` due to profile `production`
    DEBUG    Activating rule `import-task-no-when` due to profile `production`
    DEBUG    Activating rule `meta-no-dependencies` due to profile `production`
    DEBUG    Activating rule `single-entry-point` due to profile `production`
    DEBUG    Activating rule `use-loop` due to profile `production`
    DEBUG    Activating rule `galaxy` due to profile `shared`
    DEBUG    Activating rule `ignore-errors` due to profile `shared`
    DEBUG    Activating rule `layout` due to profile `shared`
    DEBUG    Activating rule `meta-incorrect` due to profile `shared`
    DEBUG    Activating rule `meta-no-tags` due to profile `shared`
    DEBUG    Activating rule `meta-video-links` due to profile `shared`
    DEBUG    Activating rule `meta-version` due to profile `shared`
    DEBUG    Activating rule `meta-runtime` due to profile `shared`
    DEBUG    Activating rule `no-changed-when` due to profile `shared`
    DEBUG    Activating rule `no-changelog` due to profile `shared`
    DEBUG    Activating rule `no-handler` due to profile `shared`
    DEBUG    Activating rule `no-relative-paths` due to profile `shared`
    DEBUG    Activating rule `max-block-depth` due to profile `shared`
    DEBUG    Activating rule `max-tasks` due to profile `shared`
    DEBUG    Activating rule `unsafe-loop` due to profile `shared`
    DEBUG    Activating rule `avoid-implicit` due to profile `safety`
    DEBUG    Activating rule `latest` due to profile `safety`
    DEBUG    Activating rule `package-latest` due to profile `safety`
    DEBUG    Activating rule `risky-file-permissions` due to profile `safety`
    DEBUG    Activating rule `risky-octal` due to profile `safety`
    DEBUG    Activating rule `risky-shell-pipe` due to profile `safety`
    DEBUG    Activating rule `name` due to profile `moderate`
    DEBUG    Activating rule `name` due to profile `moderate`
    DEBUG    Activating rule `name` due to profile `moderate`
    DEBUG    Activating rule `spell-var-name` due to profile `moderate`
    DEBUG    Activating rule `command-instead-of-module` due to profile `basic`
    DEBUG    Activating rule `command-instead-of-shell` due to profile `basic`
    DEBUG    Activating rule `deprecated-bare-vars` due to profile `basic`
    DEBUG    Activating rule `deprecated-local-action` due to profile `basic`
    DEBUG    Activating rule `deprecated-module` due to profile `basic`
    DEBUG    Activating rule `inline-env-var` due to profile `basic`
    DEBUG    Activating rule `key-order` due to profile `basic`
    DEBUG    Activating rule `literal-compare` due to profile `basic`
    DEBUG    Activating rule `jinja` due to profile `basic`
    DEBUG    Activating rule `no-free-form` due to profile `basic`
    DEBUG    Activating rule `no-jinja-when` due to profile `basic`
    DEBUG    Activating rule `no-tabs` due to profile `basic`
    DEBUG    Activating rule `partial-become` due to profile `basic`
    DEBUG    Activating rule `playbook-extension` due to profile `basic`
    DEBUG    Activating rule `role-name` due to profile `basic`
    DEBUG    Activating rule `schema` due to profile `basic`
    DEBUG    Activating rule `name` due to profile `basic`
    DEBUG    Activating rule `var-naming` due to profile `basic`
    DEBUG    Activating rule `yaml` due to profile `basic`
    DEBUG    Activating rule `internal-error` due to profile `min


Output on 6.14.4:

    /code/code/production # ansible-lint -v
    INFO     Set ANSIBLE_LIBRARY=/root/.cache/ansible-compat/ab8e18/modules:/root/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
    INFO     Set ANSIBLE_COLLECTIONS_PATH=/root/.cache/ansible-compat/ab8e18/collections:/root/.ansible/collections:/usr/share/ansible/collections
    INFO     Set ANSIBLE_ROLES_PATH=/root/.cache/ansible-compat/ab8e18/roles:roles:/root/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
    INFO     Discovered files to lint using: git -c safe.directory=/code/code/production ls-files --cached --others --exclude-standard -z
    INFO     Excluded removed files using: git -c safe.directory=/code/code/production ls-files --deleted -z
    INFO     Discovered files to lint using: git -c safe.directory=/code/code/production ls-files --cached --others --exclude-standard -z
    INFO     Excluded removed files using: git -c safe.directory=/code/code/production ls-files --deleted -z
    INFO     Executing syntax check on playbook site.yml (1.35s)
    
    Passed with production profile: 0 failure(s), 0 warning(s) on 5 files.
    A new release of ansible-lint is available: 6.14.4 → 6.16.2


