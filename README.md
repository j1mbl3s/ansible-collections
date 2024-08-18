# j1mbl3s/ansible-collections

My personal collection of `ansible-galaxy`... collections.

Pretty much just a bunch of roles.
I use them to manage machines on my personal network.

This probably not production ready or something, idk.
Use at your own risk.

## Installation

I declare the `j1mbl3s` namespace here, so you shouldn't go installing other collections or roles that clash with my `j1mbl3s` namespace collections.

### From source

Assuming you have cloned this repository to `../ansible-collections`:

1. Create a `requirements.yaml` file:

    ```yaml
    # requirements.yaml

    collections:

      # install all collections under the j1mbl3s namespace
      - source: ../ansible-collections/j1mbl3s
        type: subdirs

      # or a single collection, j1mbl3s.common
      - source: ../ansible-collections/j1mbl3s/common
        type: dir
    ```

2. Install the collections defined in the `requirements.yaml`:

    ```sh
    ansible-galaxy collection install -r requirements.yaml
    ```

### From GitHub

Install a collection or all collections in a namespace with the following command, replacing `[tag]`, `[namespace]` and `[collection]`.

```shell
ansible-galaxy collection install 'git@github.com:j1mbl3s/ansible-collections.git#[tag]/[namespace]/[collection]'
```

`[tag]` is optional, and uses the default branch when unspecified.

```sh
# Example: All `j1mbl3s` namespaced collections from the default branch
ansible-galaxy collection install 'git@github.com:j1mbl3s/ansible-collections.git#/j1mbl3s'

# Example: The `j1mbl3s.common` collection from the default branch
ansible-galaxy collection install 'git@github.com:j1mbl3s/ansible-collections.git#/j1mbl3s/common'
```
