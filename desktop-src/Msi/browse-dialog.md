---
description: Un cuadro de diálogo Examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear mediante este control.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Cuadro de diálogo Examinar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7caceb8e10bc99a9edd8fa5b828efa2e5cbc8b4ed7164d40e2235e19c098199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380727"
---
# <a name="browse-dialog"></a>Cuadro de diálogo Examinar

Un cuadro de diálogo Examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear mediante este control.

Este tipo de cuadro de diálogo normalmente contiene los tres controles siguientes. Estos controles están conectados a la misma propiedad. Esa propiedad es la ruta de acceso que se está seleccionando.

-   Un [control PathEdit para](pathedit-control.md) seleccionar la sección final de la ruta de acceso. Este control no puede perder el foco si la cola especificada no es válida en el volumen actual.
-   Un [control DirectoryCombo](directorycombo-control.md) para mostrar la ruta de acceso seleccionada actualmente que muestra el control PathEdit. Este control no muestra el último segmento de la ruta de acceso.
-   Un [control DirectoryList](directorylist-control.md) para mostrar las carpetas debajo del directorio mostrado actualmente por DirectoryCombo. Esto también puede mostrar una carpeta que aún no se ha creado.

Normalmente, un cuadro de diálogo Examinar también contiene un [control DirectoryCombo](directorycombo-control.md) que especifica los tipos de volumen que se mostrarán. Es habitual que todos los tipos de volumen se muestren en un cuadro de diálogo Examinar.

Los cuadros de diálogo Examinar normalmente contienen tres [controles PushButton](pushbutton-control.md). Estos botones están vinculados a sus respectivos eventos ControlEvent en [la tabla ControlEvent](controlevent-table.md). Estos botones se usan para activar las siguientes opciones de control.



| Opción de control | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Subir un nivel   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nueva carpeta     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Abrir           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Para que la opción Nueva carpeta funcione con un nombre de carpeta no predeterminado, la ruta de acceso de la nueva carpeta debe especificarse en la [tabla UIText](uitext-table.md). La cadena de ruta de acceso debe usar el formulario "nombre de archivo corto nombre de archivo \| largo" para el nombre de archivo. Por ejemplo, use un nombre de archivo como "MyProd~1 \| Mi producto desaprobado". Consulte el [tipo de](filename.md) datos de columna Filename para obtener más información sobre el formato de nombre de archivo. Si la ruta de acceso no está presente en la tabla UIText o si se establece en un valor no válido, se establece en un valor de "Nueva carpeta de Fldr" de \| forma predeterminada. El **botón Nueva** carpeta se puede omitir si el cuadro de diálogo solo necesita buscar carpetas existentes.

 

 



