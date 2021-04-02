---
title: Propiedad SuperPanAccelerationFactor de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica el factor de aceleración de SuperPan. El factor de aceleración de SuperPan determina la rapidez con la que se gira la pantalla en el modo SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SuperPanAccelerationFactor
- Propiedad SuperPanAccelerationFactor Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad SuperPanAccelerationFactor
- Propiedad SuperPanAccelerationFactor Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997151"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="e0e1f-109">IMsRdpClientAdvancedSettings7:: SuperPanAccelerationFactor (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e0e1f-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="e0e1f-110">Especifica o recupera un valor que indica el factor de aceleración de SuperPan.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="e0e1f-111">El factor de aceleración de SuperPan determina la rapidez con la que se gira la pantalla en el modo SuperPan.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="e0e1f-112">El factor de aceleración es el número de píxeles que la vista de pantalla desplaza en una dirección determinada para cada píxel de movimiento del mouse por parte del cliente.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="e0e1f-113">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e1f-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0e1f-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="e0e1f-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0e1f-115">Property value</span></span>

<span data-ttu-id="e0e1f-116">Factor de aceleración de SuperPan que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="e0e1f-117">El factor de aceleración SuperPan es el número de píxeles que la vista de pantalla desplaza en una dirección determinada para cada píxel de movimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="e0e1f-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e1f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0e1f-118">Remarks</span></span>

<span data-ttu-id="e0e1f-119">Para obtener más información sobre SuperPan, consulte [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="e0e1f-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e1f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e1f-120">Requirements</span></span>



| <span data-ttu-id="e0e1f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e1f-121">Requirement</span></span> | <span data-ttu-id="e0e1f-122">Value</span><span class="sxs-lookup"><span data-stu-id="e0e1f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e1f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0e1f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e1f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0e1f-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="e0e1f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0e1f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e1f-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0e1f-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="e0e1f-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0e1f-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0e1f-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e1f-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e0e1f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0e1f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0e1f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e1f-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e0e1f-131">IID</span><span class="sxs-lookup"><span data-stu-id="e0e1f-131">IID</span></span><br/>                      | <span data-ttu-id="e0e1f-132">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="e0e1f-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0e1f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0e1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e1f-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e0e1f-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e0e1f-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e0e1f-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e0e1f-136">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="e0e1f-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





