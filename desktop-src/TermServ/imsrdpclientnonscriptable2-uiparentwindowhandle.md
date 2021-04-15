---
title: Propiedad UIParentWindowHandle de IMsRdpClientNonScriptable2
description: Establece o recupera el identificador de ventana para que sea la ventana primaria de los cuadros de diálogo que muestra el control. Esto permite que cualquier ventana mostrada por el control sea modal correctamente con respecto a las ventanas que muestra la aplicación primaria.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad UIParentWindowHandle
- Propiedad UIParentWindowHandle Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad UIParentWindowHandle
- Propiedad UIParentWindowHandle Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad UIParentWindowHandle
- Propiedad UIParentWindowHandle Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad UIParentWindowHandle
- Propiedad UIParentWindowHandle Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad UIParentWindowHandle
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489118"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="30bf1-113">IMsRdpClientNonScriptable2:: UIParentWindowHandle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="30bf1-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="30bf1-114">Establece o recupera el identificador de ventana para que sea la ventana primaria de los cuadros de diálogo que muestra el control.</span><span class="sxs-lookup"><span data-stu-id="30bf1-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="30bf1-115">Esto permite que cualquier ventana mostrada por el control sea modal correctamente con respecto a las ventanas que muestra la aplicación primaria.</span><span class="sxs-lookup"><span data-stu-id="30bf1-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="30bf1-116">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="30bf1-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bf1-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30bf1-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="30bf1-118">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="30bf1-118">Property value</span></span>

<span data-ttu-id="30bf1-119">El nuevo identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="30bf1-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30bf1-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="30bf1-120">Error codes</span></span>

<span data-ttu-id="30bf1-121">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="30bf1-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bf1-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30bf1-122">Remarks</span></span>

<span data-ttu-id="30bf1-123">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30bf1-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30bf1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30bf1-124">Requirements</span></span>



| <span data-ttu-id="30bf1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="30bf1-125">Requirement</span></span> | <span data-ttu-id="30bf1-126">Value</span><span class="sxs-lookup"><span data-stu-id="30bf1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30bf1-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30bf1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30bf1-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30bf1-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="30bf1-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30bf1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30bf1-130">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="30bf1-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="30bf1-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="30bf1-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="30bf1-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30bf1-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="30bf1-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30bf1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30bf1-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30bf1-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="30bf1-135">IID</span><span class="sxs-lookup"><span data-stu-id="30bf1-135">IID</span></span><br/>                      | <span data-ttu-id="30bf1-136">IID \_ IMsRdpClientNonScriptable2 se define como 17a5e535-4072-4fa4-af32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="30bf1-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30bf1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="30bf1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bf1-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="30bf1-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="30bf1-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="30bf1-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="30bf1-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="30bf1-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="30bf1-141">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="30bf1-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="30bf1-142">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="30bf1-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="30bf1-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="30bf1-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





