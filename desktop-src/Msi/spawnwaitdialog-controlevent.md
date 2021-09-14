---
description: SpawnWaitDialog ControlEvent desencadena el cuadro de diálogo especificado por la columna Argument de la tabla ControlEvent, si la expresión de la columna Condition se evalúa como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266044"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent

SpawnWaitDialog ControlEvent desencadena el cuadro de diálogo especificado por la columna Argument de la [tabla ControlEvent](controlevent-table.md), si la expresión de la columna Condition se evalúa como FALSE. El cuadro de diálogo permanece mientras la expresión condicional permanezca en FALSE y se quite en cuanto la condición se evalúe como TRUE.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cuadro de diálogo de la [tabla Dialog](dialog-table.md).

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

SpawnWaitDialog ControlEvent se puede usar para esperar a cualquier tarea en segundo plano cuya finalización se pueda probar mediante una expresión condicional como el estado de una propiedad. Para obtener un ejemplo del uso de SpawnWaitDialog ControlEvent, vea la sección Creación de un elemento [condicional "Espere . . ." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).

 

 



