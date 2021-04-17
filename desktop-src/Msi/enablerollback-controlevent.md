---
description: Este ControlEvent, se puede usar para activar o desactivar las funcionalidades de reversión del instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652530"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent,

Este ControlEvent, se puede usar para activar o desactivar las funcionalidades de reversión del instalador.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

False desactiva las funciones de reversión del instalador. True activa las capacidades de reversión del instalador.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Se puede usar para desactivar las capacidades de reversión Si el instalador detecta que no hay suficiente espacio en disco disponible para completar la instalación. En este caso, se debe usar ControlEvent, con las propiedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .

 

 



