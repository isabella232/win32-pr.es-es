---
description: Esta propiedad envía un comando al dispositivo para buscar un código de tiempo especificado. El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079930"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="23ef3-104">KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="23ef3-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="23ef3-105">Esta propiedad envía un comando al dispositivo para buscar un código de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="23ef3-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="23ef3-106">El controlador de dispositivo UVC admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="23ef3-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="23ef3-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="23ef3-107">Property Set GUID</span></span> | <span data-ttu-id="23ef3-108">\_transporte ext \_ PROPSETID</span><span class="sxs-lookup"><span data-stu-id="23ef3-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="23ef3-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="23ef3-109">Property ID</span></span>       | <span data-ttu-id="23ef3-110">KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="23ef3-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="23ef3-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="23ef3-111">Data Type</span></span>         | <span data-ttu-id="23ef3-112">**KSPROPERTY \_ Estructura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="23ef3-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="23ef3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23ef3-113">Remarks</span></span>

<span data-ttu-id="23ef3-114">Rellene el miembro de **código de tiempo** de la estructura **KSPROPERTY \_ EXTXPORT \_ S** con el fotograma deseado, segundo, minuto y hora.</span><span class="sxs-lookup"><span data-stu-id="23ef3-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="23ef3-115">La estructura **KSPROPERTY \_ EXTXPORT \_ S** se describe en el DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="23ef3-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="23ef3-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="23ef3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ef3-117">Conjunto de propiedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="23ef3-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



