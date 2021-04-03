---
description: Durante una instalación Windows Installer, el instalador puede buscar una entrada del registro y crear una propiedad que contenga el valor del registro.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Buscar una entrada del registro y crear una propiedad que contiene el valor del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907685"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Buscar una entrada del registro y crear una propiedad que contiene el valor del registro

**Para buscar una entrada del registro y crear una propiedad que contenga el valor de ese archivo**

1.  No agregue la firma a la [tabla de firma](signature-table.md) o a la [tabla CompLocator](complocator-table.md). Si una firma de archivo se muestra en la [tabla AppSearch](appsearch-table.md) y no aparece en las tablas Signature o CompLocator, el instalador busca en la [tabla RegLocator](reglocator-table.md).

2.  Especifique la entrada del registro que se va a buscar en la [tabla RegLocator](reglocator-table.md). Si la firma no está presente en la [tabla de signatura](signature-table.md) y el valor de la columna Type es **msidbLocatorTypeRawValue**, se supone que la búsqueda es para el nombre de clave del registro específico al que apunta la tabla RegLocator.

    [Tabla RegLocator](reglocator-table.md) (parcial)

    

    | Signatura\_         | Root         | Clave                                                           | Nombre                  | Tipo                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **Software** \\ de **Microsoft** \\ **MyApp**<br/> <br/> | **Myname**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  Por último, rellene la [tabla AppSearch](appsearch-table.md) para que la [acción AppSearch](appsearch-action.md) devuelva el valor de AppValue. Después de que el instalador ejecute la acción AppSearch, el valor de MYREGVAL es el valor de AppValue.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad            | Firma           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




