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
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="7e969-103">Cómo crear cuadros de diálogo de tareas</span><span class="sxs-lookup"><span data-stu-id="7e969-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="7e969-104">Se crea un cuadro de diálogo de tarea y se muestra mediante la función [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="7e969-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7e969-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="7e969-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7e969-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="7e969-106">Technologies</span></span>

-   [<span data-ttu-id="7e969-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="7e969-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7e969-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7e969-108">Prerequisites</span></span>

-   <span data-ttu-id="7e969-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e969-109">C/C++</span></span>
-   <span data-ttu-id="7e969-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="7e969-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7e969-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7e969-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="7e969-112">TaskDialog</span><span class="sxs-lookup"><span data-stu-id="7e969-112">TaskDialog</span></span>

<span data-ttu-id="7e969-113">La función **TaskDialog** es adecuada para los cuadros de diálogo sencillos que presentan información textual y solicitan una opción estándar.</span><span class="sxs-lookup"><span data-stu-id="7e969-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="7e969-114">Esta función de creación no admite barras de progreso, casillas, pies de página, botones de expansión/contracción, botones personalizados o botones de radio.</span><span class="sxs-lookup"><span data-stu-id="7e969-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="7e969-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="7e969-115">TaskDialogIndirect</span></span>

<span data-ttu-id="7e969-116">La función **TaskDialogIndirect** es más eficaz, admite todos los elementos de interfaz disponibles y también permite capturar eventos en un procedimiento de devolución de llamada para que la aplicación pueda actualizar una barra de progreso o responder a un clic de un hipervínculo o un botón.</span><span class="sxs-lookup"><span data-stu-id="7e969-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e969-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e969-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e969-118">Usar cuadros de diálogo de tareas</span><span class="sxs-lookup"><span data-stu-id="7e969-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 




