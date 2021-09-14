---
description: Durante una Windows installer, el instalador puede buscar un archivo en una ubicación específica del sistema del usuario.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Buscar un archivo en una ubicación específica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069642"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Buscar un archivo en una ubicación específica

**Para buscar un archivo en una ubicación específica en un sistema de usuario**

1.  Enumume la firma y el nombre del archivo en la [tabla de firma](signature-table.md). Los campos restantes de este registro pueden ser NULL para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md). Escriba la ruta de acceso completa al archivo en el sistema de usuario en el campo Ruta de acceso. Escriba un valor de 0 en la columna Profundidad para buscar en la carpeta bin.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma          | Parent | Ruta de acceso                                                    | Profundidad        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ Ubicación de proyectos \\ myProducts \\ de archivos de \\ programa<br/> | 0<br/> |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones. Si MyApp.exe está instalado en C: Archivos de programa MyProducts Projects bin, el instalador establece la propiedad \\ \\ \\ \\ MYAPP en la ubicación del archivo.

 

 




