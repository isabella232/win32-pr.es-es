---
title: Cómo obtener datos proporcionados por el usuario desde un cuadro de diálogo de tarea
description: Para completar una tarea, los usuarios envían los detalles de la tarea a la aplicación configurando los controles en el cuadro de diálogo de tarea y haciendo clic en un botón de comando (normalmente correcto).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995683"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Cómo obtener datos proporcionados por el usuario desde un cuadro de diálogo de tarea

Para completar una tarea, los usuarios envían los detalles de la tarea a la aplicación configurando los controles en el cuadro de diálogo de tarea y haciendo clic en un botón de comando (normalmente **correcto**).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="getting-user-input-from-a-task-dialog"></a>Obtener datos proporcionados por el usuario desde un cuadro de diálogo de tarea

Puede identificar el botón en el que se hizo clic examinando el parámetro *pnButton* de la función de llamada. También puede identificar el botón de radio seleccionado en el parámetro *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)y el estado de la casilla de verificación del parámetro *pfVerificationFlagChecked* .

Los clics en los botones e hipervínculos se reciben mediante la función [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) en forma [de \_ TDN \_ clic en el botón de](tdn-button-clicked.md) y TDN hipervínculo [ \_ \_ en](tdn-hyperlink-clicked.md) las notificaciones. Si la función de devolución de llamada devuelve S \_ OK después de controlar una notificación de botón, el cuadro de diálogo de tarea se cierra y el identificador de comando del botón se devuelve en *pnButton*. Si devuelve S \_ false o no tiene una función de devolución de llamada, el cuadro de diálogo de tarea permanece abierto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar cuadros de diálogo de tareas](using-task-dialogs.md)
</dt> </dl>

 

 