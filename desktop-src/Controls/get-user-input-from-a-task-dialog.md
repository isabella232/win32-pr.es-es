---
title: Cómo obtener la entrada del usuario desde un cuadro de diálogo de tarea
description: Para completar una tarea, los usuarios envían los detalles de la tarea a la aplicación configurando los controles en el cuadro de diálogo de tarea y, a continuación, haciendo clic en un botón de comando (normalmente Aceptar).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d034c434f5bd2fe5e3c2230765b21116c1eeb47a8ef4a057480a0f9e9d4c0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436414"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Cómo obtener la entrada del usuario desde un cuadro de diálogo de tarea

Para completar una tarea, los usuarios envían los detalles de la tarea a la aplicación configurando los controles en el cuadro de diálogo de tarea y, a continuación, haciendo clic en un botón de comando (normalmente **Aceptar).**

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="getting-user-input-from-a-task-dialog"></a>Obtener la entrada del usuario de un cuadro de diálogo de tarea

Puede identificar el botón en el que se hizo clic examinando el *parámetro pnButton* de la función que realiza la llamada. También puede identificar el botón de radio seleccionado del parámetro *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)y el estado de la casilla de verificación del *parámetro pfVerificationFlagChecked.*

La función [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) recibe los clics en botones e hipervínculos en forma de notificaciones [ \_ \_ CLICKED de TDN BUTTON](tdn-button-clicked.md) y [TDN \_ HYPERLINK \_ CLICKED.](tdn-hyperlink-clicked.md) Si la función de devolución de llamada devuelve S OK después de controlar una notificación de botón, el cuadro de diálogo de tarea se cierra y el identificador de comando del botón \_ se devuelve en *pnButton*. Si devuelve S FALSE o no tiene una función de devolución de llamada, el cuadro de \_ diálogo de tarea permanece abierto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar cuadros de diálogo de tareas](using-task-dialogs.md)
</dt> </dl>

 

 