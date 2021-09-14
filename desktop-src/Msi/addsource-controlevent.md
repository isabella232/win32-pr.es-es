---
description: Este evento notifica al instalador, mientras se mantiene en ejecución el diálogo actual, que una característica o todas las características se van a ejecutar desde el origen.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159188"
---
# <a name="addsource-controlevent"></a>AddSource ControlEvent

Este evento notifica al instalador, mientras se mantiene en ejecución el diálogo actual, que una característica o todas las características se van a ejecutar desde el origen. Este evento se puede publicar mediante un [control PushButton](pushbutton-control.md), [un control Checkbox](checkbox-control.md)o un control [SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena, ya sea el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento y se usa para notificar al instalador sin detener el cuadro de diálogo.

 

 



