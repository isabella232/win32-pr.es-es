---
description: Describe el uso del objeto PenInputPanel con cuadros combinados.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Usar PenInputPanel con cuadros combinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809596"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="f8ad2-103">Usar PenInputPanel con cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="f8ad2-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="f8ad2-104">\[El objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) se ha reemplazado por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f8ad2-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="f8ad2-105">Consulte el panel de [entrada de texto Programming](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="f8ad2-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="f8ad2-106">Si adjunta un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a un control [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , puntee en el lápiz de Tablet PC en el cuadro combinado editar parte del control en tiempo de ejecución, el objeto PenInputPanel no aparece.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="f8ad2-107">Sin embargo, aparece si puntea en la flecha desplegable.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="f8ad2-108">Esto se debe a que la ventana del control de edición del cuadro combinado no es la ventana que recibe los mensajes de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="f8ad2-109">Los cuadros combinados tienen una ventana de edición secundaria.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="f8ad2-110">La solución a este problema es determinar si la ventana a la que está asociado el objeto PenInputPanel tiene una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="f8ad2-111">Si es así, puede adjuntar el objeto PenInputPanel a la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="f8ad2-112">Al establecer la propiedad [VerticalOffset](/previous-versions/ms571983(v=vs.100)) del objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) en un valor de-1, el panel aparece en la parte superior del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 
