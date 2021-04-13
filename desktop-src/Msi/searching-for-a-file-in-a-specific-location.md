---
description: Durante una instalación Windows Installer, el instalador puede buscar un archivo en una ubicación específica en el sistema del usuario.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Buscar un archivo en una ubicación específica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546022"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Buscar un archivo en una ubicación específica

**Para buscar un archivo en una ubicación específica en un sistema de usuarios**

1.  Enumere la firma y el nombre del archivo en la [tabla de firmas](signature-table.md). Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.

    [Tabla de firmas](signature-table.md)

    

    | Firma          | Nombre de archivo            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.

    [Tabla AppSearch](appsearch-table.md) (parcial)

    

    | Propiedad         | Firma          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md). Escriba la ruta de acceso completa al archivo en el sistema de usuario en el campo ruta de acceso. Escriba un valor de 0 en la columna de profundidad para buscar en la carpeta bin.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma          | Parent | Ruta                                                    | Profundidad        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ archivos de programa \\ suproducts \\ bin de proyectos \\<br/> | 0<br/> |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones. Si MyApp.exe está instalado en C: \\ archivos de programa \\ suproducts \\ \\ bin, el instalador establece la propiedad MyApp en la ubicación del archivo.

 

 




