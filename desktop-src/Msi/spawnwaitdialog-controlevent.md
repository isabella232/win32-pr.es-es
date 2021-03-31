---
description: SpawnWaitDialog ControlEvent, desencadena el cuadro de diálogo especificado por la columna argument de la tabla ControlEvent,, si la expresión de la columna condition se evalúa como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001248"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent,

SpawnWaitDialog ControlEvent, desencadena el cuadro de diálogo especificado por la columna argument de la [tabla ControlEvent,](controlevent-table.md), si la expresión de la columna condition se evalúa como false. El cuadro de diálogo permanece activo mientras la expresión condicional sigue siendo falsa y se quita en cuanto la condición se evalúa como TRUE.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Cuadro de diálogo en la [tabla del cuadro de diálogo](dialog-table.md).

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

SpawnWaitDialog ControlEvent, se puede usar para esperar a cualquier tarea en segundo plano la finalización de la que se puede probar mediante una expresión condicional como el estado de una propiedad. Para obtener un ejemplo del uso de SpawnWaitDialog ControlEvent,, consulte la sección [creación de una instrucción condicional "Wait..." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).

 

 



