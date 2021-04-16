---
description: Esta propiedad envía un comando al dispositivo para buscar un número de pista absoluta (ATN). El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686276"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="d57bd-104">búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="d57bd-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="d57bd-105">Esta propiedad envía un comando al dispositivo para buscar un número de pista absoluta (ATN).</span><span class="sxs-lookup"><span data-stu-id="d57bd-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="d57bd-106">El controlador de dispositivo UVC admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d57bd-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="d57bd-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="d57bd-107">Property Set GUID</span></span> | <span data-ttu-id="d57bd-108">\_transporte ext \_ PROPSETID</span><span class="sxs-lookup"><span data-stu-id="d57bd-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="d57bd-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="d57bd-109">Property ID</span></span>       | <span data-ttu-id="d57bd-110">búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="d57bd-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="d57bd-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d57bd-111">Data Type</span></span>         | <span data-ttu-id="d57bd-112">**KSPROPERTY \_ Estructura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="d57bd-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d57bd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d57bd-113">Remarks</span></span>

<span data-ttu-id="d57bd-114">Establezca el miembro **dwAbsTrackNumber** de la estructura **KSPROPERTY \_ EXTXPORT \_ S** en el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="d57bd-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="d57bd-115">La especificación UVC no define el modo en que el dispositivo usa el bit de continuidad.</span><span class="sxs-lookup"><span data-stu-id="d57bd-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="d57bd-116">La estructura **KSPROPERTY \_ EXTXPORT \_ S** se describe en el DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="d57bd-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="d57bd-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d57bd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57bd-118">Conjunto de propiedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="d57bd-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



