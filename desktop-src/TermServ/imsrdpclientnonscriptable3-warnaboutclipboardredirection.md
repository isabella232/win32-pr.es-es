---
title: Propiedad WarnAboutClipboardRedirection de IMsRdpClientNonScriptable3
description: Especifica o recupera si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533933"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="2e14e-120">IMsRdpClientNonScriptable3:: WarnAboutClipboardRedirection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2e14e-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="2e14e-121">Especifica o recupera si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="2e14e-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="2e14e-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2e14e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e14e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e14e-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="2e14e-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2e14e-124">Property value</span></span>

<span data-ttu-id="2e14e-125">Especifica si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="2e14e-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e14e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e14e-126">Requirements</span></span>



| <span data-ttu-id="2e14e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e14e-127">Requirement</span></span> | <span data-ttu-id="2e14e-128">Value</span><span class="sxs-lookup"><span data-stu-id="2e14e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e14e-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e14e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e14e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e14e-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="2e14e-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e14e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e14e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e14e-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2e14e-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2e14e-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e14e-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e14e-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2e14e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e14e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e14e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e14e-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2e14e-137">IID</span><span class="sxs-lookup"><span data-stu-id="2e14e-137">IID</span></span><br/>                      | <span data-ttu-id="2e14e-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="2e14e-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e14e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e14e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e14e-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2e14e-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="2e14e-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2e14e-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2e14e-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2e14e-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





