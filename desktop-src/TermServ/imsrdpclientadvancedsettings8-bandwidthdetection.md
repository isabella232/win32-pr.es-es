---
title: Propiedad BandwidthDetection de IMsRdpClientAdvancedSettings8
description: Especifica si los cambios de ancho de banda se detectan automáticamente.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BandwidthDetection
- Propiedad BandwidthDetection Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685900"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="3b412-106">IMsRdpClientAdvancedSettings8:: BandwidthDetection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3b412-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="3b412-107">Especifica si los cambios de ancho de banda se detectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3b412-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="3b412-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3b412-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b412-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b412-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="3b412-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3b412-110">Property value</span></span>

<span data-ttu-id="3b412-111">**Variante \_ TRUE** si los cambios de ancho de banda se detectan automáticamente o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b412-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b412-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b412-112">Requirements</span></span>



| <span data-ttu-id="3b412-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b412-113">Requirement</span></span> | <span data-ttu-id="3b412-114">Value</span><span class="sxs-lookup"><span data-stu-id="3b412-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b412-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b412-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b412-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3b412-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="3b412-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b412-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b412-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b412-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="3b412-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3b412-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b412-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b412-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b412-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b412-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b412-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b412-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b412-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b412-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b412-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3b412-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





