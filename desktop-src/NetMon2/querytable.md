---
description: La estructura QUERYTABLE proporciona una lista de los equipos que usan actualmente Monitor de red para capturar datos de red.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estructura QUERYTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677685"
---
# <a name="querytable-structure"></a><span data-ttu-id="08da1-103">Estructura QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="08da1-103">QUERYTABLE structure</span></span>

<span data-ttu-id="08da1-104">La estructura **QUERYTABLE** proporciona una lista de los equipos que usan actualmente monitor de red para capturar datos de red.</span><span class="sxs-lookup"><span data-stu-id="08da1-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="08da1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08da1-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="08da1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="08da1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="08da1-107">**nStationQueries**</span><span class="sxs-lookup"><span data-stu-id="08da1-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="08da1-108">En la entrada, el número máximo de equipos que desea que Monitor de red devuelvan.</span><span class="sxs-lookup"><span data-stu-id="08da1-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="08da1-109">En la salida, el número de estructuras [STATIONQUERY](stationquery.md) devueltas por monitor de red.</span><span class="sxs-lookup"><span data-stu-id="08da1-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="08da1-110">Cada estructura **STATIONQUERY** representa un equipo que está capturando datos actualmente.</span><span class="sxs-lookup"><span data-stu-id="08da1-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="08da1-111">**StationQuery**</span><span class="sxs-lookup"><span data-stu-id="08da1-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="08da1-112">En la entrada, una matriz de estructuras [STATIONQUERY](stationquery.md) vacías que contiene el número de elementos especificados en **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="08da1-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="08da1-113">En la salida, una estructura [STATIONQUERY](stationquery.md) rellena para cada equipo que está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="08da1-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="08da1-114">El número de elementos rellenados es devuelto por **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="08da1-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08da1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08da1-115">Remarks</span></span>

<span data-ttu-id="08da1-116">La aplicación que realiza la llamada debe asignar la memoria para esta estructura y la matriz [STATIONQUERY](stationquery.md) , y se puede liberar después de que ya no se necesite la información.</span><span class="sxs-lookup"><span data-stu-id="08da1-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="08da1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08da1-117">Requirements</span></span>



| <span data-ttu-id="08da1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="08da1-118">Requirement</span></span> | <span data-ttu-id="08da1-119">Value</span><span class="sxs-lookup"><span data-stu-id="08da1-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08da1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08da1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="08da1-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08da1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="08da1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08da1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="08da1-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08da1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="08da1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08da1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="08da1-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08da1-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08da1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="08da1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08da1-127">IDelaydC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="08da1-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="08da1-128">IESP::QueryStations</span><span class="sxs-lookup"><span data-stu-id="08da1-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="08da1-129">IRTC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="08da1-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="08da1-130">IStas:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="08da1-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="08da1-131">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="08da1-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




