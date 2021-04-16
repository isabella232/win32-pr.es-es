---
description: Un cuadro de diálogo de error es un cuadro de diálogo modal que muestra un mensaje de error. Puede haber más de un cuadro de diálogo de error en cada instalación.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543027"
---
# <a name="error-dialog"></a><span data-ttu-id="16e9e-104">Cuadro de diálogo de error</span><span class="sxs-lookup"><span data-stu-id="16e9e-104">Error Dialog</span></span>

<span data-ttu-id="16e9e-105">Un cuadro de diálogo de error es un cuadro de diálogo modal que muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="16e9e-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="16e9e-106">Puede haber más de un cuadro de diálogo de error en cada instalación.</span><span class="sxs-lookup"><span data-stu-id="16e9e-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="16e9e-107">Es necesario establecer una propiedad ErrorDialog que especifique qué cuadro de diálogo se va a usar.</span><span class="sxs-lookup"><span data-stu-id="16e9e-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="16e9e-108">Si esta propiedad no está establecida o no señala a un cuadro de diálogo de error válido, no se mostrarán los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="16e9e-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="16e9e-109">En este caso, el error solo se registra con una advertencia sobre el cuadro de diálogo que falta.</span><span class="sxs-lookup"><span data-stu-id="16e9e-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="16e9e-110">Un cuadro de diálogo de error debe tener establecido el [bit de estilo del cuadro de diálogo de error](error-dialog-style-bit.md) .</span><span class="sxs-lookup"><span data-stu-id="16e9e-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="16e9e-111">El cuadro de diálogo debe tener un [control de texto](text-control.md) denominado ErrorText.</span><span class="sxs-lookup"><span data-stu-id="16e9e-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="16e9e-112">El registro para el cuadro de diálogo de error de la [tabla de diálogo](dialog-table.md) debe tener el control ErrorText escrito en el \_ primer campo de control.</span><span class="sxs-lookup"><span data-stu-id="16e9e-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="16e9e-113">El cuadro de diálogo debe contener siete [pulsadores](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="16e9e-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="16e9e-114">Todos estos botones especifican [EndDialog](enddialog-controlevent.md) ControlEvent, en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e9e-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="16e9e-115">Cada botón especifica uno de los siguientes atributos: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span><span class="sxs-lookup"><span data-stu-id="16e9e-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="16e9e-116">El foco de estos controles no debe vincularse mediante el uso de la \_ siguiente columna control de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e9e-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="16e9e-117">Estos botones deben colocarse aproximadamente en la misma posición en el cuadro de diálogo porque, cuando se crea, solo se crea un subconjunto de estos siete botones, dependiendo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="16e9e-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="16e9e-118">La coordenada X de los botones se modifica para que los botones que se muestran se espacian uniformemente.</span><span class="sxs-lookup"><span data-stu-id="16e9e-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="16e9e-119">La coordenada Y, el alto y el ancho de los botones no cambian.</span><span class="sxs-lookup"><span data-stu-id="16e9e-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="16e9e-120">Dado que los botones están dispuestos horizontalmente, no se puede colocar ningún otro control en la misma región horizontal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16e9e-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="16e9e-121">En el caso de un cuadro de diálogo de error, \_ se omiten los campos predeterminados del control y cancelar el control \_ de la [tabla del cuadro de diálogo](dialog-table.md) .</span><span class="sxs-lookup"><span data-stu-id="16e9e-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="16e9e-122">El \_ primer campo de control de un cuadro de diálogo de error debe especificar el control ErrorText.</span><span class="sxs-lookup"><span data-stu-id="16e9e-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="16e9e-123">Si en este cuadro de diálogo se incluye un [control de icono](icon-control.md) denominado ErrorIcon, se muestran los siguientes iconos estándar de Windows:</span><span class="sxs-lookup"><span data-stu-id="16e9e-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="16e9e-124">\_Error de IDI en respuesta a los mensajes de imtFatalExit.</span><span class="sxs-lookup"><span data-stu-id="16e9e-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="16e9e-125">\_ADVERTENCIA IDI en respuesta a los mensajes imtError y imtWarning.</span><span class="sxs-lookup"><span data-stu-id="16e9e-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="16e9e-126">IDI \_ información en respuesta a los mensajes de imtOutOfDiskSpace.</span><span class="sxs-lookup"><span data-stu-id="16e9e-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="16e9e-127">El control ErrorIcon debe crearse con el [atributo de control FixedSize](fixedsize-control-attribute.md) establecido para evitar el tamaño incorrecto de los iconos estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="16e9e-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 



