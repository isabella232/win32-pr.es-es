---
description: SpawnDialog ControlEvent notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras se mantiene en ejecución el cuadro de diálogo actual.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b0dd281e4306fab7c62d218781c2ad932b82f22b335d662181fb65891eeb5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628035"
---
# <a name="spawndialog-controlevent"></a>SpawnDialog ControlEvent

SpawnDialog ControlEvent notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras se mantiene en ejecución el cuadro de diálogo actual.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena que es el nombre del nuevo cuadro de diálogo.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para crear un diálogo secundario, como "¿Está seguro de que desea cancelar?" .

 

 



