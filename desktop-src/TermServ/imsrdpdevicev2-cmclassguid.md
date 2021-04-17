---
title: Propiedad CmClassGuid de IMsRdpDeviceV2
description: Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CmClassGuid
- Propiedad CmClassGuid Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676557"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="676df-106">IMsRdpDeviceV2:: CmClassGuid (propiedad)</span><span class="sxs-lookup"><span data-stu-id="676df-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="676df-107">Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="676df-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="676df-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="676df-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="676df-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="676df-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="676df-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="676df-110">Property value</span></span>

<span data-ttu-id="676df-111">GUID de la clase de instalación de Configuration Manager para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="676df-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="676df-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="676df-112">Requirements</span></span>



| <span data-ttu-id="676df-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="676df-113">Requirement</span></span> | <span data-ttu-id="676df-114">Value</span><span class="sxs-lookup"><span data-stu-id="676df-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="676df-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="676df-115">Minimum supported client</span></span><br/> | <span data-ttu-id="676df-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="676df-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="676df-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="676df-117">Minimum supported server</span></span><br/> | <span data-ttu-id="676df-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="676df-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="676df-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="676df-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="676df-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676df-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="676df-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="676df-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="676df-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676df-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="676df-123">IID</span><span class="sxs-lookup"><span data-stu-id="676df-123">IID</span></span><br/>                      | <span data-ttu-id="676df-124">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="676df-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="676df-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="676df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676df-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="676df-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





