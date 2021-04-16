---
description: Describe cómo crear un objeto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Creación de un objeto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696138"
---
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="f23c3-103">Creación de un objeto PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="f23c3-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="f23c3-104">\[[**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) y por [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="f23c3-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="f23c3-105">Consulte el panel de [entrada de texto Programming](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="f23c3-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="f23c3-106">Los constructores de código administrado proporcionan una forma cómoda de crear un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) y adjuntarlo a un control en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="f23c3-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="f23c3-107">En este ejemplo de C se \# crea un objeto PenInputPanel y se asocia a un control [InkEdit](/previous-versions/ms835842(v=msdn.10)) existente, `InkEdit1` , con una línea de código.</span><span class="sxs-lookup"><span data-stu-id="f23c3-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="f23c3-108">El mismo ejemplo en Visual Basic .NET tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="f23c3-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="f23c3-109">Esta técnica es útil en los casos en los que un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) se asociará a un solo control a lo largo de su duración.</span><span class="sxs-lookup"><span data-stu-id="f23c3-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="f23c3-110">En los casos en los que desee usar un objeto PenInputPanel y asociarlo a varios controles, como se muestra en el [ejemplo PenInputPanel](peninputpanel-sample.md), use la propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) para cambiar el control al que está asociado el objeto PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="f23c3-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="f23c3-111">Para asociar un objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un control sin usar un constructor, use la propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="f23c3-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="f23c3-112">Utilice esta técnica para los lenguajes que no admiten los constructores administrados, como C++.</span><span class="sxs-lookup"><span data-stu-id="f23c3-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 
