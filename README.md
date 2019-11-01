# Report Phase 1

## rs.status()
```
rs0:SECONDARY> rs.status()
{
        "set" : "rs0",
        "date" : ISODate("2019-11-01T07:07:26.854Z"),
        "myState" : 2,
        "term" : NumberLong(1),
        "syncingTo" : "mongodb1:27017",
        "syncSourceHost" : "mongodb1:27017",
        "syncSourceId" : 0,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572592040, 1),
                        "t" : NumberLong(1)
                },
                "lastCommittedWallTime" : ISODate("2019-11-01T07:07:20.085Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572592040, 1),
                        "t" : NumberLong(1)
                },
                "readConcernMajorityWallTime" : ISODate("2019-11-01T07:07:20.085Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572592040, 1),
                        "t" : NumberLong(1)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572592040, 1),
                        "t" : NumberLong(1)
                },
                "lastAppliedWallTime" : ISODate("2019-11-01T07:07:20.085Z"),
                "lastDurableWallTime" : ISODate("2019-11-01T07:07:20.085Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572592040, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572592040, 1),
        "members" : [
                {
                        "_id" : 0,
                        "name" : "mongodb1:27017",
                        "ip" : "10.0.0.3",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 166277,
                        "optime" : {
                                "ts" : Timestamp(1572592040, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572592040, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:07:20Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:07:20Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:07:26.450Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:07:26.449Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572425778, 1),
                        "electionDate" : ISODate("2019-10-30T08:56:18Z"),
                        "configVersion" : 1
                },
                {
                        "_id" : 1,
                        "name" : "mongodb2:27017",
                        "ip" : "10.0.0.2",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 166277,
                        "optime" : {
                                "ts" : Timestamp(1572592040, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572592040, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:07:20Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:07:20Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:07:26.491Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:07:26.491Z"),
                        "pingMs" : NumberLong(1),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "mongodb1:27017",
                        "syncSourceHost" : "mongodb1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                },
                {
                        "_id" : 2,
                        "name" : "mongodb3:27017",
                        "ip" : "10.0.0.4",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 166281,
                        "optime" : {
                                "ts" : Timestamp(1572592040, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:07:20Z"),
                        "syncingTo" : "mongodb1:27017",
                        "syncSourceHost" : "mongodb1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572592040, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572592040, 1)
}
```

## rs.config()
```
rs0:SECONDARY> rs.config()
{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "mongodb1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "mongodb2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "mongodb3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5db95028bc53b62bc6170cfd")
        }
}
```

## Screenshot
![Most recent messages](https://i.imgur.com/g8ra4sP.png)

# Report Phase 2
## rs.status()
```
rs0:SECONDARY> rs.status()
{
        "set" : "rs0",
        "date" : ISODate("2019-11-01T07:16:05.323Z"),
        "myState" : 2,
        "term" : NumberLong(2),
        "syncingTo" : "mongodb2:27017",
        "syncSourceHost" : "mongodb2:27017",
        "syncSourceId" : 1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572592563, 1),
                        "t" : NumberLong(2)
                },
                "lastCommittedWallTime" : ISODate("2019-11-01T07:16:03.438Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572592563, 1),
                        "t" : NumberLong(2)
                },
                "readConcernMajorityWallTime" : ISODate("2019-11-01T07:16:03.438Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572592563, 1),
                        "t" : NumberLong(2)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572592563, 1),
                        "t" : NumberLong(2)
                },
                "lastAppliedWallTime" : ISODate("2019-11-01T07:16:03.438Z"),
                "lastDurableWallTime" : ISODate("2019-11-01T07:16:03.438Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572592515, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572592515, 1),
        "members" : [
                {
                        "_id" : 0,
                        "name" : "mongodb1:27017",
                        "ip" : "10.0.0.3",
                        "health" : 0,
                        "state" : 8,
                        "stateStr" : "(not reachable/healthy)",
                        "uptime" : 0,
                        "optime" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDate" : ISODate("1970-01-01T00:00:00Z"),
                        "optimeDurableDate" : ISODate("1970-01-01T00:00:00Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:16:04.715Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:13:52.714Z"),
                        "pingMs" : NumberLong(1),
                        "lastHeartbeatMessage" : "Couldn't get a connection within the time limit",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "configVersion" : -1
                },
                {
                        "_id" : 1,
                        "name" : "mongodb2:27017",
                        "ip" : "10.0.0.2",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 166796,
                        "optime" : {
                                "ts" : Timestamp(1572592563, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572592563, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:16:03Z"),
                        "optimeDurableDate" : ISODate("2019-11-01T07:16:03Z"),
                        "lastHeartbeat" : ISODate("2019-11-01T07:16:04.824Z"),
                        "lastHeartbeatRecv" : ISODate("2019-11-01T07:16:03.633Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572592443, 1),
                        "electionDate" : ISODate("2019-11-01T07:14:03Z"),
                        "configVersion" : 1
                },
                {
                        "_id" : 2,
                        "name" : "mongodb3:27017",
                        "ip" : "10.0.0.4",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 166800,
                        "optime" : {
                                "ts" : Timestamp(1572592563, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-11-01T07:16:03Z"),
                        "syncingTo" : "mongodb2:27017",
                        "syncSourceHost" : "mongodb2:27017",
                        "syncSourceId" : 1,
                        "infoMessage" : "",
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572592563, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572592563, 1)
}
```

## rs.config()
```
rs0:SECONDARY> rs.config()
{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "mongodb1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "mongodb2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "mongodb3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5db95028bc53b62bc6170cfd")
        }
}
```

## Screenshot
![Most Recent messages](https://i.imgur.com/18BmpqF.png)
