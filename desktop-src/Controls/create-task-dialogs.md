---
title: Cómo crear cuadros de diálogo de tareas
description: Se crea un cuadro de diálogo de tarea y se muestra mediante la función TaskDialog o la función TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6f74f1922330cae1550fda1a9ad6d451221452017f3856ae5e859948019828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504025"
---
# <a name="how-to-create-task-dialogs"></a>Cómo crear cuadros de diálogo de tareas

Se crea un cuadro de diálogo de tarea y se muestra mediante la [**función TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o [**la función TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="taskdialog"></a>TaskDialog

La **función TaskDialog** es adecuada para cuadros de diálogo simples que presentan información textual y solicitan una opción estándar. Esta función de creación no admite barras de progreso, casillas, pies de página, botones de expandir o contraer, botones personalizados ni botones de radio.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La **función TaskDialogIndirect** es más eficaz, admite todos los elementos de interfaz disponibles y también permite capturar eventos en un procedimiento de devolución de llamada para que la aplicación pueda actualizar una barra de progreso o responder a un clic de un hipervínculo o botón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar cuadros de diálogo de tareas](using-task-dialogs.md)
</dt> </dl>

 

 




