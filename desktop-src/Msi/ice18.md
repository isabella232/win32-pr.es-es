---
description: ICE18 valida que los directorios vacíos que se usan como ruta de acceso de clave para un componente se muestran en la tabla CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca102e8fdec5e30283cd879ddb5677a2bba79f90ba5a9a790ea50923e0aeedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581145"
---
# <a name="ice18"></a>ICE18

ICE18 valida que los directorios vacíos que se usan como ruta de acceso de clave para un componente se muestran en la [tabla CreateFolder](createfolder-table.md).

Si la columna KeyPath de la tabla [Component](component-table.md) es Null, significa que el directorio que aparece en la columna Directory es la ruta de \_ acceso de clave para ese componente. Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, esta carpeta debe aparecer en la [tabla CreateFolder](createfolder-table.md) para evitar que el instalador intente instalarse cada vez.

No haga que el directorio SystemFolder sea la ruta de acceso de clave de un componente. Dado que esta carpeta está presente en todos los sistemas operativos, el instalador siempre detecta la ruta de acceso de la clave tanto si el componente está presente como si no. En este caso, la ruta de acceso de la clave debe ser un archivo, una entrada del Registro o un origen de datos ODBC.

Al realizar una validación ICE18, comprueba primero si lo siguiente es cierto:

-   La columna KeyPath de la [tabla Component](component-table.md) contiene un valor NULL.
-   Que no hay archivos enumerados para el componente en la [tabla File](file-table.md).
-   Que no hay ningún archivo para el componente enumerado en la tabla [RemoveFile](removefile-table.md) y que el valor de DirProperty es el mismo que la columna Directory de \_ la tabla [Component](component-table.md).
-   Que no hay archivos para el componente enumerado en la tabla [DuplicateFile](duplicatefile-table.md) y que el valor de DestFolder es el mismo que la columna Directory de la \_ tabla [Component](component-table.md).
-   Que no hay ningún archivo para el componente enumerado en la tabla [MoveFile](movefile-table.md) y que el valor de DestFolder es el mismo que la columna Directory de la \_ tabla [Component](component-table.md).

Si todas son verdaderas, ICE18 valida lo siguiente:

-   Que la columna \_ Component de la tabla [CreateFolder](createfolder-table.md) tiene el mismo valor que la columna Component de la [tabla Component](component-table.md).
-   Que la columna \_ Directory de la tabla CreateFolder tiene el mismo valor que la columna Directory de la tabla \_ [Component](component-table.md).

## <a name="result"></a>Resultado

ICE18 envía un mensaje de error si el paquete de instalación especifica un directorio como ruta de acceso de clave para el componente que no aparece en la [tabla CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



