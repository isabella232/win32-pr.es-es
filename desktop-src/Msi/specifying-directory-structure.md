---
description: El instalador mantiene información acerca de la estructura de directorios de instalación en la tabla de directorios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificar la estructura de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908120"
---
# <a name="specifying-directory-structure"></a>Especificar la estructura de directorios

El instalador mantiene información acerca de la estructura de directorios de instalación en la [tabla de directorios](directory-table.md). Vea el [Grupo tablas principales](core-tables-group.md). En esta sección, agregará información de la estructura de directorios para el ejemplo del Bloc de notas a la base de datos vacía que creó en la [importación de una base de datos en blanco](importing-a-blank-database.md). Use el editor de bases de datos orca que se proporciona con el SDK u otro editor para abrir la tabla de directorio en MNP2000.msi. Utilice el editor de para escribir los datos siguientes en la tabla de directorios en blanco.

[Tabla de directorio](directory-table.md)



| Directorio                                        | Directorio \_ primario                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts: eventos       |
| HOLDIR                                           | MONDIR                                           | .: Festivos        |
| MENUDIR                                          | NOTEPADDIR                                       | Menú              |
| MONDIR                                           | NOTEPADDIR                                       | Canaliza              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_Estacionamiento rojo: Bloc de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Deportes: eventos     |



 

Al escribir estos datos en la tabla de directorio se especifican las estructuras de directorio de origen y de destino. Vea la [tabla de directorios](directory-table.md) y [el uso de los temas de la tabla de directorios](using-the-directory-table.md) . Tenga en cuenta que la propiedad [**targetDir**](targetdir.md) debe ser el nombre de una raíz en la tabla de directorio de cada instalación.

[Continuar](specifying-components.md)

 

 



