---
description: Este control ControlEvent se puede usar para activar o desactivar las funcionalidades de reversión del instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143116"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent

Este control ControlEvent se puede usar para activar o desactivar las funcionalidades de reversión del instalador.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

False desactiva las funcionalidades de reversión del instalador. True activa las funcionalidades de reversión del instalador.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Se puede usar para desactivar las funcionalidades de reversión si el instalador detecta que no hay suficiente espacio en disco disponible para completar la instalación. En este caso, el control ControlEvent debe usarse con las propiedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)y [**PROMPTROLLBACKCOST.**](promptrollbackcost.md)

 

 



