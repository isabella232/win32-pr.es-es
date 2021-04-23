---
description: Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado. El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909452"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="1672d-104">BÚSQUEDA DE CÓDIGO \_ DE TIEMPO DE EXTXPORT \_ DE KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="1672d-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="1672d-105">Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="1672d-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="1672d-106">El controlador de dispositivo UVC admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="1672d-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="1672d-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="1672d-107">Label</span></span> | <span data-ttu-id="1672d-108">Value</span><span class="sxs-lookup"><span data-stu-id="1672d-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="1672d-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="1672d-109">Property Set GUID</span></span> | <span data-ttu-id="1672d-110">TRANSPORTE EXT DE PROPSETID \_ \_</span><span class="sxs-lookup"><span data-stu-id="1672d-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="1672d-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="1672d-111">Property ID</span></span>       | <span data-ttu-id="1672d-112">BÚSQUEDA DE CÓDIGO \_ DE TIEMPO DE EXTXPORT \_ DE KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="1672d-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="1672d-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1672d-113">Data Type</span></span>         | <span data-ttu-id="1672d-114">**KSPROPERTY \_ EXTXPORT \_ S (estructura)**</span><span class="sxs-lookup"><span data-stu-id="1672d-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="1672d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1672d-115">Remarks</span></span>

<span data-ttu-id="1672d-116">Rellene el miembro **Timecode de** la estructura **\_ EXTXPORT \_ S de KSPROPERTY** con el marco, segundo, minuto y hora deseados.</span><span class="sxs-lookup"><span data-stu-id="1672d-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="1672d-117">La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en El DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="1672d-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="1672d-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1672d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1672d-119">Conjunto de propiedades de transporte de dispositivos externos</span><span class="sxs-lookup"><span data-stu-id="1672d-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



