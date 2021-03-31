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
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="e1968-103">Cómo obtener datos proporcionados por el usuario desde un cuadro de diálogo de tarea</span><span class="sxs-lookup"><span data-stu-id="e1968-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="e1968-104">Para completar una tarea, los usuarios envían los detalles de la tarea a la aplicación configurando los controles en el cuadro de diálogo de tarea y haciendo clic en un botón de comando (normalmente **correcto**).</span><span class="sxs-lookup"><span data-stu-id="e1968-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e1968-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="e1968-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e1968-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="e1968-106">Technologies</span></span>

-   [<span data-ttu-id="e1968-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="e1968-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e1968-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e1968-108">Prerequisites</span></span>

-   <span data-ttu-id="e1968-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e1968-109">C/C++</span></span>
-   <span data-ttu-id="e1968-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="e1968-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e1968-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e1968-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="e1968-112">Obtener datos proporcionados por el usuario desde un cuadro de diálogo de tarea</span><span class="sxs-lookup"><span data-stu-id="e1968-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="e1968-113">Puede identificar el botón en el que se hizo clic examinando el parámetro *pnButton* de la función de llamada.</span><span class="sxs-lookup"><span data-stu-id="e1968-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="e1968-114">También puede identificar el botón de radio seleccionado en el parámetro *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)y el estado de la casilla de verificación del parámetro *pfVerificationFlagChecked* .</span><span class="sxs-lookup"><span data-stu-id="e1968-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="e1968-115">Los clics en los botones e hipervínculos se reciben mediante la función [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) en forma [de \_ TDN \_ clic en el botón de](tdn-button-clicked.md) y TDN hipervínculo [ \_ \_ en](tdn-hyperlink-clicked.md) las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e1968-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="e1968-116">Si la función de devolución de llamada devuelve S \_ OK después de controlar una notificación de botón, el cuadro de diálogo de tarea se cierra y el identificador de comando del botón se devuelve en *pnButton*.</span><span class="sxs-lookup"><span data-stu-id="e1968-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="e1968-117">Si devuelve S \_ false o no tiene una función de devolución de llamada, el cuadro de diálogo de tarea permanece abierto.</span><span class="sxs-lookup"><span data-stu-id="e1968-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1968-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1968-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1968-119">Usar cuadros de diálogo de tareas</span><span class="sxs-lookup"><span data-stu-id="e1968-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 