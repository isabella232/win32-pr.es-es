---
description: Durante una instalación Windows Installer, el instalador puede buscar un archivo en todas las unidades fijas.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Buscar un archivo en todas las unidades fijas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678031"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Buscar un archivo en todas las unidades fijas

**Para buscar un archivo en todas las unidades fijas**

1.  Escriba la firma y el nombre del archivo en la [tabla de firmas](signature-table.md). Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md) (parcial)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla AppSearch](appsearch-table.md)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md). Deje vacíos los campos primario y de ruta de acceso para buscar en todas las unidades fijas del sistema de usuario. Especifique en la columna profundidad el número de niveles de subdirectorio que se van a buscar. Por ejemplo, establecer Depth en 0 detecta c: \\MyApp.exe, pero no detecta el archivo a una profundidad de 2, por ejemplo: c: archivos de \\ programa \\ mis aplicaciones \\MyApp.exe.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma          | Parent | Ruta | Profundidad        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones. Si MyApp.exe está instalado, el instalador establece la propiedad MYAPP en la ubicación del archivo. Si el archivo está instalado, MYAPP se evalúa como true en una expresión condicional.

 

 




