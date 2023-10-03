# Ahu 
Ceremonial platform where worship was offered to the ancestors. Constructed from fitted stones, they form the foundation where the Moai would later be placed.

# Description
The package downloads all ImpactU products (approximately 203672). From these products, a filter is applied to identify those that do not have Google Scholar information. Subsequently, a copy of the filtered products is created with the necessary fields for implementing the Moai package.
All databases are stored in MongoDB.
## Dependence
* Install MongoDB.
Installation guide at https://www.mongodb.com/docs/manual/administration/install-community/

## Install package
```bash
$ pip install -i https://test.pypi.org/simple/ ahu
```
## Usage

```bash
>>> ahu_run -- db_name="my_db" --original_collection_name="No_Scholar" --filtered_collection_name="For_Moai" ----keep_abstract=False
```

Output
An example of the fields in the for_moai collection is:
```bash
{
	"_id" : ObjectId(),
	"journal" : "Brazilian Journal of Biology",
	"publisher" : "Instituto Internacional de Ecologia",
	"country" : "BR",
	"title" : "New records of Coronatella (Crustacea, Branchiopoda, Chydoridae) from Colombia with the first report of Coronatella undata and of the male of Coronatella monacantha",
	"author" : "JM, Fuentes-Reinés and P, Eslava and LMA, Elmoor-Loureiro",
	"year" : 2024,
	"volume" : "84",
	"issue" : "",
	"page" : "",
	"language" : "en",
	"abstract" : "",
	"doi" : "10.1590/1519-6984.254487",
	"pmid" : "https://pubmed.ncbi.nlm.nih.gov/35293542"
}

```
If an error occurs during execution, be sure to delete the collections or rename them, as this will present problems with the identifiers generated by MongoDB.

Links:
* [Test pip page](https://test.pypi.org/project/Ahu/)
* Flake8 Tool For Style Guide Enforcement
  * https://flake8.pycqa.org/ 
  * https://peps.python.org/pep-0008/
* [GitHub actions](https://help.github.com/en/actions/language-and-framework-guides/using-python-with-github-actions)