---
description: Información general sobre cómo mostrar el panel de entrada.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Mostrar el panel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707423"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="2ad88-103">Mostrar el panel de entrada</span><span class="sxs-lookup"><span data-stu-id="2ad88-103">Displaying the Input Panel</span></span>

<span data-ttu-id="2ad88-104">\[[**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) para código administrado).</span><span class="sxs-lookup"><span data-stu-id="2ad88-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="2ad88-105">Consulte el panel de [entrada de texto Programming](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="2ad88-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="2ad88-106">El orden de los distintos eventos de foco para un control es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ad88-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="2ad88-107">Control. Enter</span><span class="sxs-lookup"><span data-stu-id="2ad88-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="2ad88-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="2ad88-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="2ad88-109">Control. Leave</span><span class="sxs-lookup"><span data-stu-id="2ad88-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="2ad88-110">Control. validando</span><span class="sxs-lookup"><span data-stu-id="2ad88-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="2ad88-111">Control. validado</span><span class="sxs-lookup"><span data-stu-id="2ad88-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="2ad88-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="2ad88-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="2ad88-113">No hay ninguna garantía de que el control realmente tenga el foco en el momento en que se escribe la propiedad [control. visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) cuando se establece en el controlador de eventos [control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="2ad88-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="2ad88-114">El evento control. Enter es el mejor lugar para asociar el objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un control, pero el evento [control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) es el mejor lugar para cambiar la propiedad [PenInputPanel. visible](/previous-versions/ms571984(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="2ad88-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
