---
description: SpawnWaitDialog ControlEvent desencadena el cuadro de diálogo especificado por la columna Argument de la tabla ControlEvent, si la expresión de la columna Condition se evalúa como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffeddfcb46f67d292de81a5a8195ba17c2a63b305be229ae96b2133448d41f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628015"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent

SpawnWaitDialog ControlEvent desencadena el cuadro de diálogo especificado por la columna Argument de la [tabla ControlEvent](controlevent-table.md), si la expresión de la columna Condition se evalúa como FALSE. El cuadro de diálogo permanece mientras la expresión condicional permanezca en FALSE y se quite en cuanto la condición se evalúe como TRUE.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario niveles](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cuadro de diálogo de la [tabla Dialog](dialog-table.md).

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

SpawnWaitDialog ControlEvent se puede usar para esperar a cualquier tarea en segundo plano cuya finalización se pueda probar mediante una expresión condicional como el estado de una propiedad. Para obtener un ejemplo del uso de SpawnWaitDialog ControlEvent, vea la sección Creación de un elemento [condicional "Espere . . ." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).

 

 



