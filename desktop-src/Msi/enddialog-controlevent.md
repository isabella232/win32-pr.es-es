---
description: Este evento notifica al instalador que quite un cuadro de diálogo modal. En todos los casos, el instalador quita el cuadro de diálogo presente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277180"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent,

Este evento notifica al instalador que quite un cuadro de diálogo modal. En todos los casos, el instalador quita el cuadro de diálogo presente.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

En la tabla siguiente se muestra la acción del evento resultante de los distintos argumentos especificados en la [tabla ControlEvent,](controlevent-table.md).



| Argumento | Acción del instalador                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Salir     | La secuencia del asistente está cerrada y el control vuelve al instalador con el valor UserExit. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo. |
| Volver a intentar    | La secuencia del asistente está cerrada y el control vuelve al instalador con el valor Suspend. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo.  |
| Ignorar   | La secuencia del asistente está cerrada y el control vuelve al instalador con el valor terminado. Este argumento no se puede usar en un cuadro de diálogo que sea un elemento secundario de otro cuadro de diálogo. |
| Valor devuelto   | El control vuelve al elemento primario del cuadro de diálogo actual, o si no hay ningún elemento primario, el control vuelve al instalador con el valor Success.                                 |



 

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

En los cuadros de diálogo normales, la columna argument de la [tabla ControlEvent,](controlevent-table.md) puede ser "Return", "Exit", "Retry" u "ignore".

En los cuadros de diálogo de error, la columna argument de la [tabla ControlEvent,](controlevent-table.md) puede ser ' ErrorOk ', ' ErrorCancel ', ' ErrorAbort ', ' ErrorRetry ', ' ErrorIgnore ', ' ErrorYes ' o ' ErrorNo '.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para cerrar un cuadro de diálogo.

 

 



