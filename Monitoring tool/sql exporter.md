
SQL Exporter : https://github.com/free/sql_exporter




1. install "go" from https://go.dev/doc/install if not installed 
2. verify cmd > "go version"
4. use "go install github.com/free/sql_exporter/cmd/sql_exporter@latest"
5. create sql_exporter.yml [[sql_exporter.yml]]
6. create "pricing_data_freshness.collector.yml" [[pricing_data_freshness.collector.yml]]
7. run "sql_exporter -config.file sql_exporter.yml"




