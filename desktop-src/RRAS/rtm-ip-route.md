---
title: Estructura de RTM_IP_ROUTE (RTM. h)
description: La \_ estructura de ruta IP de RTM \_ contiene información que describe una ruta propiedad de la familia de protocolos IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE de la estructura RAS
- PRTM_IP_ROUTE de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677003"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="f85a2-105">\_Estructura de ruta IP de RTM \_</span><span class="sxs-lookup"><span data-stu-id="f85a2-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="f85a2-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f85a2-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f85a2-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="f85a2-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f85a2-108">La estructura de **\_ \_ ruta IP de RTM** contiene información que describe una ruta propiedad de la familia de protocolos IP.</span><span class="sxs-lookup"><span data-stu-id="f85a2-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="f85a2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f85a2-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="f85a2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f85a2-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f85a2-111">**Marca de tiempo de RR \_**</span><span class="sxs-lookup"><span data-stu-id="f85a2-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-112">Especifica la hora a la que se creó o se actualizó por última vez la entrada de ruta.</span><span class="sxs-lookup"><span data-stu-id="f85a2-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="f85a2-113">Este miembro lo establece el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="f85a2-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="f85a2-114">La hora se expresa como una estructura de FILETIME.</span><span class="sxs-lookup"><span data-stu-id="f85a2-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-115">**RR \_ RoutingProtocol**</span><span class="sxs-lookup"><span data-stu-id="f85a2-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-116">Especifica el protocolo de enrutamiento que ha agregado la ruta.</span><span class="sxs-lookup"><span data-stu-id="f85a2-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="f85a2-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-118">Especifica la interfaz a través de la que se obtuvo la ruta.</span><span class="sxs-lookup"><span data-stu-id="f85a2-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-119">**RR \_ ProtocolSpecificData**</span><span class="sxs-lookup"><span data-stu-id="f85a2-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-120">Especifica una estructura de [**\_ \_ datos específica del protocolo**](protocol-specific-data.md) que contiene la memoria reservada para los datos específicos del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="f85a2-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-121">**\_Red RR**</span><span class="sxs-lookup"><span data-stu-id="f85a2-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-122">Especifica una estructura de [**\_ red IP**](ip-network.md) que contiene una dirección de red IP.</span><span class="sxs-lookup"><span data-stu-id="f85a2-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="f85a2-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-124">Especifica una estructura de [**\_ dirección de próximo \_ salto \_ IP**](ip-next-hop-address.md) que contiene la dirección del enrutador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="f85a2-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="f85a2-125">**RR \_ FamilySpecificData**</span><span class="sxs-lookup"><span data-stu-id="f85a2-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="f85a2-126">Especifica una estructura de [**\_ \_ datos específica de IP**](ip-specific-data.md) que contiene datos específicos de la familia de protocolos IP.</span><span class="sxs-lookup"><span data-stu-id="f85a2-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f85a2-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f85a2-127">Remarks</span></span>

<span data-ttu-id="f85a2-128">Los miembros de la estructura de **\_ \_ ruta IP de RTM** están alineados con **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f85a2-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f85a2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f85a2-129">Requirements</span></span>



| <span data-ttu-id="f85a2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f85a2-130">Requirement</span></span> | <span data-ttu-id="f85a2-131">Value</span><span class="sxs-lookup"><span data-stu-id="f85a2-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f85a2-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f85a2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f85a2-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f85a2-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="f85a2-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f85a2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f85a2-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f85a2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f85a2-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f85a2-136">End of server support</span></span><br/>    | <span data-ttu-id="f85a2-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f85a2-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f85a2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f85a2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f85a2-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f85a2-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f85a2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f85a2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85a2-141">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="f85a2-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f85a2-142">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="f85a2-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="f85a2-143">**\_red IP**</span><span class="sxs-lookup"><span data-stu-id="f85a2-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="f85a2-144">**Dirección IP del \_ próximo \_ salto \_**</span><span class="sxs-lookup"><span data-stu-id="f85a2-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="f85a2-145">**\_datos específicos de IP \_**</span><span class="sxs-lookup"><span data-stu-id="f85a2-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





