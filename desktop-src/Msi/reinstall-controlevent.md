---
description: Permite al autor iniciar una reinstalación de algunas o todas las características, mientras se ejecuta el cuadro de diálogo actual.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstalar ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069675"
---
# <a name="reinstall-controlevent"></a>Reinstalar ControlEvent

El control ReinstalarEvental permite al autor iniciar una reinstalación de algunas o todas las características, mientras se ejecuta el cuadro de diálogo actual.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md) [un control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funciona con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena que es el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Este evento está vinculado a un control [PushButton](pushbutton-control.md) en un cuadro de diálogo modal. El mismo control [PushButton](pushbutton-control.md) también debe estar asociado a [un control ReinstallMode](reinstallmode-controlevent.md) ControlEvent.

 

 



