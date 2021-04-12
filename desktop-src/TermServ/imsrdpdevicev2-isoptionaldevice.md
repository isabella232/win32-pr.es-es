---
title: Propiedad IsOptionalDevice de IMsRdpDeviceV2
description: Especifica si el dispositivo es opcional para el redireccionamiento USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad IsOptionalDevice
- Propiedad IsOptionalDevice Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491633"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="c5c7d-106">IMsRdpDeviceV2:: IsOptionalDevice (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c5c7d-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="c5c7d-107">Especifica si el dispositivo es opcional para el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="c5c7d-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="c5c7d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5c7d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c7d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5c7d-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="c5c7d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5c7d-110">Property value</span></span>

<span data-ttu-id="c5c7d-111">**true** si el dispositivo es opcional; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c5c7d-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c7d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5c7d-112">Requirements</span></span>



| <span data-ttu-id="c5c7d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c7d-113">Requirement</span></span> | <span data-ttu-id="c5c7d-114">Value</span><span class="sxs-lookup"><span data-stu-id="c5c7d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c7d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c7d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c7d-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="c5c7d-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="c5c7d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c7d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c7d-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="c5c7d-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="c5c7d-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5c7d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5c7d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c7d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5c7d-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5c7d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c7d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c7d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5c7d-123">IID</span><span class="sxs-lookup"><span data-stu-id="c5c7d-123">IID</span></span><br/>                      | <span data-ttu-id="c5c7d-124">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="c5c7d-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c5c7d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5c7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c7d-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="c5c7d-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





