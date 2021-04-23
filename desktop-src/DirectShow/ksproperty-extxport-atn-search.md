---
description: Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN). El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909453"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="0b8fa-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="0b8fa-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="0b8fa-105">Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="0b8fa-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="0b8fa-106">El controlador de dispositivo UVC admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0b8fa-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="0b8fa-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="0b8fa-107">Label</span></span> | <span data-ttu-id="0b8fa-108">Value</span><span class="sxs-lookup"><span data-stu-id="0b8fa-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="0b8fa-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="0b8fa-109">Property Set GUID</span></span> | <span data-ttu-id="0b8fa-110">TRANSPORTE EXT DE PROPSETID \_ \_</span><span class="sxs-lookup"><span data-stu-id="0b8fa-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="0b8fa-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b8fa-111">Property ID</span></span>       | <span data-ttu-id="0b8fa-112">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="0b8fa-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="0b8fa-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b8fa-113">Data Type</span></span>         | <span data-ttu-id="0b8fa-114">**KSPROPERTY \_ EXTXPORT \_ S (estructura)**</span><span class="sxs-lookup"><span data-stu-id="0b8fa-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b8fa-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b8fa-115">Remarks</span></span>

<span data-ttu-id="0b8fa-116">Establezca el **miembro dwAbsTrackNumber** de la **estructura \_ EXTXPORT \_ S de KSPROPERTY** en el valor siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b8fa-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="0b8fa-117">La especificación UVC no define cómo el dispositivo usa el bit de continuidad.</span><span class="sxs-lookup"><span data-stu-id="0b8fa-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="0b8fa-118">La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en El DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="0b8fa-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b8fa-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0b8fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8fa-120">Conjunto de propiedades de transporte de dispositivos externos</span><span class="sxs-lookup"><span data-stu-id="0b8fa-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



