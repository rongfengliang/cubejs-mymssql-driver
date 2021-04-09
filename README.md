# cube.js for mssql driver

> fork form official driver 

## Usage

* .env

just like official docs 


* cube.js

```code
const {MSSqlDriver,MssqlQuery} = require("@dalongrong/mymssql-driver")
module.exports = {
    dialectFactory: (dataSource) => {
        // need config  datasource  for multitenant env
        return MssqlQuery
    },
    dbType: ({ dataSource } = {}) => {
        return "mymssql"
    },
    driverFactory: ({ dataSource } = {}) => {
        return new MSSqlDriver({})
    }
};
```