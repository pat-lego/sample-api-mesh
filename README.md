# Creating an API Mesh with Venia

## Resources to watch 

- Getting Started (https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/api-mesh/getting-started-api-mesh.html?lang=en)
- Installing AIO (https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/api-mesh/installing-aio-mesh-plugin.html?lang=en)
- Working with Projects (https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/api-mesh/aio-projects-workspaces.html?lang=en)
- Create a singular mesh (https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/api-mesh/graphql-single-source.html?lang=en)
- Create a complex mesh (https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/api-mesh/graphql-multiple-source.html?lang=en)

# Project Link

https://developer.adobe.com/console/projects/35196/4566206088344973092/overview

# Developer Extensions

https://chrome.google.com/webstore/detail/graphiql-extension/jhbedfdjpmemmbghfecnaeeiokonjclb?hl=en-US

# GraphQL Schema

```
# Welcome to GraphiQL
#
# GraphiQL is an in-browser tool for writing, validating, and
# testing GraphQL queries.
#
# Type queries into this side of the screen, and you will see intelligent
# typeaheads aware of the current GraphQL type schema and live syntax and
# validation errors highlighted within the text.
#
# GraphQL queries typically start with a "{" character. Lines that start
# with a # are ignored.
#
# An example GraphQL query might look like:
#
#     {
#       field(arg: "value") {
#         subField
#       }
#     }
#
# Keyboard shortcuts:
#
#  Prettify Query:  Shift-Ctrl-P (or press the prettify button above)
#
#     Merge Query:  Shift-Ctrl-M (or press the merge button above)
#
#       Run Query:  Ctrl-Enter (or press the play button above)
#
#   Auto Complete:  Ctrl-Space (or just start typing)
#

{
  products(
    search: "a",
    pageSize: 3,
    currentPage: 1
  ) {
     items {
      uid
				name
      	sku
      	url_key
      	...on ConfigurableProduct { 
          variants {
            product {
                sku
              	price_range {
                  minimum_price {
                    final_price {
                      currency
                      value
                    }
                  }
                }
            }
          }
        }
    }
  }
}
```