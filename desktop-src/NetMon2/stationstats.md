---
description: La estructura STATIONSTATS proporciona estadísticas sobre una estación específica descrita por la captura actual.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Estructura STATIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082460"
---
# <a name="stationstats-structure"></a><span data-ttu-id="a5edb-103">Estructura STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="a5edb-103">STATIONSTATS structure</span></span>

<span data-ttu-id="a5edb-104">La estructura **STATIONSTATS** proporciona estadísticas sobre una [*estación*](s.md) específica descrita por la captura actual.</span><span class="sxs-lookup"><span data-stu-id="a5edb-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5edb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5edb-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="a5edb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5edb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5edb-107">**NextStationStats**</span><span class="sxs-lookup"><span data-stu-id="a5edb-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-108">Índice de la siguiente estación registrada en la matriz de estructura **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="a5edb-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-109">**SessionPartnerList**</span><span class="sxs-lookup"><span data-stu-id="a5edb-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-110">Índice de la lista de asociados de la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-111">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="a5edb-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-112">Este miembro está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a5edb-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-113">**StationAddress**</span><span class="sxs-lookup"><span data-stu-id="a5edb-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-114">Dirección MAC de la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-115">**Pad**</span><span class="sxs-lookup"><span data-stu-id="a5edb-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-116">Alineación de **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a5edb-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-117">**TotalPacketsReceived**</span><span class="sxs-lookup"><span data-stu-id="a5edb-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-118">Número total de paquetes enviados a la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-119">**TotalDirectedPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="a5edb-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-120">Número total de paquetes dirigidos enviados por la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-121">**TotalBroadcastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="a5edb-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-122">Número total de paquetes dirigidos a difusión (dirección MAC FF FF FF FF FF FF) enviados por la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-123">**TotalMulticastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="a5edb-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-124">Número total de paquetes de multidifusión (conjunto de bits de grupo en la dirección de destino) enviados por la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="a5edb-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-126">Número total de bytes enviados a la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="a5edb-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="a5edb-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="a5edb-128">Número total de bytes enviados por la estación.</span><span class="sxs-lookup"><span data-stu-id="a5edb-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5edb-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5edb-129">Remarks</span></span>

<span data-ttu-id="a5edb-130">Monitor de red almacena información de la sesión y de la estación en dos matrices asociadas.</span><span class="sxs-lookup"><span data-stu-id="a5edb-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="a5edb-131">cuyos elementos son estructuras [SESSIONSTATS](sessionstats.md) y **STATIONSTATS** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a5edb-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="a5edb-132">Los miembros de estas estructuras se pueden usar para navegar entre ellos.</span><span class="sxs-lookup"><span data-stu-id="a5edb-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="a5edb-133">Por ejemplo, para pasar a la siguiente estación, use **NextStationStats**.</span><span class="sxs-lookup"><span data-stu-id="a5edb-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="a5edb-134">Para ir a la lista de asociados de sesión en la matriz SESSIONSTATS, use el índice proporcionado en **SessionPartnerList**.</span><span class="sxs-lookup"><span data-stu-id="a5edb-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="a5edb-135">La matriz **STATIONSTATS** contiene un elemento para cada estación utilizada durante la captura actual.</span><span class="sxs-lookup"><span data-stu-id="a5edb-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="a5edb-136">El algoritmo Monitor de red utiliza para agregar elementos a esta matriz se basa en la forma más eficaz de registrar información mientras la captura está en curso.</span><span class="sxs-lookup"><span data-stu-id="a5edb-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="a5edb-137">Por consiguiente, la siguiente estación no es siempre el siguiente elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a5edb-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5edb-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5edb-138">Requirements</span></span>



| <span data-ttu-id="a5edb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5edb-139">Requirement</span></span> | <span data-ttu-id="a5edb-140">Value</span><span class="sxs-lookup"><span data-stu-id="a5edb-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a5edb-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5edb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a5edb-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a5edb-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5edb-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5edb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a5edb-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5edb-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5edb-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5edb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5edb-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5edb-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5edb-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5edb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5edb-148">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="a5edb-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="a5edb-149">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="a5edb-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="a5edb-150">IStas:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="a5edb-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




