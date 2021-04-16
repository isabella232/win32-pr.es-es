---
title: Propiedad RelativeMouseMode de IMsRdpClientAdvancedSettings6
description: Especifica si el mouse debe usar el modo relativo.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RelativeMouseMode
- Propiedad RelativeMouseMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RelativeMouseMode
- Propiedad RelativeMouseMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RelativeMouseMode
- Propiedad RelativeMouseMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676823"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="e2d41-110">IMsRdpClientAdvancedSettings6:: RelativeMouseMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e2d41-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="e2d41-111">Especifica si el mouse debe usar el modo relativo.</span><span class="sxs-lookup"><span data-stu-id="e2d41-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="e2d41-112">Contiene **Variant \_ true** si el mouse está en modo relativo o **Variant \_ false** si el mouse está en modo absoluto.</span><span class="sxs-lookup"><span data-stu-id="e2d41-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="e2d41-113">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e2d41-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d41-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2d41-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="e2d41-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e2d41-115">Property value</span></span>

<span data-ttu-id="e2d41-116">Contiene el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2d41-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d41-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2d41-117">Remarks</span></span>

<span data-ttu-id="e2d41-118">El modo de mouse indica la forma en que el control ActiveX calcula las coordenadas del mouse que envía al servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="e2d41-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="e2d41-119">Cuando el mouse está en modo relativo, el control ActiveX calcula las coordenadas del mouse con respecto a la última posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2d41-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="e2d41-120">Cuando el mouse está en modo absoluto, el control ActiveX calcula las coordenadas del mouse relativas al escritorio del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e2d41-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d41-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d41-121">Requirements</span></span>



| <span data-ttu-id="e2d41-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d41-122">Requirement</span></span> | <span data-ttu-id="e2d41-123">Value</span><span class="sxs-lookup"><span data-stu-id="e2d41-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d41-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d41-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d41-125">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="e2d41-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="e2d41-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d41-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d41-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2d41-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e2d41-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e2d41-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2d41-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d41-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e2d41-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2d41-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2d41-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d41-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e2d41-132">IID</span><span class="sxs-lookup"><span data-stu-id="e2d41-132">IID</span></span><br/>                      | <span data-ttu-id="e2d41-133">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="e2d41-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2d41-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d41-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d41-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e2d41-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e2d41-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e2d41-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e2d41-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e2d41-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





