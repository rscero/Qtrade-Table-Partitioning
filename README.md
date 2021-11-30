# Qtrade-Table-Partitioning

1. Determine partitioning key and retention periods
2. Create schemes and function (see existing objects for examples)
	Should be a single function created: pf<tablename>
	Should be two schemes created: 	ps<tablename> on DATA filegroup
									ps<tablename>_NCX on INDEXES filegroup
		both using the single function
3. Add data to PostDeployment .\Data\TablePartitions.sql file (example in the file)
4. Partition the table (see sample script in manual scripts\Partitioning Scripts folder) 
