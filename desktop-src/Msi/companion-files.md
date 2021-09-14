---
description: El estado de instalación de un archivo complementario no depende de su propia información de control de versiones de archivo, sino del control de versiones de su elemento primario complementario.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Archivos complementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158856"
---
# <a name="companion-files"></a>Archivos complementarios

El estado de instalación de un archivo complementario no depende de su propia información de control de versiones de archivo, sino del control de versiones de su elemento primario complementario. Consulte las [reglas de control de versiones de archivos](file-versioning-rules.md). Para especificar un archivo complementario, la clave [](file-table.md) principal del elemento primario complementario de la tabla Archivo debe crearse en la columna Versión del registro del elemento complementario.

En el ejemplo siguiente, FileA es el elemento primario complementario y FileB es el archivo complementario.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Versión |
|-------|---------|
| ArchivoA | 1.0.0.0 |
| FileB | ArchivoA   |



 

En este ejemplo, el estado de instalación de FileB depende de las reglas de [control](file-versioning-rules.md) de versiones de archivo y de la información de control de versiones de FileA. Si el instalador determina que la versión de FileA del paquete debe instalarse a través de una versión anterior de FileA que ya existe en el equipo del usuario, también instalará FileB desde el paquete independientemente de la versión de cualquier ArchivoB instalado.

Tenga en cuenta que un archivo que sea la ruta de acceso de clave para su componente no debe ser un archivo complementario. Esto daría lugar a que el archivo primario complementario determinara la lógica de control de versiones del archivo de ruta de acceso de clave.

 

 



