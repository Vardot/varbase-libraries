# Varbase Libraries

List of needed libraries for Varbase used packages with Composer.

---

Use `"vardot/varbase-libraries": "~10.1.0"` 
> with **Varbase `~10.1.0`** and **Drupal `~11`**

---

Use `"vardot/varbase-libraries": "~10.0.0"` 
> with **Varbase `~10.0.0`** **CKEditor `5`** and **Drupal `~10`**

---

Use `"vardot/varbase-libraries": "~9.2.0"`
> with **Varbase `~9.1.0`** **CKEditor `5`** and **Drupal `~10`**

---

Use `"vardot/varbase-libraries": "~9.1.0"`
> with **Varbase `~9.1.0`** **CKEditor `4`**  and **Drupal `~10`**

---

## Managing Only Local Libraries in Projects

In case of needing to manage project's local libraries only.

* Moving to a better drupal libraries management with Varbase
* As a step to remove the use of asset-packagist.org in Varbase


NO libraries **for Varbase ~10.1.0**
> With **Drupal 10/11** :
> Use the `"vardot/varbase-libraries": "10.1.0.0"` static version to have no libraries and manage local libraries in the project with a copy of libraries from https://github.com/vardot/varbase-libraries/blob/10.1.x/composer.json or NPM/YARN

---

NO libraries **for Varbase ~10.0.0**
> With **CKEditor 5** and **Drupal 10** :
> Use the `"vardot/varbase-libraries": "10.0.0.0"` static version to have no libraries and manage local libraries in the project with a copy of libraries from https://github.com/vardot/varbase-libraries/blob/10.0.x/composer.json or NPM/YARN


---

NO libraries **For Varbase ~9.1.0**
> With **CKEditor 4** and **Drupal 10** :
> Use the `"vardot/varbase-libraries": "9.1.0.0"` static version to have no libraries and manage local libraries in the project with a copy of libraries from https://github.com/vardot/varbase-libraries/blob/9.1.x/composer.json or NPM/YARN


---

NO libraries **For Varbase ~9.1.0**
> With **CKEditor 5** and **Drupal 10** :
> Use the `"vardot/varbase-libraries": "9.2.0.0"` static version to have no libraries and manage local libraries in the project with a copy of libraries from https://github.com/vardot/varbase-libraries/blob/9.2.x/composer.json or NPM/YARN


## **Advanced:** Merge `composer.libraries.json` from `vardot/varbase-libraries` in `vendor/`

For projects that want full control over which libraries are included, without relying on **asset-packagist.org**, you can merge the libraries directly from the vardot/varbase-libraries package using [wikimedia/composer-merge-plugin](https://github.com/wikimedia/composer-merge-plugin).

**Setup Steps**

Install the merge plugin:

```
composer require wikimedia/composer-merge-plugin:~2
```
Add merge configuration to your root composer.json:

```
"extra": {
  "merge-plugin": {
    "include": [
      "vendor/vardot/varbase-libraries/composer.libraries.json"
    ],
    "recurse": true,
    "replace": false,
    "merge-dev": false
  }
}
```
