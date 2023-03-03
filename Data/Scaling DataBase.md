## Cold Standby

We have 2 DataBases 1 that copy periodically from the other.

1 get the server request and the other one just copy after 1 hour, 1 day the data

Vertical scaling

IMAGE

## Warm Standby

This implies a replication of the primary DataBase.

We have a DataBase that gets requests from the server and the other one that replicates the main one.

We can implemet the replication routine, but also we can use the already existing ones.

Vertical scaling

IMAGE

## Hot Standby

In this one we are writing in all DataBases at the same time. This is kind of Horizontaly Scaling.

## Sharding

In sharding we have the primary DataBases as Shards and for each of them we have a backup shard in order to mentain the data save.

IMAGE

When we are working with No-SQL DataBase we will chose a shard and we will try to put all data for that customer in that shard, in order to do no make any join operation.

Exampels of No-SQL DataBase:

### MongoDB

In MondoDB the Shard is called Replica-Set and each Shard can have multiple Secondaryies, which are the backups. In this way we can have a Secondary for a region and that is scalble.

But in this case we have only one point to entry

IMAGE

### Cassandra

We have a router that will chose the shard to send
