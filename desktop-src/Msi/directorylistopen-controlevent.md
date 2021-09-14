---
description: Este evento selecciona y resalta un directorio en el control DirectoryList que el usuario ha elegido abrir. Para obtener información relacionada, vea Cuadro de diálogo Examinar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158561"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

Este evento selecciona y resalta un directorio en el [control DirectoryList](directorylist-control.md) que el usuario ha elegido abrir. Para obtener información relacionada, vea [Cuadro de diálogo Examinar](browse-dialog.md).

Este evento debe publicarse mediante un [control PushButton](pushbutton-control.md) ubicado en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Si no se ha seleccionado ningún directorio en el [control DirectoryList](directorylist-control.md), un evento DirectoryListOpen deshabilita cualquier otro control que publique un evento DirectoryListOpen.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa un argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) en el mismo cuadro de diálogo modal que DirectoryList se usa para desencadenar la ejecución paso a paso por la ruta de acceso.

 

 



