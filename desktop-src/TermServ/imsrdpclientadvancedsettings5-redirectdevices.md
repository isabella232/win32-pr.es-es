---
title: Propiedad RedirectDevices de IMsRdpClientAdvancedSettings5
description: Establece o recupera la configuración para la redirección de dispositivos.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDevices
- Propiedad RedirectDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectDevices
- Propiedad RedirectDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectDevices
- Propiedad RedirectDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectDevices
- Propiedad RedirectDevices Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676667"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="1b61c-112">IMsRdpClientAdvancedSettings5:: RedirectDevices (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1b61c-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="1b61c-113">Establece o recupera la configuración para la redirección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1b61c-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="1b61c-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1b61c-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b61c-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b61c-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="1b61c-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1b61c-116">Property value</span></span>

<span data-ttu-id="1b61c-117">Establece el modo de redireccionamiento de dispositivos en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="1b61c-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="1b61c-118">Si se establece en **true**, se habilita el modo de redirección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1b61c-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b61c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b61c-119">Requirements</span></span>



| <span data-ttu-id="1b61c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b61c-120">Requirement</span></span> | <span data-ttu-id="1b61c-121">Value</span><span class="sxs-lookup"><span data-stu-id="1b61c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b61c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b61c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b61c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b61c-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1b61c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b61c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b61c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b61c-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1b61c-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1b61c-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b61c-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b61c-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1b61c-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b61c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b61c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b61c-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1b61c-130">IID</span><span class="sxs-lookup"><span data-stu-id="1b61c-130">IID</span></span><br/>                      | <span data-ttu-id="1b61c-131">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1b61c-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b61c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b61c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b61c-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1b61c-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1b61c-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1b61c-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1b61c-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1b61c-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1b61c-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1b61c-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





