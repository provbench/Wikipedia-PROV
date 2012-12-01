#  Quick guide to using the traces

## Traces content

Each archive file contains a (small) fragment of Wkipedia History pages, structured as a PROV provenance graph. The extractor pulls the content of history pages from a user-defined start page from the live Wikipedia API, and stores them into a Neo4J graph database. The resulting PROV structure, as well as the configuration options to control the crawling of the extractor, are described in a separate document. 

The traces in this folder are Neo4J DB files.  Each .tar.gz archive contains a single folder, with extension .db. The folder contains the entire content of a Neo4J data file. Thus, "loading" these files simply amounts to copying the .db file into the appropriate data folder in the Neo4J folder structure.

Here are the detailed instructions.

1. download Neo4J from [here](http://neo4j.org/ "Neo4J")

2. there is no installation. Simply unzip and move the folder wherever you like.

3. untar the trace file and move the .db folder under the data/ folder of Neo4J.

   3.1 the simplest way to get running is simply to rename the .db file to "graph.db" which is what Neo4J expects unless you tell it otherwise, using the server configuration instructions found [here](http://docs.neo4j.org/chunked/milestone/server-configuration.html)

4. start and manage the server as described in the README file.

## Queries.

File *cypher-queries.txt* contains a number of sample queries in Neo4J's Cypher query language. A nice client interface for trying them out and visualizing fragments of the traces is NeoClipse.  You can get it from [here](https://github.com/neo4j/neoclipse/downloads). Try the Cypher query editor

## Traces specification.

<table  border="2pt" align="center">
    <tr>
        <td>Filename</td>
        <td>filesize</td>
        <td>max revisions</td>
        <td>max users</td>
        <td>max depth</td>
        <td>number of nodes</td>
        <td>number of relations</td>
    </tr>

<tr>
        <td>Newcastle-r10-u3-d5.db.tar.gz</td>
        <td>3.6M</td>
        <td>10</td>
        <td>3</td>
        <td>5</td>
        <td>2758</td>
        <td>4218</td>
    </tr>

<tr>
        <td>Newcastle-r20-u1-d1.db.tar.gz</td>
        <td>80K</td>
        <td>20</td>
        <td>1</td>
        <td>1</td>
        <td>58</td>
        <td>80</td>
    </tr>

<tr>
        <td>Newcastle-r20-u5-d2.db.tar.gz</td>
        <td>203K</td>
        <td>20</td>
        <td>5</td>
        <td>2</td>
        <td>178</td>
        <td>200</td>
    </tr>

<tr>
        <td>Newcastle-r100-u25-d25.db.tar.gz</td>
        <td>6.1M</td>
        <td>100</td>
        <td>25</td>
        <td>25</td>
        <td>4044</td>
        <td>6623</td>
    </tr>

<tr>
        <td>Earthship-r100-u3-d5.db.tar.gz</td>
        <td>3.6M</td>
        <td>100</td>
        <td>3</td>
        <td>5</td>
        <td>2994</td>
        <td>4876</td>
    </tr>

<tr>
        <td>Eartships-r200-u25-d25.db.tar.gz</td>
        <td>1.2M</td>
        <td>200</td>
        <td>25</td>
        <td>25</td>
        <td>991</td>
        <td>1600</td>
    </tr>


</table>



--Paolo Missier
