---
description: Durante una Windows instalador, el instalador puede buscar un archivo en todas las unidades fijas.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Buscar un archivo en todas las unidades fijas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d460cd55fe54a98c6a02e23e49af9ea9838c7651262fa03f868bdb76acc2d506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041255"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Buscar un archivo en todas las unidades fijas

**Para buscar un archivo en todas las unidades fijas**

1.  Escriba la firma de archivo y el nombre en la [tabla de firma](signature-table.md). Los campos restantes de este registro pueden ser NULL para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md) (parcial)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla de AppSearch](appsearch-table.md)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md). Deje los campos Primario y Ruta de acceso vacíos para buscar en todas las unidades fijas del sistema de usuario. Especifique en la columna Profundidad el número de niveles de subdirectorio que se buscarán. Por ejemplo, si se establece Profundidad en 0, se detecta c:MyApp.exe, pero no se detecta el archivo en una profundidad de 2, por ejemplo: c: Archivos de \\ \\ programa \\ MyApps \\MyApp.exe.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma          | Parent | Ruta de acceso | Profundidad        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones. Si MyApp.exe está instalado, el instalador establece la propiedad MYAPP en la ubicación del archivo. Si el archivo está instalado, MYAPP se evalúa como True en una expresión condicional.

 

 




