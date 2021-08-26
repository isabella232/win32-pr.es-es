---
description: Este evento notifica al control DirectoryList que el usuario desea seleccionar el elemento primario del directorio actual. Para obtener información relacionada, vea Examinar cuadro de diálogo.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99fb0731a06f30cf788e3565e0988bf5b20ebce7abec8be351f4d1fe9d2aab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086185"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent

Este evento notifica al [control DirectoryList que](directorylist-control.md) el usuario desea seleccionar el elemento primario del directorio actual. Para obtener información relacionada, vea [Examinar cuadro de diálogo](browse-dialog.md).

Este evento debe publicarse mediante un [control PushButton ubicado](pushbutton-control.md) en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Si el directorio actual es el directorio raíz de la unidad, un evento DirectoryListUp deshabilita cualquier otro control que publique un evento DirectoryListUp.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) en el mismo cuadro de diálogo modal que DirectoryList se usa para desencadenar el paso a paso por la ruta de acceso.

 

 



