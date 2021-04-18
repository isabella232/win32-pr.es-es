---
title: Propiedad ConnectionBarShowPinButton de IMsRdpClientAdvancedSettings5
description: Establece o recupera la configuración del botón anclar en la barra de conexión.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectionBarShowPinButton
- Propiedad ConnectionBarShowPinButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ConnectionBarShowPinButton
- Propiedad ConnectionBarShowPinButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectionBarShowPinButton
- Propiedad ConnectionBarShowPinButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectionBarShowPinButton
- Propiedad ConnectionBarShowPinButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685928"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="59eb9-112">IMsRdpClientAdvancedSettings5:: ConnectionBarShowPinButton (propiedad)</span><span class="sxs-lookup"><span data-stu-id="59eb9-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="59eb9-113">Establece o recupera la configuración del botón anclar en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="59eb9-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="59eb9-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="59eb9-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eb9-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59eb9-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="59eb9-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="59eb9-116">Property value</span></span>

<span data-ttu-id="59eb9-117">Un valor booleano de **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="59eb9-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="59eb9-118">Un valor de **true** muestra el botón anclar en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="59eb9-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="59eb9-119">Un valor de **false** oculta el botón de anclaje en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="59eb9-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eb9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59eb9-120">Requirements</span></span>



| <span data-ttu-id="59eb9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="59eb9-121">Requirement</span></span> | <span data-ttu-id="59eb9-122">Value</span><span class="sxs-lookup"><span data-stu-id="59eb9-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59eb9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59eb9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59eb9-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59eb9-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="59eb9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59eb9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59eb9-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59eb9-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="59eb9-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="59eb9-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="59eb9-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59eb9-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="59eb9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59eb9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59eb9-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59eb9-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="59eb9-131">IID</span><span class="sxs-lookup"><span data-stu-id="59eb9-131">IID</span></span><br/>                      | <span data-ttu-id="59eb9-132">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="59eb9-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59eb9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="59eb9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eb9-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="59eb9-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="59eb9-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="59eb9-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="59eb9-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="59eb9-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="59eb9-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="59eb9-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





