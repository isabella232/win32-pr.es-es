---
title: Propiedad ConnectionBarText de IMsRdpClientNonScriptable3
description: Establece o recupera el texto para actualizar la barra de conexión.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803620"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="d9d1c-120">IMsRdpClientNonScriptable3:: ConnectionBarText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d9d1c-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="d9d1c-121">Establece o recupera el texto para actualizar la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="d9d1c-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="d9d1c-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d9d1c-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d1c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9d1c-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="d9d1c-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9d1c-124">Property value</span></span>

<span data-ttu-id="d9d1c-125">Establece la cadena de texto que se va a mostrar en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="d9d1c-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d1c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9d1c-126">Remarks</span></span>

<span data-ttu-id="d9d1c-127">Debe llamar al método **IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText** antes de llamar al método de [**\_ pantalla completa IMsTscSecuredSettings::p UT**](imstscsecuredsettings-fullscreen.md) o al método de [**\_ pantalla completa IMsRdpClient::p UT**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="d9d1c-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d1c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9d1c-128">Requirements</span></span>



| <span data-ttu-id="d9d1c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9d1c-129">Requirement</span></span> | <span data-ttu-id="d9d1c-130">Value</span><span class="sxs-lookup"><span data-stu-id="d9d1c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d1c-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d1c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d1c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9d1c-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d9d1c-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d1c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d1c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9d1c-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d9d1c-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9d1c-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9d1c-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9d1c-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d9d1c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9d1c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d1c-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9d1c-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d9d1c-139">IID</span><span class="sxs-lookup"><span data-stu-id="d9d1c-139">IID</span></span><br/>                      | <span data-ttu-id="d9d1c-140">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="d9d1c-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9d1c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9d1c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d1c-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d9d1c-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d9d1c-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d9d1c-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d9d1c-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d9d1c-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





