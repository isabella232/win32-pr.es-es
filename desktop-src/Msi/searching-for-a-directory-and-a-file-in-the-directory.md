---
description: Durante una Windows installer, el instalador puede buscar un directorio y un archivo en ese directorio.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Buscar un directorio y un archivo en el directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e857460dc58fa5fded802cb53b9ae6a558e5a27426baef87be9f561fa35fe6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041185"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Buscar un directorio y un archivo en el directorio

**Para buscar un directorio y, a continuación, un archivo en ese directorio**

1.  En primer lugar, busque el directorio .

    AppDir debe definirse como la firma válida del directorio. Si AppDir no se define como una firma válida, AppSearch no tiene un lugar para buscar el archivo; por ejemplo, si la búsqueda es para c: MyDirMyApp.exe, AppDir debe definirse como \\ \\ c: \\ MyDir. AppDir puede definirse mediante la inclusión de un registro en la [tabla DrLocator](drlocator-table.md)o mediante algún otro método. No se incluye ningún registro en la tabla [de firmas para](signature-table.md) la búsqueda de directorios. Para la búsqueda de archivos, enumume la firma y el nombre del archivo en la tabla de firmas. Los campos restantes de este registro pueden ser NULL para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md) (parcial)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Use la [tabla AppSearch](appsearch-table.md).

    Escriba la propiedad que va a establecer el instalador si está instalado el directorio con la firma AppDir. Si el instalador encuentra que este directorio está instalado, establece MYDIR en la ruta de acceso del directorio. Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md).

    Escriba en la columna Principal la firma, AppDir, que se define como la ruta de acceso del directorio. Especifique en la columna Profundidad el número de niveles de subdirectorio que se buscarán en este directorio. AppDir debe definirse como la firma del directorio. AppDir se puede definir incluyendo un registro como se muestra aquí o por otro método.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma | Parent | Ruta de acceso      | Profundidad |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ MyDir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones.

    Si MyApp.exe se encuentra instalado en AppDir, el instalador establece la propiedad MYAPP en la ubicación del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar aplicaciones, archivos, entradas del Registro o entradas de .ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




