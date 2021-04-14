---
description: Un cuadro de diálogo examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear con este control.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Cuadro de diálogo examinar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423876"
---
# <a name="browse-dialog"></a>Cuadro de diálogo examinar

Un cuadro de diálogo examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear con este control.

Este tipo de cuadro de diálogo contiene normalmente los tres controles siguientes. Estos controles se conectan a la misma propiedad. Esa propiedad es la ruta de acceso que se selecciona.

-   Un [control PathEdit](pathedit-control.md) para seleccionar la sección tail del trazado. Este control no puede perder el foco si la cola introducida no es válida en el volumen actual.
-   Un [control DirectoryCombo](directorycombo-control.md) para mostrar la ruta de acceso seleccionada actualmente que muestra el control PathEdit. Este control no muestra el último segmento de la ruta de acceso.
-   Un [control DirectoryList](directorylist-control.md) para mostrar las carpetas debajo del directorio mostrado actualmente por el DirectoryCombo. Esto también puede mostrar una carpeta que aún no se ha creado.

Un cuadro de diálogo de exploración también contiene normalmente un [control DirectoryCombo](directorycombo-control.md) que especifica los tipos de volúmenes que se van a mostrar. Es habitual que todos los tipos de volúmenes se muestren en un cuadro de diálogo de exploración.

Los cuadros de diálogo de exploración suelen contener tres [controles de pulsador](pushbutton-control.md). Estos botones están vinculados a sus respectivas ControlEvents en la [tabla ControlEvent,](controlevent-table.md). Estos botones se utilizan para activar las siguientes opciones de control.



| Opción de control | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Subir un nivel   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nueva carpeta     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Abrir           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Para que la opción nueva carpeta funcione con un nombre de carpeta no predeterminado, se debe especificar la ruta de acceso de la nueva carpeta en la [tabla UIText](uitext-table.md). La cadena de ruta de acceso debe usar el \| formato de nombre de archivo largo de nombre corto de archivo para el nombre de archivo. Por ejemplo, use un nombre de archivo como "mi Prod ~ 1 \| My aventuras Product". Vea el tipo de datos de la columna [filename](filename.md) para obtener más información sobre el formato de nombre de archivo. Si la ruta de acceso no está presente en la tabla UIText, o si está establecida en un valor no válido, se establece en un valor de "FLDR \| nueva carpeta" de forma predeterminada. Se puede omitir el botón **nueva carpeta** si el cuadro de diálogo solo necesita buscar carpetas existentes.

 

 



