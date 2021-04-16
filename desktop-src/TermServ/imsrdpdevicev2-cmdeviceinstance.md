---
title: Propiedad CmDeviceInstance de IMsRdpDeviceV2
description: Contiene la instancia de dispositivo de Configuration Manager del dispositivo.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CmDeviceInstance
- Propiedad CmDeviceInstance Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685854"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="16c28-106">IMsRdpDeviceV2:: CmDeviceInstance (propiedad)</span><span class="sxs-lookup"><span data-stu-id="16c28-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="16c28-107">Contiene la instancia de dispositivo de Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c28-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="16c28-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16c28-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c28-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16c28-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="16c28-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="16c28-110">Property value</span></span>

<span data-ttu-id="16c28-111">Instancia de dispositivo de Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c28-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c28-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c28-112">Requirements</span></span>



| <span data-ttu-id="16c28-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c28-113">Requirement</span></span> | <span data-ttu-id="16c28-114">Value</span><span class="sxs-lookup"><span data-stu-id="16c28-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16c28-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c28-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16c28-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="16c28-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="16c28-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c28-117">Minimum supported server</span></span><br/> | <span data-ttu-id="16c28-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="16c28-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="16c28-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="16c28-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="16c28-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c28-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16c28-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16c28-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c28-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c28-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16c28-123">IID</span><span class="sxs-lookup"><span data-stu-id="16c28-123">IID</span></span><br/>                      | <span data-ttu-id="16c28-124">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="16c28-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="16c28-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="16c28-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c28-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="16c28-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





