---
title: Estructura de RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ estructura de ruta de IPX RTM contiene información que describe una ruta para la familia del protocolo IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE de la estructura RAS
- PRTM_IPX_ROUTE de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996167"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="6eb46-105">\_Estructura de ruta IPX de RTM \_</span><span class="sxs-lookup"><span data-stu-id="6eb46-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="6eb46-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6eb46-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="6eb46-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="6eb46-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="6eb46-108">La estructura de **\_ \_ ruta de IPX RTM** contiene información que describe una ruta para la familia del protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="6eb46-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb46-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6eb46-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="6eb46-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6eb46-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6eb46-111">**Marca de tiempo de RR \_**</span><span class="sxs-lookup"><span data-stu-id="6eb46-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-112">Especifica la hora a la que se creó o se actualizó por última vez la entrada de ruta.</span><span class="sxs-lookup"><span data-stu-id="6eb46-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="6eb46-113">Este miembro lo establece el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="6eb46-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="6eb46-114">La hora se expresa como una estructura de FILETIME.</span><span class="sxs-lookup"><span data-stu-id="6eb46-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-115">**RR \_ RoutingProtocol**</span><span class="sxs-lookup"><span data-stu-id="6eb46-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-116">Especifica el protocolo de enrutamiento que ha agregado la ruta.</span><span class="sxs-lookup"><span data-stu-id="6eb46-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="6eb46-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-118">Especifica la interfaz a través de la que se obtuvo la ruta.</span><span class="sxs-lookup"><span data-stu-id="6eb46-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-119">**RR \_ ProtocolSpecificData**</span><span class="sxs-lookup"><span data-stu-id="6eb46-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-120">Especifica una estructura de [**\_ \_ datos específica del protocolo**](protocol-specific-data.md) que contiene la memoria reservada para los datos específicos de los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="6eb46-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-121">**\_Red RR**</span><span class="sxs-lookup"><span data-stu-id="6eb46-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-122">Especifica una estructura de [**\_ red IPX**](ipx-network.md) que contiene una dirección de red IP.</span><span class="sxs-lookup"><span data-stu-id="6eb46-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="6eb46-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-124">Especifica una estructura de [**\_ dirección de próximo \_ salto \_ IPX**](ipx-next-hop-address.md) que contiene la dirección del enrutador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="6eb46-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="6eb46-125">**RR \_ FamilySpecificData**</span><span class="sxs-lookup"><span data-stu-id="6eb46-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="6eb46-126">Especifica una estructura de [**\_ \_ datos específica de IPX**](ipx-specific-data.md) que contiene datos específicos de la familia de protocolos IPX.</span><span class="sxs-lookup"><span data-stu-id="6eb46-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eb46-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6eb46-127">Remarks</span></span>

<span data-ttu-id="6eb46-128">Los miembros de la estructura de **\_ \_ ruta IPX RTM** están alineados con el **valor DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6eb46-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb46-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb46-129">Requirements</span></span>



| <span data-ttu-id="6eb46-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb46-130">Requirement</span></span> | <span data-ttu-id="6eb46-131">Value</span><span class="sxs-lookup"><span data-stu-id="6eb46-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6eb46-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eb46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb46-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6eb46-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="6eb46-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eb46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb46-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6eb46-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6eb46-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6eb46-136">End of server support</span></span><br/>    | <span data-ttu-id="6eb46-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6eb46-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="6eb46-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eb46-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb46-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb46-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb46-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6eb46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb46-141">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="6eb46-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="6eb46-142">Estructuras de la versión 1 del administrador de tablas de enrutamiento \_ \_</span><span class="sxs-lookup"><span data-stu-id="6eb46-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="6eb46-143">**\_red IPX**</span><span class="sxs-lookup"><span data-stu-id="6eb46-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="6eb46-144">**\_dirección de próximo \_ salto \_ de IPX**</span><span class="sxs-lookup"><span data-stu-id="6eb46-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="6eb46-145">**\_datos específicos de IPX \_**</span><span class="sxs-lookup"><span data-stu-id="6eb46-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





