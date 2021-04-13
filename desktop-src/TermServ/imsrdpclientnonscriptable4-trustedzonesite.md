---
title: Propiedad TrustedZoneSite de IMsRdpClientNonScriptable4
description: Especifica si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente del usuario.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite
- Propiedad TrustedZoneSite Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad TrustedZoneSite
- Propiedad TrustedZoneSite Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422430"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="e8e86-116">IMsRdpClientNonScriptable4:: TrustedZoneSite (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e8e86-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="e8e86-117">Especifica si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8e86-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="e8e86-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e8e86-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e86-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e86-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="e8e86-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8e86-120">Property value</span></span>

<span data-ttu-id="e8e86-121">Establece la propiedad TrustedZoneSite.</span><span class="sxs-lookup"><span data-stu-id="e8e86-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="e8e86-122">Este método no tiene ningún efecto sobre si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="e8e86-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8e86-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e8e86-123">Error codes</span></span>

<span data-ttu-id="e8e86-124">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8e86-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e86-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e86-125">Requirements</span></span>



| <span data-ttu-id="e8e86-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e86-126">Requirement</span></span> | <span data-ttu-id="e8e86-127">Value</span><span class="sxs-lookup"><span data-stu-id="e8e86-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e86-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e86-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e86-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8e86-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e8e86-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e86-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e86-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8e86-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e8e86-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e8e86-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8e86-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e86-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e8e86-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8e86-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8e86-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e86-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e8e86-136">IID</span><span class="sxs-lookup"><span data-stu-id="e8e86-136">IID</span></span><br/>                      | <span data-ttu-id="e8e86-137">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="e8e86-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8e86-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e86-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e86-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e8e86-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="e8e86-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="e8e86-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





