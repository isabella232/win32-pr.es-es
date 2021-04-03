---
title: Propiedad PublisherCertificateChain de IMsRdpClientNonScriptable4
description: Controla la cadena de certificados del publicador. La cadena se almacena en una variante de tipo VT \_ BYREF que contiene un puntero a una estructura de contexto de cadena de certificados \_ \_ . Para obtener información acerca de las estructuras de VT \_ BYREF, consulte Variant y VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain
- Propiedad PublisherCertificateChain Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PublisherCertificateChain
- Propiedad PublisherCertificateChain Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905384"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="501a4-118">IMsRdpClientNonScriptable4::P propiedad ublisherCertificateChain</span><span class="sxs-lookup"><span data-stu-id="501a4-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="501a4-119">Controla la cadena de certificados del publicador.</span><span class="sxs-lookup"><span data-stu-id="501a4-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="501a4-120">La cadena se almacena en una variante de tipo **VT \_ BYREF** que contiene un puntero a una estructura de [**\_ \_ contexto de cadena de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="501a4-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="501a4-121">Para obtener información acerca de las estructuras de **VT \_ BYREF** , consulte [Variant y VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="501a4-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="501a4-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="501a4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="501a4-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="501a4-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="501a4-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="501a4-124">Property value</span></span>

<span data-ttu-id="501a4-125">Establece la cadena de certificados del publicador.</span><span class="sxs-lookup"><span data-stu-id="501a4-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="501a4-126">La cadena se almacena en una variante de tipo **VT \_ BYREF** que contiene un puntero a una estructura de [**\_ \_ contexto de cadena de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="501a4-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="501a4-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="501a4-127">Error codes</span></span>

<span data-ttu-id="501a4-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="501a4-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="501a4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="501a4-129">Requirements</span></span>



| <span data-ttu-id="501a4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="501a4-130">Requirement</span></span> | <span data-ttu-id="501a4-131">Value</span><span class="sxs-lookup"><span data-stu-id="501a4-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="501a4-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="501a4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="501a4-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="501a4-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="501a4-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="501a4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="501a4-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="501a4-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="501a4-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="501a4-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="501a4-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="501a4-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="501a4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="501a4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501a4-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="501a4-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="501a4-140">IID</span><span class="sxs-lookup"><span data-stu-id="501a4-140">IID</span></span><br/>                      | <span data-ttu-id="501a4-141">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="501a4-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="501a4-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="501a4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501a4-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="501a4-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="501a4-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="501a4-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

