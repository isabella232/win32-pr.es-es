---
description: Este evento notifica al control DirectoryList que se debe crear una nueva carpeta. crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378905"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent

Este evento notifica al [control DirectoryList](directorylist-control.md) que se debe crear una nueva carpeta. crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición. El nombre predeterminado de la nueva carpeta se puede crear en la [tabla UIText](uitext-table.md). Escriba "NewFolder" en la columna Clave. Escriba el valor del nombre predeterminado de la nueva carpeta en la columna Texto. Este valor debe tener el formato de un tipo de datos de columna [Filename](filename.md) y usar la sintaxis \| LFN de SFN. Si este valor no está presente en la tabla UIText o es un valor no válido, el instalador usa un valor predeterminado de "Fldr \| New Folder". Para obtener información relacionada, vea [Examinar cuadro de diálogo](browse-dialog.md).

Este evento debe publicarse mediante un [control PushButton ubicado](pushbutton-control.md) en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario niveles](user-interface-levels.md).

Tenga en cuenta que si se vuelve a llamar a este control ControlEvent cuando ya existe una nueva carpeta, no se creará una segunda carpeta. En este caso, al llamar a DirectoryListNew, se selecciona el nombre de la nueva carpeta existente para su edición.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) en el mismo cuadro de diálogo modal que DirectoryList se usa para desencadenar la creación de una nueva carpeta.

 

 



