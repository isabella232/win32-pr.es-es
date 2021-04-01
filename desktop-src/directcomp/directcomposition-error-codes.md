---
title: Códigos de error de DirectComposition (Dcomp. h)
description: En esta sección se describen los códigos de error específicos de DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150690"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="388e5-103">Códigos de error de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="388e5-103">DirectComposition error codes</span></span>

<span data-ttu-id="388e5-104">Si se produce un error, Microsoft DirectComposition devuelve un código como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="388e5-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="388e5-105">En esta sección se describen los códigos de error específicos de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="388e5-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="388e5-106">Para obtener una lista de los códigos de error del modelo de objetos componentes (COM) generales, vea [códigos de error com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="388e5-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="388e5-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**ERROR de DCOMPOSITION \_ \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="388e5-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="388e5-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="388e5-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="388e5-109">El identificador de ventana que se especificó en una llamada al método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertenece a un proceso diferente del que creó el objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="388e5-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="388e5-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="388e5-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="388e5-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="388e5-112">La superficie ya se estaba representando cuando la aplicación llamó al método [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) .</span><span class="sxs-lookup"><span data-stu-id="388e5-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="388e5-113">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="388e5-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="388e5-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa**</span><span class="sxs-lookup"><span data-stu-id="388e5-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="388e5-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="388e5-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="388e5-116">La aplicación llamó al método [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para una superficie que no se está representando.</span><span class="sxs-lookup"><span data-stu-id="388e5-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="388e5-117">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="388e5-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="388e5-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**la \_ ventana de error DCOMPOSITION \_ \_ ya está \_ compuesta**</span><span class="sxs-lookup"><span data-stu-id="388e5-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="388e5-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="388e5-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="388e5-120">Se llamó al método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) con *hWnd* y los parámetros de *nivel superior* para los que ya existe un árbol visual.</span><span class="sxs-lookup"><span data-stu-id="388e5-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="388e5-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="388e5-121">Remarks</span></span>

<span data-ttu-id="388e5-122">Si una llamada a [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) era la acción más reciente:</span><span class="sxs-lookup"><span data-stu-id="388e5-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="388e5-123">Llamar a este método:</span><span class="sxs-lookup"><span data-stu-id="388e5-123">Calling this method:</span></span>                                    | <span data-ttu-id="388e5-124">Devuelve este valor:</span><span class="sxs-lookup"><span data-stu-id="388e5-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="388e5-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="388e5-126">**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="388e5-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="388e5-128">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="388e5-129">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="388e5-130">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="388e5-131">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="388e5-132">**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="388e5-133">Si una llamada a [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) era la acción más reciente:</span><span class="sxs-lookup"><span data-stu-id="388e5-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="388e5-134">Llamar a este método:</span><span class="sxs-lookup"><span data-stu-id="388e5-134">Calling this method:</span></span>                                    | <span data-ttu-id="388e5-135">Devuelve este valor:</span><span class="sxs-lookup"><span data-stu-id="388e5-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="388e5-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="388e5-137">**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="388e5-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="388e5-139">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="388e5-140">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="388e5-141">**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="388e5-142">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="388e5-143">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="388e5-144">Si una llamada a [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) era la acción más reciente:</span><span class="sxs-lookup"><span data-stu-id="388e5-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="388e5-145">Llamar a este método:</span><span class="sxs-lookup"><span data-stu-id="388e5-145">Calling this method:</span></span>                                    | <span data-ttu-id="388e5-146">Devuelve este valor:</span><span class="sxs-lookup"><span data-stu-id="388e5-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="388e5-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="388e5-148">**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**</span><span class="sxs-lookup"><span data-stu-id="388e5-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="388e5-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="388e5-150">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="388e5-151">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="388e5-152">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="388e5-153">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="388e5-154">**\_superficie de error DCOMPOSITION \_ \_ que se va a \_ representar.**</span><span class="sxs-lookup"><span data-stu-id="388e5-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="388e5-155">Si una llamada a [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) era la acción más reciente:</span><span class="sxs-lookup"><span data-stu-id="388e5-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="388e5-156">Llamar a este método:</span><span class="sxs-lookup"><span data-stu-id="388e5-156">Calling this method:</span></span>                                    | <span data-ttu-id="388e5-157">Devuelve este valor:</span><span class="sxs-lookup"><span data-stu-id="388e5-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="388e5-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="388e5-159">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="388e5-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="388e5-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="388e5-161">**la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.**</span><span class="sxs-lookup"><span data-stu-id="388e5-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="388e5-162">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="388e5-163">**la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.**</span><span class="sxs-lookup"><span data-stu-id="388e5-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="388e5-164">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="388e5-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="388e5-165">**la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.**</span><span class="sxs-lookup"><span data-stu-id="388e5-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="388e5-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="388e5-166">Requirements</span></span>



| <span data-ttu-id="388e5-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="388e5-167">Requirement</span></span> | <span data-ttu-id="388e5-168">Value</span><span class="sxs-lookup"><span data-stu-id="388e5-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="388e5-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388e5-169">Minimum supported client</span></span><br/> | <span data-ttu-id="388e5-170">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="388e5-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="388e5-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388e5-171">Minimum supported server</span></span><br/> | <span data-ttu-id="388e5-172">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="388e5-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="388e5-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="388e5-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="388e5-174"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="388e5-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388e5-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="388e5-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388e5-176">Referencia de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="388e5-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

