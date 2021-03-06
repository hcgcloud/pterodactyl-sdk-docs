# Utilization Server <small>with Account API</small>
Get the utilization of a given server.

## Usage
``` php
<?php
	$pterodactyl->utilizationServer($serverIdentifier);
?>
```

## Parameters

!!! note
    The `serverIdentifier` is the `identifier` of the server, not `id`, `externalId` or `uuid`.

| Parameter | Description | Rules |
| - | - | - |
| serverIdentifier | The `identifier` of the server | |

## Returns

``` json
{
	"cpu": {
		"current": 199.337,
		"cores": [16.999, 105.385, 1.226, 1.764, 4.335, 0.559, 14.094, 0, 53.014, 1.962, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
		"limit": 0
	},
	"disk": {
		"current": 205,
		"limit": 256
	},
	"memory": {
		"current": 97,
		"limit": 128
	},
	"state": "on",
	"object": "stats"
}
```

## Example

``` php
<?php
	$server = $pterodactyl->utilizationServer('76c59598');
	print_r($server);
?>
```