---
title: Cómo crear cuadros de diálogo de tareas
description: Se crea un cuadro de diálogo de tarea y se muestra mediante la función TaskDialog o la función TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075296"
---
# <a name="how-to-create-task-dialogs"></a>Cómo crear cuadros de diálogo de tareas

Se crea un cuadro de diálogo de tarea y se muestra mediante la función [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="taskdialog"></a>TaskDialog

La función **TaskDialog** es adecuada para los cuadros de diálogo sencillos que presentan información textual y solicitan una opción estándar. Esta función de creación no admite barras de progreso, casillas, pies de página, botones de expansión/contracción, botones personalizados o botones de radio.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La función **TaskDialogIndirect** es más eficaz, admite todos los elementos de interfaz disponibles y también permite capturar eventos en un procedimiento de devolución de llamada para que la aplicación pueda actualizar una barra de progreso o responder a un clic de un hipervínculo o un botón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar cuadros de diálogo de tareas](using-task-dialogs.md)
</dt> </dl>

 

 




