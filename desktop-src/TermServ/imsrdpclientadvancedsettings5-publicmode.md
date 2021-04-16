---
title: Propiedad PublicMode de IMsRdpClientAdvancedSettings5
description: Establece o recupera la configuración para el modo público. El modo público impide que el cliente almacene en caché los datos de usuario en el sistema local.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PublicMode
- Propiedad PublicMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad PublicMode
- Propiedad PublicMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad PublicMode
- Propiedad PublicMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad PublicMode
- Propiedad PublicMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676668"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="4ade3-113">IMsRdpClientAdvancedSettings5::P propiedad ublicMode</span><span class="sxs-lookup"><span data-stu-id="4ade3-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="4ade3-114">Establece o recupera la configuración para el modo público.</span><span class="sxs-lookup"><span data-stu-id="4ade3-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="4ade3-115">El modo público impide que el cliente almacene en caché los datos de usuario en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="4ade3-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="4ade3-116">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4ade3-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ade3-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ade3-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="4ade3-118">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4ade3-118">Property value</span></span>

<span data-ttu-id="4ade3-119">Establece la configuración de modo público en **Variant \_ true** o **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="4ade3-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="4ade3-120">Si se establece en **Variant \_ true**, se habilita la configuración de modo público.</span><span class="sxs-lookup"><span data-stu-id="4ade3-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ade3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ade3-121">Requirements</span></span>



| <span data-ttu-id="4ade3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ade3-122">Requirement</span></span> | <span data-ttu-id="4ade3-123">Value</span><span class="sxs-lookup"><span data-stu-id="4ade3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ade3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ade3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ade3-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ade3-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="4ade3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ade3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ade3-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ade3-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="4ade3-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ade3-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ade3-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ade3-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4ade3-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ade3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ade3-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ade3-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4ade3-132">IID</span><span class="sxs-lookup"><span data-stu-id="4ade3-132">IID</span></span><br/>                      | <span data-ttu-id="4ade3-133">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="4ade3-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ade3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ade3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ade3-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4ade3-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4ade3-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4ade3-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4ade3-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4ade3-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4ade3-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4ade3-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





