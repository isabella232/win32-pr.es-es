---
description: Este evento notifica al instalador que quite un cuadro de diálogo modal. En todos los casos, el instalador quita el cuadro de diálogo actual.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158484"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent

Este evento notifica al instalador que quite un cuadro de diálogo modal. En todos los casos, el instalador quita el cuadro de diálogo actual.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

En la tabla siguiente se muestra la acción del evento resultante de distintos argumentos especificados en la [tabla ControlEvent](controlevent-table.md).



| Argumento | Acción del instalador                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Salir     | La secuencia del asistente se cierra y el control vuelve al instalador con el valor UserExit. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo. |
| Volver a intentar    | La secuencia del asistente se cierra y el control vuelve al instalador con el valor Suspender. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo.  |
| Ignorar   | La secuencia del asistente se cierra y el control vuelve al instalador con el valor Finalizado. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo. |
| Valor devuelto   | El control vuelve al elemento primario del cuadro de diálogo actual o, si no hay ningún elemento primario, el control vuelve al instalador con el valor Correcto.                                 |



 

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

En los cuadros de diálogo normales, la columna Argument de la [tabla ControlEvent](controlevent-table.md) puede ser "Return", "Exit", "Retry" o "Ignore".

En los cuadros de diálogo de error, la columna Argument de la [tabla ControlEvent](controlevent-table.md) puede ser "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" o "ErrorNo".

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para cerrar un cuadro de diálogo.

 

 



