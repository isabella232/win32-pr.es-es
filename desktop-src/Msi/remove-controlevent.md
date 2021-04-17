---
description: El instalador recibe una notificación a través de este evento cuando se selecciona una característica o todas las características para su eliminación mientras se mantiene el cuadro de diálogo presente en ejecución.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Quitar ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667471"
---
# <a name="remove-controlevent"></a>Quitar ControlEvent,

El instalador recibe una notificación a través de este evento cuando se selecciona una característica o todas las características para su eliminación mientras se mantiene el cuadro de diálogo presente en ejecución.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Cadena que es el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="action-by-publisher-when-subscriber-activated"></a>Acción por publicador cuando el suscriptor está activado

El instalador mantiene el cuadro de diálogo presente en ejecución y lo notifica al instalador.

## <a name="typical-use"></a>Uso típico

Control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal asociado a este evento.

 

 



