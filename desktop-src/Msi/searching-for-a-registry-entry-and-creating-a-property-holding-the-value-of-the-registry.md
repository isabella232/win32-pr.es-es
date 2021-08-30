---
description: Durante una Windows installer, el instalador puede buscar una entrada del Registro y crear una propiedad que mantiene el valor del registro.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Buscar una entrada del Registro y crear una propiedad que mantiene el valor del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a1d02c7c39b6de07ddc0e76d202420386ae2c55d3f70106cd88432a53ec854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041125"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Buscar una entrada del Registro y crear una propiedad que mantiene el valor del Registro

**Para buscar una entrada del Registro y crear una propiedad que mantiene el valor de ese archivo**

1.  No agregue la firma a la tabla [de firmas](signature-table.md) o a la [tabla CompLocator](complocator-table.md). Si una firma de archivo aparece en la tabla [AppSearch](appsearch-table.md) y no aparece en las tablas Signature o CompLocator, el instalador busca en la [tabla RegLocator](reglocator-table.md).

2.  Especifique la entrada del Registro que se va a buscar en la [tabla RegLocator](reglocator-table.md). Si la firma no está presente en la tabla [de](signature-table.md) firmas y el valor de la columna Type es **msidbLocatorTypeRawValue**, se supone que la búsqueda es para el nombre de clave del Registro específico al que apunta la tabla RegLocator.

    [Tabla RegLocator](reglocator-table.md) (parcial)

    

    | Firma\_         | Root         | Clave                                                           | Nombre                  | Tipo                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **SOFTWARE** \\ **Microsoft** \\ **MyApp**<br/> <br/> | **Minombre**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  Por último, rellene la [tabla AppSearch para](appsearch-table.md) que la [acción AppSearch](appsearch-action.md) devuelva el valor de AppValue. Una vez que el instalador ejecuta la acción AppSearch, el valor de MYREGVAL es el valor de AppValue.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad            | Firma           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




