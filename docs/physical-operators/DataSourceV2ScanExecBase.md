# DataSourceV2ScanExecBase

`DataSourceV2ScanExecBase` is an [extension](#contract) of [LeafExecNode](SparkPlan.md#LeafExecNode) abstraction for [leaf physical operators](#implementations) that [track number of output rows](#metrics) when executed ([with](#doExecuteColumnar) or [without](#doExecute) support for [columnar reads](#supportsColumnar)).

## Contract

### <span id="inputRDD"> inputRDD

```scala
inputRDD: RDD[InternalRow]
```

Used when...FIXME

### <span id="partitions"> partitions

```scala
partitions: Seq[InputPartition]
```

Used when...FIXME

### <span id="readerFactory"> readerFactory

```scala
readerFactory: PartitionReaderFactory
```

Used when...FIXME

### <span id="scan"> scan

```scala
scan: Scan
```

Used when...FIXME

## Implementations

* [BatchScanExec](BatchScanExec.md)
* ContinuousScanExec
* MicroBatchScanExec

## <span id="doExecute"> doExecute

```scala
doExecute(): RDD[InternalRow]
```

`doExecute`...FIXME

`doExecute` is part of the [SparkPlan](SparkPlan.md#doExecute) abstraction.

## <span id="doExecuteColumnar"> doExecuteColumnar

```scala
doExecuteColumnar(): RDD[ColumnarBatch]
```

`doExecuteColumnar`...FIXME

`doExecuteColumnar` is part of the [SparkPlan](SparkPlan.md#doExecuteColumnar) abstraction.

## <span id="inputRDDs"> inputRDDs

```scala
inputRDDs(): Seq[RDD[InternalRow]]
```

`inputRDDs`...FIXME

`inputRDDs` is used when...FIXME

## <span id="metrics"> metrics

```scala
metrics: Map[String, SQLMetric]
```

`metrics`...FIXME

`metrics` is part of the [SparkPlan](SparkPlan.md#metrics) abstraction.

## <span id="outputPartitioning"> outputPartitioning

```scala
outputPartitioning: physical.Partitioning
```

`outputPartitioning`...FIXME

`outputPartitioning` is part of the [SparkPlan](SparkPlan.md#outputPartitioning) abstraction.

## <span id="simpleString"> simpleString

```scala
simpleString(
    maxFields: Int): String
```

`simpleString`...FIXME

`simpleString` is part of the [TreeNode](../spark-sql-catalyst-TreeNode.md#simpleString) abstraction.

## <span id="supportsColumnar"> supportsColumnar

```scala
supportsColumnar: Boolean
```

`supportsColumnar`...FIXME

`supportsColumnar` is part of the [SparkPlan](SparkPlan.md#supportsColumnar) abstraction.