---
description: Este evento notifica al instalador que tiene que comprobar que la ruta de acceso seleccionada es válida. Si la ruta de acceso no es válida, este evento bloquea más controlEvents asociados al control.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8ae179a3d6e0debba4cecfd620bc0cebf99361875517d944886b82ff4d55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066065"
---
# <a name="checktargetpath-controlevent"></a>CheckTargetPath ControlEvent

Este evento notifica al instalador que tiene que comprobar que la ruta de acceso seleccionada es válida. Si la ruta de acceso no es válida, este evento bloquea más controlEvents asociados al control.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Nombre de la propiedad que contiene la ruta de acceso. Si la propiedad es indirecta, el nombre de la propiedad se incluye entre corchetes.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) de un cuadro de diálogo Examinar está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.

 

 



