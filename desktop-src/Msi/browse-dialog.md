---
description: Un cuadro de diálogo Examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear mediante este control.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Cuadro de diálogo Examinar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158961"
---
# <a name="browse-dialog"></a>Cuadro de diálogo Examinar

Un cuadro de diálogo Examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear mediante este control.

Este tipo de cuadro de diálogo normalmente contiene los tres controles siguientes. Estos controles están conectados a la misma propiedad. Esa propiedad es la ruta de acceso que se está seleccionando.

-   Un [control PathEdit](pathedit-control.md) para seleccionar la sección final de la ruta de acceso. Este control no puede perder el foco si la cola especificada no es válida en el volumen actual.
-   Un [control DirectoryCombo](directorycombo-control.md) para mostrar la ruta de acceso seleccionada actualmente que muestra el control PathEdit. Este control no muestra el último segmento de la ruta de acceso.
-   Control [DirectoryList para](directorylist-control.md) mostrar las carpetas debajo del directorio mostrado actualmente por DirectoryCombo. Esto también puede mostrar una carpeta que aún no se ha creado.

Un cuadro de diálogo Examinar normalmente también contiene un [control DirectoryCombo](directorycombo-control.md) que especifica los tipos de volumen que se mostrarán. Es habitual que todos los tipos de volumen se muestren en un cuadro de diálogo Examinar.

Los cuadros de diálogo Examinar normalmente contienen tres [controles PushButton](pushbutton-control.md). Estos botones están vinculados a sus respectivos eventos ControlEvent en [la tabla ControlEvent](controlevent-table.md). Estos botones se usan para activar las siguientes opciones de control.



| Opción de control | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Subir un nivel   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nueva carpeta     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Abrir           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Para que la opción Nueva carpeta funcione con un nombre de carpeta no predeterminado, la ruta de acceso de la nueva carpeta debe especificarse en la [tabla UIText](uitext-table.md). La cadena de ruta de acceso debe usar el formulario "nombre de archivo corto nombre de archivo \| largo" para el nombre de archivo. Por ejemplo, use un nombre de archivo como "MyProd~1 \| Mi producto desaprobado". Consulte el tipo [de datos de](filename.md) columna Nombre de archivo para obtener más información sobre el formato de nombre de archivo. Si la ruta de acceso no está presente en la tabla UIText o si se establece en un valor no válido, se establece en un valor de "Fldr New Folder" de \| forma predeterminada. El **botón Nueva** carpeta se puede omitir si el cuadro de diálogo solo necesita buscar carpetas existentes.

 

 



