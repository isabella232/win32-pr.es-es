---
description: Durante una Windows instalador, el instalador puede buscar un archivo y crear una propiedad que contenga la ruta de acceso del archivo.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Buscar un archivo y crear una propiedad que mantiene la ruta de acceso del archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069643"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Buscar un archivo y crear una propiedad que mantiene la ruta de acceso del archivo

**Para buscar un archivo y crear una propiedad que mantiene la ruta de acceso de ese archivo**

1.  En primer lugar, realice una búsqueda del archivo enumerando la firma y el nombre del archivo en la [tabla de firma](signature-table.md).

    Los campos restantes de este registro se pueden dejar vacíos para especificar una búsqueda de cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md) (parcial)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  A continuación, especifique la ruta de acceso del archivo que se está buscando en la [tabla DrLocator](drlocator-table.md).

    Dado que AppFolder no aparece en la tabla [de](signature-table.md)firma, el instalador determina que AppFolder es una carpeta en lugar de un archivo.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma            | Parent             | Ruta de acceso | Profundidad |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Por último, rellene la [tabla AppSearch para](appsearch-table.md) que la [acción AppSearch](appsearch-action.md) devuelva la ruta de acceso de AppFolder.

    Después de que el instalador ejecute la acción AppSearch, el valor de MYFOLDER es la ruta de acceso completa de AppFolder.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad            | Firma            |
    |---------------------|----------------------|
    | MYFOLDER<br/> | AppFolder<br/> |

    

     

 

 




