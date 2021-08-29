---
description: 'La sintaxis del evento SetProperty es diferente de la de otros controlEvents En lugar del nombre del evento, se coloca la propiedad entre corchetes: nombre \[ de \_ propiedad \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850048ab550ea091fcd714835546305b81cdd001efd15e1f55f46f924b3a0308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628615"
---
# <a name="setproperty-controlevent"></a>SetProperty ControlEvent

La sintaxis del evento SetProperty es diferente de la de otros controlEvents En lugar del nombre del evento, se coloca la propiedad entre corchetes: nombre \[ de \_ propiedad \] . El argumento es el nuevo valor de la propiedad . Para deshacer la propiedad , el argumento debe ser {} . Esto es necesario, porque el argumento es una clave principal de la tabla y, por tanto, no puede ser NULL. El argumento se formateará mediante el método FormatText, por lo que el argumento puede contener cualquier expresión que el método FormatText pueda controlar. Los valores de propiedad se evalúan en el momento del controlEvent.

Este evento se puede publicar mediante un [control PushButton](pushbutton-control.md), [un control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario niveles](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Nuevo valor de la propiedad. {} para null.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Control [PushButton](pushbutton-control.md) en un cuadro de diálogo vinculado a este evento para que cambie una propiedad cuando se inserta el botón.

 

 



