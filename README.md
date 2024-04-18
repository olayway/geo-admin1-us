Geodata [data package][datapackage] providing geojson polygons for the states in the USA.


## Data
The data comes from [Natural Earth][naturalearth], a community effort to make visually pleasing, well-crafted maps with cartography or GIS software at small scale.

This dataset covers the United States of America. admin1 are the biggest administrative area below the country : ie the states. See [documentation][doc] for more information.

The shape of the admin1 have four fields : 
* name : the common name for this admin1 subdivision
* id : Natural Earth ``adm1_code`` for the subdivision inside the country. [Documentation][doc] is not clear what this code is, but it could be FIPS
* code : the well known two letter code for the state
* country : name of the country
* ISO3166-1-Alpha-3 : three letters iso code of the country

[naturalearth]: http://www.naturalearthdata.com/
[datapackage]: http://dataprotocols.org/data-packages/
[doc]: http://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-1-states-provinces/

## License

All data is licensed under the [Open Data Commons Public Domain Dedication and License][pddl]. 

Note that the original data from [Natural Earth][naturalearth] is public domain. While no credit is 
formally required a link back or credit to [Natural Earth][naturalearth], [Lexman][lexman] and the [Open Knowledge Foundation][okfn] is much appreciated.

All source code is licenced under the [MIT licence][mit].

<Map
  center={{
    latitude: 45,
    longitude: 0
  }}
  layers={[
    {
      colorScale: {
        ending: '#00ff00',
        starting: '#ff0000'
      },
      data: './data/admin1-us.geojson',
      url: './data/admin1-us.geojson',
      name: 'Polygons',
      tooltip: {
        propNames: [
          'name'
        ]
      }
    }
  ]}
  title="Seas and Oceans Map"
  zoom={2}
/>

