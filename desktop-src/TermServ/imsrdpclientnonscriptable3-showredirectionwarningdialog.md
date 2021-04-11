---
title: Propiedad ShowRedirectionWarningDialog de IMsRdpClientNonScriptable3
description: Especifica o recupera si se debe mostrar el cuadro de diálogo de advertencia de redirección.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog
- Propiedad ShowRedirectionWarningDialog Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad ShowRedirectionWarningDialog
- Propiedad ShowRedirectionWarningDialog Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad ShowRedirectionWarningDialog
- Propiedad ShowRedirectionWarningDialog Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad ShowRedirectionWarningDialog
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad ShowRedirectionWarningDialog
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad ShowRedirectionWarningDialog
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad ShowRedirectionWarningDialog
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad ShowRedirectionWarningDialog
- Servicios de Escritorio remoto de la propiedad ShowRedirectionWarningDialog, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad ShowRedirectionWarningDialog
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079094"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="9dfe2-120">IMsRdpClientNonScriptable3:: ShowRedirectionWarningDialog (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9dfe2-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="9dfe2-121">Especifica o recupera si se debe mostrar el cuadro de diálogo de advertencia de redirección.</span><span class="sxs-lookup"><span data-stu-id="9dfe2-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="9dfe2-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9dfe2-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfe2-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dfe2-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="9dfe2-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9dfe2-124">Property value</span></span>

<span data-ttu-id="9dfe2-125">Especifica si se debe mostrar el cuadro de diálogo de advertencia de redirección.</span><span class="sxs-lookup"><span data-stu-id="9dfe2-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfe2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dfe2-126">Requirements</span></span>



| <span data-ttu-id="9dfe2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfe2-127">Requirement</span></span> | <span data-ttu-id="9dfe2-128">Value</span><span class="sxs-lookup"><span data-stu-id="9dfe2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfe2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dfe2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfe2-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dfe2-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9dfe2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dfe2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfe2-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dfe2-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9dfe2-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9dfe2-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dfe2-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfe2-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9dfe2-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dfe2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dfe2-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfe2-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9dfe2-137">IID</span><span class="sxs-lookup"><span data-stu-id="9dfe2-137">IID</span></span><br/>                      | <span data-ttu-id="9dfe2-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="9dfe2-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dfe2-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dfe2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfe2-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="9dfe2-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="9dfe2-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="9dfe2-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="9dfe2-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="9dfe2-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





