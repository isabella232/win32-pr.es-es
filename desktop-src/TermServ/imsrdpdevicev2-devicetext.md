---
title: Propiedad DeviceText de IMsRdpDeviceV2
description: Contiene el texto del dispositivo.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceText
- Propiedad DeviceText Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274512"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="47ddb-106">IMsRdpDeviceV2::D propiedad eviceText</span><span class="sxs-lookup"><span data-stu-id="47ddb-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="47ddb-107">Contiene el texto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47ddb-107">Contains the device text.</span></span> <span data-ttu-id="47ddb-108">Este es el nombre que Windows muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="47ddb-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="47ddb-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="47ddb-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ddb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47ddb-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="47ddb-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="47ddb-111">Property value</span></span>

<span data-ttu-id="47ddb-112">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47ddb-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="47ddb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47ddb-113">Requirements</span></span>



| <span data-ttu-id="47ddb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47ddb-114">Requirement</span></span> | <span data-ttu-id="47ddb-115">Value</span><span class="sxs-lookup"><span data-stu-id="47ddb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ddb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47ddb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47ddb-117">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="47ddb-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="47ddb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47ddb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47ddb-119">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="47ddb-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="47ddb-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="47ddb-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="47ddb-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ddb-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="47ddb-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47ddb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47ddb-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ddb-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="47ddb-124">IID</span><span class="sxs-lookup"><span data-stu-id="47ddb-124">IID</span></span><br/>                      | <span data-ttu-id="47ddb-125">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="47ddb-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="47ddb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="47ddb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ddb-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="47ddb-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





