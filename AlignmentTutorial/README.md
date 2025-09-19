# Tutorial: Generating Ontology Alignments with LogMap

This tutorial shows how to generate ontology alignments using the [LogMap](https://github.com/ernestojimenezruiz/logmap-matcher) tool.  
LogMap is a state-of-the-art ontology matching system that combines lexical and structural matching strategies and includes logical reasoning to ensure that the resulting ontology network is consistent.

---




## Clone this projet

```bash
$ git clone git@github.com:huanyu-li/test.git
$ cd test
```

## Clone the LogMap repository or download a release
```bash
$ git clone https://github.com/ernestojimenezruiz/logmap-matcher.git
$ cd logmap-matcher
```


## Compile using maven:
```bash
$ mvn clean package
```

This creates an executable JAR in the `target` directory

Alternatively, download a precompiled distribution from the [relase page](https://github.com/ernestojimenezruiz/logmap-matcher/releases).

## Running LogMap

**Java 11+** (required to run LogMap)  
  Verify with:
  ```bash
  $ java -version
  ```

```bash
$ java -jar logmap-matcher-<version>.jar MATCHER \
  http://w3id.org/CEON/ontology/product/ \
  http://w3id.org/dppo/ontology/dpp-core/ \
  /absolute_path_of_output/
```

- MATCHER tells LogMap to perform ontology matching.
- ontologyA.owl and ontologyB.owl are the input ontologies.
- /absolute_path_of_output/ is the absolute path of the location where you want to save the output alignments.

## Understanding the Output

After running LogMap, the absolute_path_of_output/ folder will contain:
logmap2_mappings.rdf – The alignment in RDF format (recommended for interoperability).
logmap2_mappings.txt – The alignment in a simple tabular text format.
A typical mapping in RDF format looks like:

```
<map>
	<Cell>
		<entity1 rdf:resource="http://w3id.org/CEON/ontology/product/Product"/>
		<entity2 rdf:resource="http://w3id.org/dppo/ontology/dpp-odp/Product"/>
		<measure rdf:datatype="xsd:float">0.5</measure>
		<relation>=</relation>
	</Cell>
</map>
```

## Optional: Converting to SSSOM

For richer metadata, you can convert RDF mappings into the SSSOM tabular format (tSV).
We provide a small converter script in this project:
```bash
$ python3 -m venv matching-venv
$ source matching-venv/bin/activate
$ pip3 install -r requirements.txt
$ python rdf2sssom.py --config config.yaml
```

The config.yaml looks like this:
```
input_file: /absolute_path_of_output/logmap2_mappings.rdf
output_file: ./aligments.tsv
tool: LogMap 

# optional
verbose: true
```


