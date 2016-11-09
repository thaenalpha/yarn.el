# yarn.el

> yarn.el makes it convenient to work with Yarn in Node.JS projects inside Emacs.

This package provides [Emacs][emacs] support for the [Yarn][yarn] package manager.

![Demo](./yarn-el-demo.gif?raw=true "Demo")


## Commands

These commands are all available from `M-x` command menu:

| Command                             | Description                                              |
|-------------------------------------|----------------------------------------------------------|
| `yarn-add`                          | Add a dependency                                         |
| `yarn-add-dev`                      | Add a dev dependency                                     |
| `yarn-add-exact`                    | Add an exact dependency                                  |
| `yarn-add-optional`                 | Add an optional dependency                               |
| `yarn-add-peer`                     | Add a peer dependency                                    |
| `yarn-add-tilde`                    | Add a tilde dependency                                   |
| `yarn-bin`                          | Print install folder for executables                     |
| `yarn-cache-clean`                  | Clean cache                                              |
| `yarn-cache-dir`                    | Display cache directory                                  |
| `yarn-cache-ls`                     | List cached packages                                     |
| `yarn-check`                        | Validate the version of all dependencies                 |
| `yarn-check-integrity`              | Validate the version and checksum of all dependencies    |
| `yarn-clean`                        | Remove unneeded files and folders from dependencies      |
| `yarn-config-delete`                | Delete a local repository configuration key              |
| `yarn-config-get`                   | Display a local repository configuration key value       |
| `yarn-config-list`                  | List local repository configuration keys and values      |
| `yarn-config-set`                   | Set a local repository configuration key                 |
| `yarn-global-add`                   | Add a global dependency                                  |
| `yarn-global-add-exact`             | Add an exact global dependency                           |
| `yarn-global-add-tilde`             | Add a tilde global dependency                            |
| `yarn-global-config-set`            | Set a global repository configuration key                |
| `yarn-info`                         | Retrieve info on a package                               |
| `yarn-info-json`                    | Retrieve JSON-formatted info on a package                |
| `yarn-info-readme`                  | Retrieve a package README                                |
| `yarn-init`                         | Initialize a new package                                 |
| `yarn-install`                      | Install all dependencies of a package                    |
| `yarn-licenses-generate-disclaimer` | Generate a disclaimer from all package licenses          |
| `yarn-licenses-ls`                  | List all package licenses                                |
| `yarn-link`                         | Make package available to other packages for development |
| `yarn-link-package`                 | Link an available package                                |
| `yarn-login`                        | Login to the NPM registry                                |
| `yarn-logout`                       | Logout of the NPM registry                               |
| `yarn-ls`                           | List installed packages                                  |
| `yarn-outdated`                     | List outdated packages that are installed                |
| `yarn-owner-add`                    | Add a new owner to a package                             |
| `yarn-owner-ls`                     | List owners of a package                                 |
| `yarn-owner-rm`                     | Remove an owner from a package                           |
| `yarn-pack`                         | Gzip the package                                         |
| `yarn-pack-filename`                | Gzip the package to a specified file name                |
| `yarn-publish`                      | Publish package to the NPM repository                    |
| `yarn-publish-private`              | Publish package privately to the NPM repository          |
| `yarn-publish-public`               | Public package publically to the NPM repository          |
| `yarn-publish-tag`                  | Publish package to the NPM repository with a tag         |
| `yarn-remove`                       | Remove a dependency                                      |
| `yarn-run`                          | Run a script                                             |
| `yarn-self-update`                  | Update Yarn                                              |
| `yarn-update`                       | Update Yarn (alias for `yarn-self-update`)               |
| `yarn-tag-add`                      | Add a tag                                                |
| `yarn-tag-ls`                       | List all tags                                            |
| `yarn-tag-rm`                       | Remove a tag                                             |
| `yarn-test`                         | Run a test script                                        |
| `yarn-unlink`                       | Unlink a package already linked for development          |
| `yarn-upgrade`                      | Upgrade all dependencies                                 |
| `yarn-version`                      | Bump package version                                     |
| `yarn-why`                          | Information about why a package is installed             |


## Output

Command output is piped to the `*yarn*` buffer, except in the case of `yarn-licenses-generate-disclaimer` which is instead piped to the `*yarn-disclaimer*` buffer.


## Example keyboard bindings

This package does not create keyboard bindings for you, instead, you must add them to your own Emacs init script.

Example:

```elisp
(global-set-key (kbd "M-n i") 'yarn-install)
(global-set-key (kbd "M-n n") 'yarn-init)
(global-set-key (kbd "M-n a") 'yarn-add)
(global-set-key (kbd "M-n r") 'yarn-run)
(global-set-key (kbd "M-n p") 'yarn-publish)
(global-set-key (kbd "M-n t") 'yarn-test)
(global-set-key (kbd "M-n v") 'yarn-version)
(global-set-key (kbd "M-n g") 'yarn-upgrade)
(global-set-key (kbd "M-n u") 'yarn-update)
```


## Credits

Credits to [npm.el][npm.el] and contributors, which this package was forked from.


[emacs]: https://www.gnu.org/software/emacs
[yarn]: https://yarnpkg.com
[npm.el]: https://github.com/azer/npm.el
