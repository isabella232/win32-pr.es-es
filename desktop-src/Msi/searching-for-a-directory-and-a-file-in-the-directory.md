---
description: Durante una instalación Windows Installer, el instalador puede buscar un directorio y un archivo en ese directorio.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Buscar un directorio y un archivo en el directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667665"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Buscar un directorio y un archivo en el directorio

**Para buscar un directorio y, a continuación, un archivo en ese directorio**

1.  Primera búsqueda del directorio.

    AppDir debe definirse como la firma válida del directorio. Si AppDir no está definido como una firma válida, AppSearch no tiene un lugar donde encontrar el archivo; por ejemplo, si la búsqueda es para c: \\ MyDir \\MyApp.exe, AppDir debe definirse como c: \\ MyDir. AppDir se puede definir mediante la inclusión de un registro en la [tabla DrLocator](drlocator-table.md)o de algún otro método. No se incluye ningún registro en la [tabla de firma](signature-table.md) de la búsqueda de directorio. En la búsqueda de archivos, muestre la firma y el nombre del archivo en la tabla de firmas. Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md) (parcial)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Use la [tabla AppSearch](appsearch-table.md).

    Escriba la propiedad que va a establecer el instalador si el directorio con la firma AppDir está instalado. Si el instalador encuentra que este directorio está instalado, establece MYDIR en la ruta de acceso del directorio. Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md).

    Escriba en la columna primaria la firma, AppDir, que se define como la ruta de acceso del directorio. Especifique en la columna profundidad el número de niveles de subdirectorio que se buscarán en este directorio. AppDir debe definirse como la firma del directorio. AppDir se puede definir mediante la inclusión de un registro como se muestra aquí o mediante otro método.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma | Parent | Ruta      | Profundidad |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ MyDir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones.

    Si se encuentra MyApp.exe está instalado en AppDir, el instalador establece la propiedad MYAPP en la ubicación del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




