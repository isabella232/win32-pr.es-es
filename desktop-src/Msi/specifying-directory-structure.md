---
description: El instalador mantiene información sobre la estructura de directorios de instalación en la tabla de directorios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificar la estructura de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266028"
---
# <a name="specifying-directory-structure"></a>Especificar la estructura de directorios

El instalador mantiene información sobre la estructura de directorios de instalación en la [tabla de directorios](directory-table.md). Vea el [grupo Tablas principales](core-tables-group.md). En esta sección agregará información de estructura de directorios para el ejemplo Bloc de notas a la base de datos vacía que creó en [Importación de una base de datos en blanco.](importing-a-blank-database.md) Use el editor de bases de datos Orca que se proporciona con el SDK u otro editor para abrir la tabla de directorios en MNP2000.msi. Use el editor para escribir los datos siguientes en la tabla de directorios en blanco.

[Tabla de directorios](directory-table.md)



| Directorio                                        | Elemento primario \_ del directorio                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| NOCIONESDIR                                          | NOTEPADDIR                                       | Events:Events       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menú              |
| MONDIR                                           | NOTEPADDIR                                       | Puerta              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Bloc de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Deportes:Eventos     |



 

Al escribir estos datos en la tabla Directory se especifican las estructuras de directorio de origen y de destino. Consulte los [temas Tabla de directorios](directory-table.md) [y Uso de la tabla de](using-the-directory-table.md) directorios. Tenga en cuenta que [**la propiedad TARGETDIR**](targetdir.md) debe ser el nombre de una raíz de la tabla Directory de cada instalación.

[Continuar](specifying-components.md)

 

 



