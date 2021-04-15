---
title: Propiedad MarkRdpSettingsSecure de IMsRdpClientNonScriptable4
description: Especifica si los valores de Protocolo de escritorio remoto (RDP) se marcan como seguros.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure
- Propiedad MarkRdpSettingsSecure Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad MarkRdpSettingsSecure
- Propiedad MarkRdpSettingsSecure Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534450"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="17b56-116">IMsRdpClientNonScriptable4:: MarkRdpSettingsSecure (propiedad)</span><span class="sxs-lookup"><span data-stu-id="17b56-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="17b56-117">Especifica si los valores de [Protocolo de escritorio remoto](remote-desktop-protocol.md) (RDP) se marcan como seguros.</span><span class="sxs-lookup"><span data-stu-id="17b56-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="17b56-118">Esto indica que los valores aplicados al control están firmados por un editor de terceros o de confianza.</span><span class="sxs-lookup"><span data-stu-id="17b56-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="17b56-119">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="17b56-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b56-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17b56-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="17b56-121">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="17b56-121">Property value</span></span>

<span data-ttu-id="17b56-122">Establece si la configuración de RDP está marcada como segura.</span><span class="sxs-lookup"><span data-stu-id="17b56-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="17b56-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="17b56-123">Error codes</span></span>

<span data-ttu-id="17b56-124">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="17b56-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b56-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b56-125">Requirements</span></span>



| <span data-ttu-id="17b56-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b56-126">Requirement</span></span> | <span data-ttu-id="17b56-127">Value</span><span class="sxs-lookup"><span data-stu-id="17b56-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b56-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b56-128">Minimum supported client</span></span><br/> | <span data-ttu-id="17b56-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17b56-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="17b56-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b56-130">Minimum supported server</span></span><br/> | <span data-ttu-id="17b56-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b56-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="17b56-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="17b56-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="17b56-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b56-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="17b56-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17b56-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b56-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b56-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="17b56-136">IID</span><span class="sxs-lookup"><span data-stu-id="17b56-136">IID</span></span><br/>                      | <span data-ttu-id="17b56-137">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="17b56-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17b56-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="17b56-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b56-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="17b56-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="17b56-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="17b56-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





