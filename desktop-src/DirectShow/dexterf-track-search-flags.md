---
description: La \_ \_ enumeración de marcas de búsqueda de DEXTERF Track \_ especifica las condiciones de límite en una búsqueda de un objeto en la escala de tiempo.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumeración DEXTERF_TRACK_SEARCH_FLAGS (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653821"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="80ad0-103">\_ \_ Enumeración de marcas de búsqueda de DEXTERF Track \_</span><span class="sxs-lookup"><span data-stu-id="80ad0-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="80ad0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="80ad0-104">\[Deprecated.</span></span> <span data-ttu-id="80ad0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80ad0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80ad0-106">La `DEXTERF_TRACK_SEARCH_FLAGS` enumeración especifica las condiciones de límite en una búsqueda de un objeto en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="80ad0-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ad0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80ad0-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="80ad0-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="80ad0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="80ad0-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**límite de DEXTERF \_**</span><span class="sxs-lookup"><span data-stu-id="80ad0-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="80ad0-110">Buscar un objeto que abarque la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="80ad0-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="80ad0-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exactamente \_ en**</span><span class="sxs-lookup"><span data-stu-id="80ad0-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="80ad0-112">Buscar un objeto que se inicia exactamente en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="80ad0-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="80ad0-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**reenvío de DEXTERF \_**</span><span class="sxs-lookup"><span data-stu-id="80ad0-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="80ad0-114">Buscar un objeto que se inicia a la hora especificada o posterior.</span><span class="sxs-lookup"><span data-stu-id="80ad0-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80ad0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80ad0-115">Remarks</span></span>

<span data-ttu-id="80ad0-116">Estas condiciones de límite se resumen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="80ad0-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="80ad0-117">Valor de enumeración</span><span class="sxs-lookup"><span data-stu-id="80ad0-117">Enumeration value</span></span>    | <span data-ttu-id="80ad0-118">Condición de límite</span><span class="sxs-lookup"><span data-stu-id="80ad0-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="80ad0-119">límite de DEXTERF \_</span><span class="sxs-lookup"><span data-stu-id="80ad0-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="80ad0-120">Inicio <= hora de > TimeStop</span><span class="sxs-lookup"><span data-stu-id="80ad0-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="80ad0-121">DEXTERF \_ exactamente \_ en</span><span class="sxs-lookup"><span data-stu-id="80ad0-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="80ad0-122">Start = = hora</span><span class="sxs-lookup"><span data-stu-id="80ad0-122">Start == Time</span></span>                             |
| <span data-ttu-id="80ad0-123">reenvío de DEXTERF \_</span><span class="sxs-lookup"><span data-stu-id="80ad0-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="80ad0-124">Iniciar >= hora</span><span class="sxs-lookup"><span data-stu-id="80ad0-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="80ad0-125">Inicio: hora de inicio del objeto recuperado.</span><span class="sxs-lookup"><span data-stu-id="80ad0-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="80ad0-126">Detener: hora de detención del objeto recuperado.</span><span class="sxs-lookup"><span data-stu-id="80ad0-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="80ad0-127">Hora: tiempo de búsqueda especificado.</span><span class="sxs-lookup"><span data-stu-id="80ad0-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ad0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80ad0-128">Requirements</span></span>



| <span data-ttu-id="80ad0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="80ad0-129">Requirement</span></span> | <span data-ttu-id="80ad0-130">Value</span><span class="sxs-lookup"><span data-stu-id="80ad0-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80ad0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80ad0-131">Header</span></span><br/> | <dl> <span data-ttu-id="80ad0-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="80ad0-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ad0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="80ad0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ad0-134">**IAMTimelineTrack::GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="80ad0-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




