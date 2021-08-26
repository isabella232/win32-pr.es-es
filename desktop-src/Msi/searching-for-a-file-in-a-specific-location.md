---
description: Durante una Windows installer, el instalador puede buscar un archivo en una ubicación específica del sistema del usuario.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Buscar un archivo en una ubicación específica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041155"
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
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Use la [tabla DrLocator](drlocator-table.md). Escriba la ruta de acceso completa al archivo en el sistema de usuario en el campo Ruta de acceso. Escriba un valor de 0 en la columna Profundidad para buscar en la carpeta bin.

    [Tabla DrLocator](drlocator-table.md)

    

    | Firma          | Parent | Ruta de acceso                                                    | Profundidad        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ Ubicación de proyectos \\ myProducts \\ de archivos de \\ programa<br/> | 0<br/> |

    

     

4.  Incluya la acción AppSearch en la secuencia de acciones. Si MyApp.exe está instalado en la ubicación C: Archivos de programa MyProducts Projects, el instalador establece la propiedad \\ \\ \\ \\ MYAPP en la ubicación del archivo.

 

 




