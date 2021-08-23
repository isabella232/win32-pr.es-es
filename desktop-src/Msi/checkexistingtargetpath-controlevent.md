---
description: Este evento notifica al instalador que tiene que comprobar que se puede escribir en la ruta de acceso seleccionada. Si no se puede escribir la ruta de acceso, el evento bloquea más controlEvents asociados al control.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d523d04eba4ede88ca1382c17c5d40d48dadadbc9520d766b5cfca2b26b77fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520195"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent

Este evento notifica al instalador que tiene que comprobar que se puede escribir en la ruta de acceso seleccionada. Si no se puede escribir la ruta de acceso, el evento bloquea más controlEvents asociados al control.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Nombre de la propiedad que contiene la ruta de acceso. Si la propiedad es indirecta, el nombre de la propiedad se incluye entre corchetes.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) de un cuadro de diálogo examinar está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.

 

 



