---
description: El estado de instalación de un archivo complementario no depende de su propia información de control de versiones de archivo, sino del control de versiones de su elemento primario complementario.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Archivos complementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d35aa89e216df4e17c84fb15c9c1f19908a74e9c1d14113da4df2128cdfb87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145104"
---
# <a name="companion-files"></a>Archivos complementarios

El estado de instalación de un archivo complementario no depende de su propia información de control de versiones de archivo, sino del control de versiones de su elemento primario complementario. Vea Las reglas [de control de versiones de archivos](file-versioning-rules.md). Para especificar un archivo complementario, la clave [](file-table.md) principal del elemento primario complementario de la tabla Archivo debe crearse en la columna Versión del registro del elemento complementario.

En el ejemplo siguiente, FileA es el elemento primario complementario y FileB es el archivo complementario.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Versión |
|-------|---------|
| Archivo A | 1.0.0.0 |
| FileB | Archivo A   |



 

En este ejemplo, el estado de instalación de FileB depende de las reglas de [control](file-versioning-rules.md) de versiones de archivo y de la información de control de versiones de FileA. Si el instalador determina que la versión de FileA del paquete debe instalarse sobre una versión anterior de FileA que ya existe en el equipo del usuario, también instalará FileB desde el paquete independientemente de la versión de cualquier ArchivoB instalado.

Tenga en cuenta que un archivo que sea la ruta de acceso de clave para su componente no debe ser un archivo complementario. Esto daría lugar a que el archivo primario complementario determinara la lógica de control de versiones del archivo de ruta de acceso de clave.

 

 



