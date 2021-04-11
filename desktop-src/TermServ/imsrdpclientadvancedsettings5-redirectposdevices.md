---
title: Propiedad RedirectPOSDevices de IMsRdpClientAdvancedSettings5
description: Establece o recupera la configuración para la redirección de dispositivos de punto de servicio.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectPOSDevices
- Propiedad RedirectPOSDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectPOSDevices
- Propiedad RedirectPOSDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectPOSDevices
- Propiedad RedirectPOSDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectPOSDevices
- Propiedad RedirectPOSDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectPOSDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150601"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="65858-112">IMsRdpClientAdvancedSettings5:: RedirectPOSDevices (propiedad)</span><span class="sxs-lookup"><span data-stu-id="65858-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="65858-113">Establece o recupera la configuración para la redirección de dispositivos de punto de servicio.</span><span class="sxs-lookup"><span data-stu-id="65858-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="65858-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="65858-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65858-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65858-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="65858-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65858-116">Property value</span></span>

<span data-ttu-id="65858-117">Establece el modo de redirección de dispositivo de punto de servicio en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="65858-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="65858-118">Si se establece en **true**, se habilita el modo de redirección de dispositivo de punto de servicio.</span><span class="sxs-lookup"><span data-stu-id="65858-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="65858-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65858-119">Requirements</span></span>



| <span data-ttu-id="65858-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65858-120">Requirement</span></span> | <span data-ttu-id="65858-121">Value</span><span class="sxs-lookup"><span data-stu-id="65858-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65858-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65858-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65858-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65858-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="65858-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65858-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65858-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65858-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="65858-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65858-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="65858-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65858-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65858-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65858-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65858-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65858-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65858-130">IID</span><span class="sxs-lookup"><span data-stu-id="65858-130">IID</span></span><br/>                      | <span data-ttu-id="65858-131">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="65858-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65858-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="65858-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65858-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65858-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="65858-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65858-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65858-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65858-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65858-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="65858-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





