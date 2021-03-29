---
title: Propiedad IsUSBDevice de IMsRdpDeviceV2
description: Especifica si el dispositivo es para el redireccionamiento USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad IsUSBDevice
- Propiedad IsUSBDevice Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad IsUSBDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421922"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="d38f4-106">IMsRdpDeviceV2:: IsUSBDevice (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d38f4-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="d38f4-107">Especifica si el dispositivo es para el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="d38f4-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="d38f4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d38f4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38f4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d38f4-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="d38f4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d38f4-110">Property value</span></span>

<span data-ttu-id="d38f4-111">**true** si el dispositivo es para el redireccionamiento USB; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d38f4-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38f4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d38f4-112">Requirements</span></span>



| <span data-ttu-id="d38f4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38f4-113">Requirement</span></span> | <span data-ttu-id="d38f4-114">Value</span><span class="sxs-lookup"><span data-stu-id="d38f4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d38f4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d38f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d38f4-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="d38f4-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="d38f4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d38f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d38f4-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="d38f4-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="d38f4-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d38f4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="d38f4-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d38f4-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d38f4-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d38f4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d38f4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d38f4-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d38f4-123">IID</span><span class="sxs-lookup"><span data-stu-id="d38f4-123">IID</span></span><br/>                      | <span data-ttu-id="d38f4-124">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="d38f4-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d38f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d38f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38f4-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="d38f4-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





