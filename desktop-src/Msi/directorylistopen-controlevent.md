---
description: Este evento selecciona y resalta un directorio en el control DirectoryList que el usuario ha elegido abrir. Para obtener información relacionada, vea Examinar cuadro de diálogo.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947329"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

Este evento selecciona y resalta un directorio en el [control DirectoryList](directorylist-control.md) que el usuario ha elegido abrir. Para obtener información relacionada, vea [Examinar cuadro de diálogo](browse-dialog.md).

Este evento debe publicarse mediante un [control PushButton ubicado](pushbutton-control.md) en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario niveles](user-interface-levels.md).

Si no se ha seleccionado ningún directorio en el [control DirectoryList](directorylist-control.md), un evento DirectoryListOpen deshabilita cualquier otro control que publique un evento DirectoryListOpen.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) en el mismo cuadro de diálogo modal que DirectoryList se usa para desencadenar la ejecución paso a paso por pasos en la ruta de acceso.

 

 



