---
description: ICE18 valida que los directorios vacíos usados como una ruta de acceso de clave para un componente se muestran en la tabla CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666673"
---
# <a name="ice18"></a>ICE18

ICE18 valida que los directorios vacíos usados como una ruta de acceso de clave para un componente se muestran en la [tabla CreateFolder](createfolder-table.md).

Si la columna de ruta de acceso de la [tabla de componentes](component-table.md) es null, significa que el directorio que aparece en la \_ columna directorio es la ruta de acceso de la clave de ese componente. Dado que las carpetas creadas por el instalador se eliminan cuando se vacían, esta carpeta debe aparecer en la [tabla CreateFolder](createfolder-table.md) para evitar que el instalador intente instalarse cada vez.

No convierta el directorio Carpetadelsistema en la ruta de acceso de la clave de un componente. Dado que esta carpeta se encuentra en cada sistema operativo, el instalador detecta siempre la ruta de acceso de la clave tanto si el componente está presente como si no. En este caso, la ruta de acceso de la clave debe ser un archivo, una entrada del registro o un origen de datos ODBC.

Al realizar una validación, ICE18 comprueba en primer lugar si se cumplen todas las condiciones siguientes:

-   La columna de ruta de rutas de la [tabla de componentes](component-table.md) contiene un valor null.
-   Que no hay ningún archivo en la lista para el componente en la [tabla de archivos](file-table.md).
-   Que no hay archivos para el componente enumerado en la [tabla RemoveFile](removefile-table.md) y que el valor de DirProperty es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).
-   Que no hay archivos para el componente enumerado en la [tabla DuplicateFile](duplicatefile-table.md) y que el valor de DestFolder es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).
-   Que no hay archivos para el componente enumerado en la [tabla MoveFile](movefile-table.md) y que el valor de DestFolder es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).

Si se cumplen todas las condiciones, ICE18 valida lo siguiente:

-   Que la \_ columna componente de la [tabla CreateFolder](createfolder-table.md) tenga el mismo valor que la columna componente de la [tabla componente](component-table.md).
-   Que la \_ columna directorio de la tabla CreateFolder tenga el mismo valor que la \_ columna directorio de la [tabla componente](component-table.md).

## <a name="result"></a>Resultado

ICE18 envía un mensaje de error si el paquete de instalación especifica un directorio como la ruta de acceso de la clave del componente que no aparece en la [tabla CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



