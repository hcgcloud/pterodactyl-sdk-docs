# Suspend Server <small>with Application API</small>
Suspend the given server.

## Usage
``` php
<?php
	$pterodactyl->suspendServer($serverId);

	//For a server instance
	$server->suspend();
?>
```

## Parameters

!!! note
    The `serverId` is the `id` of the server, not `identifier`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverId | The `id` of the server | |

## Returns
**None**

Throwing exception if failed.

## Example

``` php
<?php
	try {
		$pterodactyl->suspendServer(14);
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```

``` php
<?php
	try {
		$server = $pterodactyl->server(14);
		$server->suspend();
	} catch(\Exception $e){
		print_r($e->getMessage());
	}
?>
```