---
description: Este evento notifica al instalador que haga la transición de un cuadro de diálogo modal a otro cuadro de diálogo. El instalador quita el cuadro de diálogo actual y crea el nuevo con el nombre indicado en el argumento .
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261020"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent

Este evento notifica al instalador que haga la transición de un cuadro de diálogo modal a otro cuadro de diálogo. El instalador quita el cuadro de diálogo actual y crea el nuevo con el nombre indicado en el argumento .

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena que es el nombre del nuevo cuadro de diálogo.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para indicar una transición al cuadro de diálogo siguiente o anterior de la misma secuencia del asistente.

 

 



