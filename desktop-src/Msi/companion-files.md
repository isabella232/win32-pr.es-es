---
description: El estado de instalación de un archivo complementario no depende de su propia información de versión del archivo, sino de la versión de su elemento primario complementario.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Archivos complementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002483"
---
# <a name="companion-files"></a>Archivos complementarios

El estado de instalación de un archivo complementario no depende de su propia información de versión del archivo, sino de la versión de su elemento primario complementario. Vea las [reglas de control de versiones de archivo](file-versioning-rules.md). Para especificar un archivo complementario, la clave principal del elemento primario complementario de la [tabla de archivos](file-table.md) debe crearse en la columna versión del registro del complemento.

En el ejemplo siguiente, Filea es el elemento primario Companion y FileB es el archivo complementario.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Versión |
|-------|---------|
| Archivoa | 1.0.0.0 |
| FileB | Archivoa   |



 

En este ejemplo, el estado de instalación de FileB depende de las [reglas de control de versiones de archivo](file-versioning-rules.md) y de la información de versión de Filea. Si el instalador determina que la versión de Filea en el paquete debe instalarse en una versión anterior de Filea que ya existe en el equipo del usuario, también se instalará FileB desde el paquete, independientemente de la versión de cualquier FileB instalado.

Tenga en cuenta que un archivo que es la ruta de acceso de la clave de su componente no debe ser un archivo complementario. Como resultado, la lógica de control de versiones del archivo de ruta de acceso de la clave viene determinada por el archivo principal complementario.

 

 



