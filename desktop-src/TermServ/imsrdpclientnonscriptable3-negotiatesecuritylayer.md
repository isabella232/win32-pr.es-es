---
title: Propiedad NegotiateSecurityLayer de IMsRdpClientNonScriptable3
description: Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676761"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="43f51-120">IMsRdpClientNonScriptable3:: NegotiateSecurityLayer (propiedad)</span><span class="sxs-lookup"><span data-stu-id="43f51-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="43f51-121">Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.</span><span class="sxs-lookup"><span data-stu-id="43f51-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="43f51-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="43f51-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f51-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43f51-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="43f51-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="43f51-124">Property value</span></span>

<span data-ttu-id="43f51-125">Especifica si se debe habilitar la negociación de la capa de seguridad.</span><span class="sxs-lookup"><span data-stu-id="43f51-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="43f51-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43f51-126">Remarks</span></span>

<span data-ttu-id="43f51-127">Si esta propiedad se establece en **Variant \_ FALSE** y autenticación a nivel de red (NLA) está habilitada en el sistema operativo del cliente, el cliente no negociará el nivel de seguridad y, en su lugar, usará NLA para proteger la conexión RDP.</span><span class="sxs-lookup"><span data-stu-id="43f51-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="43f51-128">Si esta propiedad se establece en **Variant \_ true**, el cliente negociará entre NLA y la seguridad básica de RDP.</span><span class="sxs-lookup"><span data-stu-id="43f51-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="43f51-129">La deshabilitación de la negociación del nivel de seguridad solo es posible cuando se conecta a un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) que ejecuta Windows Vista o sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="43f51-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="43f51-130">Si esta propiedad está habilitada y el cliente intenta conectarse a un servidor host de sesión de escritorio remoto que ejecuta un sistema operativo anterior, se producirá un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="43f51-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43f51-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43f51-131">Requirements</span></span>



| <span data-ttu-id="43f51-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f51-132">Requirement</span></span> | <span data-ttu-id="43f51-133">Value</span><span class="sxs-lookup"><span data-stu-id="43f51-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f51-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43f51-134">Minimum supported client</span></span><br/> | <span data-ttu-id="43f51-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43f51-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="43f51-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43f51-136">Minimum supported server</span></span><br/> | <span data-ttu-id="43f51-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43f51-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="43f51-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="43f51-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="43f51-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43f51-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="43f51-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43f51-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43f51-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43f51-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="43f51-142">IID</span><span class="sxs-lookup"><span data-stu-id="43f51-142">IID</span></span><br/>                      | <span data-ttu-id="43f51-143">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="43f51-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43f51-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="43f51-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f51-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="43f51-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="43f51-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="43f51-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="43f51-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="43f51-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





