---
description: La estructura SESSIONSTATS proporciona estadísticas sobre una sesión.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Estructura SESSIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276275"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="d315d-103">Estructura SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="d315d-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="d315d-104">La estructura **SESSIONSTATS** proporciona estadísticas sobre una [*sesión*](s.md).</span><span class="sxs-lookup"><span data-stu-id="d315d-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d315d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d315d-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="d315d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d315d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d315d-107">**NextSession**</span><span class="sxs-lookup"><span data-stu-id="d315d-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="d315d-108">Índice de la siguiente sesión del propietario de la estación.</span><span class="sxs-lookup"><span data-stu-id="d315d-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="d315d-109">**StationOwner**</span><span class="sxs-lookup"><span data-stu-id="d315d-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="d315d-110">Índice de una estación propietaria dentro de la matriz de estructura [STATIONSTATS](stationstats.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="d315d-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="d315d-111">La estación propietaria es la estación que inició la sesión, la estación que envió los paquetes de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d315d-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="d315d-112">**StationPartner**</span><span class="sxs-lookup"><span data-stu-id="d315d-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="d315d-113">Índice de la otra estación dentro de la matriz de estructura [STATIONSTATS](stationstats.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="d315d-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="d315d-114">La estación de asociado es la estación que recibió los paquetes de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d315d-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="d315d-115">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="d315d-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d315d-116">Este miembro está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d315d-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="d315d-117">**TotalPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="d315d-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="d315d-118">Número de paquetes enviados en la sesión.</span><span class="sxs-lookup"><span data-stu-id="d315d-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d315d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d315d-119">Remarks</span></span>

<span data-ttu-id="d315d-120">Monitor de red almacena información de la sesión y de la estación en dos matrices asociadas, cuyos elementos son **SESSIONSTATS** y [STATIONSTATS](stationstats.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d315d-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="d315d-121">Los miembros de estas estructuras se pueden usar para navegar entre ellos.</span><span class="sxs-lookup"><span data-stu-id="d315d-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="d315d-122">Por ejemplo, para pasar a la siguiente sesión de un propietario de una estación concreta, use **NextSession**.</span><span class="sxs-lookup"><span data-stu-id="d315d-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="d315d-123">Para saltar al propietario y a la estación de socio comercial de la sesión en la matriz STATIONSTATS, use el índice proporcionado en **StationOwner** y **StationPartner**.</span><span class="sxs-lookup"><span data-stu-id="d315d-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="d315d-124">La matriz SESSIONSTATS contiene un elemento para cada sesión en la captura actual.</span><span class="sxs-lookup"><span data-stu-id="d315d-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="d315d-125">El algoritmo Monitor de red usa para agregar elementos a la matriz SESSIONSTATS se basa en la grabación eficaz de la información mientras la captura está en curso.</span><span class="sxs-lookup"><span data-stu-id="d315d-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="d315d-126">Por consiguiente, la siguiente sesión de una estación propietaria específica no es siempre el siguiente elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d315d-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d315d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d315d-127">Requirements</span></span>



| <span data-ttu-id="d315d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d315d-128">Requirement</span></span> | <span data-ttu-id="d315d-129">Value</span><span class="sxs-lookup"><span data-stu-id="d315d-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d315d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d315d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d315d-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d315d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d315d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d315d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d315d-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d315d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d315d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d315d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d315d-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d315d-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d315d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d315d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d315d-137">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="d315d-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="d315d-138">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="d315d-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="d315d-139">IStas:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="d315d-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




