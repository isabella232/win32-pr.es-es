---
description: El instalador se notifica a través de este evento cuando se selecciona una característica o todas las características para su eliminación mientras se mantiene en ejecución el cuadro de diálogo actual.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Quitar ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260991"
---
# <a name="remove-controlevent"></a>Quitar ControlEvent

El instalador se notifica a través de este evento cuando se selecciona una característica o todas las características para su eliminación mientras se mantiene en ejecución el cuadro de diálogo actual.

Este evento se puede publicar mediante un [control PushButton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena que es el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="action-by-publisher-when-subscriber-activated"></a>Acción de Publisher cuando se activa el suscriptor

El instalador mantiene el cuadro de diálogo actual en ejecución y notifica al instalador.

## <a name="typical-use"></a>Uso típico

Control [PushButton](pushbutton-control.md) en un cuadro de diálogo modal asociado a este evento.

 

 



