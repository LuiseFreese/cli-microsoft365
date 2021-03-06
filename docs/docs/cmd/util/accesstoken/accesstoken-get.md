# util accesstoken get

Gets access token for the specified resource

## Usage

```sh
m365 util accesstoken get [options]
```

## Options

`-r, --resource <resource>`
: The resource for which to retrieve an access token

`--new`
: Retrieve a new access token to ensure that it's valid for as long as possible

--8<-- "docs/cmd/_global.md"

## Remarks

The `util accesstoken get` command returns an access token for the specified resource. If an access token has been previously retrieved and is still valid, the command will return the cached token. If you want to ensure that the returned access token is valid for as long as possible, you can force the command to retrieve a new access token by using the `--new` option.

If the URL of your SharePoint tenant has been previously retrieved, you can use `sharepoint` as the resource to retrieve access token for SharePoint. To verify if the URL of your SharePoint tenant has been previously retrieved, use the [`spo get`](../../spo/spo-get.md) command. To explicitly set the URL of your SharePoint tenant use the [`spo set`](../../spo/spo-set.md) command.

## Examples

Get access token for the Microsoft Graph

```sh
m365 util accesstoken get --resource https://graph.microsoft.com
```

Get access token for SharePoint Online using the shorthand identifier

```sh
m365 util accesstoken get --resource sharepoint
```

Get a new access token for SharePoint Online

```sh
m365 util accesstoken get --resource https://contoso.sharepoint.com --new
```
