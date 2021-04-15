---
description: Información general sobre el marco de trabajo de servicios de texto para Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Marco de trabajo de servicios de texto (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688604"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="70b26-103">Marco de trabajo de servicios de texto (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="70b26-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="70b26-104">Cuando el [marco de trabajo de servicios de texto (TSF)](../tsf/text-services-framework.md) está habilitado en un control con un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado, el objeto PenInputPanel puede insertar texto directamente.</span><span class="sxs-lookup"><span data-stu-id="70b26-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="70b26-105">Si el control no admite el marco de trabajo de servicios de texto (TSF), el objeto PenInputPanel debe recurrir al uso de la [función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) para insertar texto.</span><span class="sxs-lookup"><span data-stu-id="70b26-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="70b26-106">La capacidad de insertar texto directamente es muy importante para los caracteres de Asia oriental, donde el uso de la [función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) puede producir caracteres incorrectos.</span><span class="sxs-lookup"><span data-stu-id="70b26-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="70b26-107">TSF proporciona una interfaz para corregir errores de reconocimiento que permiten al usuario final corregir, reescribir o incluso dictar el texto adecuado.</span><span class="sxs-lookup"><span data-stu-id="70b26-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="70b26-108">TSF se habilita llamando al método [EnableTsf](/previous-versions/ms569656(v=vs.100)) con el parámetro *enable* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="70b26-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="70b26-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="70b26-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="70b26-110">Un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado a un control [InkEdit](/previous-versions/ms552265(v=vs.100)) proporciona una experiencia de usuario sólida porque InkEdit admite TSF.</span><span class="sxs-lookup"><span data-stu-id="70b26-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="70b26-111">Sin embargo, asegúrese de establecer la propiedad [InkMode](/previous-versions/ms835850(v=msdn.10)) en [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) en el control InkEdit, como se mencionó en el tema de [procedimientos](best-practices.md) recomendados.</span><span class="sxs-lookup"><span data-stu-id="70b26-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="70b26-112">En el [ejemplo PenInputPanel](peninputpanel-sample.md) se ofrece un ejemplo de cómo habilitar TSF.</span><span class="sxs-lookup"><span data-stu-id="70b26-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70b26-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70b26-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70b26-114">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="70b26-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
