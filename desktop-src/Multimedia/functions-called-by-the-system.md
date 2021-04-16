---
title: Funciones llamadas por el sistema
description: Funciones llamadas por el sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimedia, funciones ACM
- audio, funciones ACM
- Administrador de compresión de audio (ACM), funciones
- ACM (Administrador de compresión de audio), funciones
- Funciones ACM
- funciones de devolución de llamada
- Administrador de compresión de audio (ACM), funciones de devolución de llamada
- ACM (Administrador de compresión de audio), funciones de devolución de llamada
- procedimientos de enlace
- procedimientos del controlador
- Administrador de compresión de audio (ACM), procedimientos de enlace
- ACM (Administrador de compresión de audio), procedimientos de enlace
- Administrador de compresión de audio (ACM), procedimientos de controlador
- ACM (Administrador de compresión de audio), procedimientos de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651362"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="f181f-117">Funciones llamadas por el sistema</span><span class="sxs-lookup"><span data-stu-id="f181f-117">Functions Called by the System</span></span>

<span data-ttu-id="f181f-118">El sistema llama a tres tipos diferentes de funciones definidas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f181f-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="f181f-119">Las funciones de devolución de llamada son funciones de la aplicación a las que el sistema llama en respuesta a una solicitud realizada por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f181f-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="f181f-120">Los procedimientos de enlace ayudan a una aplicación a controlar la personalización de los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f181f-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="f181f-121">Un procedimiento de controlador es la implementación de una aplicación de su propio códec, convertidor o filtro.</span><span class="sxs-lookup"><span data-stu-id="f181f-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="f181f-122">Las funciones de devolución de llamada tienen los nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="f181f-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="f181f-123">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f181f-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="f181f-124">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f181f-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="f181f-125">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f181f-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="f181f-126">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f181f-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="f181f-127">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f181f-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="f181f-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f181f-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="f181f-129">La mayoría de las funciones de enumeración en ACM usan funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f181f-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="f181f-130">Por ejemplo, al llamar a una función de enumeración, el ACM enumera los elementos mediante una llamada repetida a la aplicación a través de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f181f-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="f181f-131">No se puede llamar a algunas funciones desde estas funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f181f-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="f181f-132">Funciones a las que no se puede llamar manipular estructuras ACM internas usadas por las funciones de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f181f-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="f181f-133">No se debe llamar a las siguientes funciones desde una función de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="f181f-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="f181f-134">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="f181f-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="f181f-135">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="f181f-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="f181f-136">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="f181f-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="f181f-137">El sistema llama a las siguientes funciones para ayudar a que una aplicación controle la personalización de los cuadros de diálogo:</span><span class="sxs-lookup"><span data-stu-id="f181f-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="f181f-138">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="f181f-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="f181f-139">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="f181f-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="f181f-140">La función siguiente se especifica como un prototipo que permite a una aplicación usar un códec, convertidor o filtro personalizado.</span><span class="sxs-lookup"><span data-stu-id="f181f-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="f181f-141">Una función que se ajuste a este prototipo se puede pasar como argumento a la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="f181f-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="f181f-142">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="f181f-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 