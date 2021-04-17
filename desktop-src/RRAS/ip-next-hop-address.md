---
title: Estructura de IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ estructura de \_ dirección de próximo salto IP \_ contiene la dirección del enrutador de próximo salto para una ruta IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS de la estructura RAS
- PIP_NEXT_HOP_ADDRESS de la estructura RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651409"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="9e12c-105">\_Estructura de dirección de próximo \_ salto IP \_</span><span class="sxs-lookup"><span data-stu-id="9e12c-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="9e12c-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9e12c-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9e12c-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="9e12c-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9e12c-108">La estructura de **\_ dirección de próximo \_ salto \_ IP** contiene la dirección del enrutador de próximo salto para una ruta IP.</span><span class="sxs-lookup"><span data-stu-id="9e12c-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e12c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e12c-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="9e12c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e12c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e12c-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="9e12c-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9e12c-112">Especifica la dirección de red IP expresada como una dirección IP en orden de bytes de la máquina.</span><span class="sxs-lookup"><span data-stu-id="9e12c-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="9e12c-113">**\_Máscara de máscara**</span><span class="sxs-lookup"><span data-stu-id="9e12c-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="9e12c-114">Especifica la máscara de red.</span><span class="sxs-lookup"><span data-stu-id="9e12c-114">Specifies the network mask.</span></span> <span data-ttu-id="9e12c-115">Aplique esta máscara a la dirección IP para extraer la dirección de red.</span><span class="sxs-lookup"><span data-stu-id="9e12c-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="9e12c-116">La máscara de red está en orden de bytes de la máquina.</span><span class="sxs-lookup"><span data-stu-id="9e12c-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e12c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e12c-117">Remarks</span></span>

<span data-ttu-id="9e12c-118">La estructura de **\_ dirección de próximo \_ salto \_ IP** es una definición de tipo de la estructura de [**\_ red IP**](ip-network.md) .</span><span class="sxs-lookup"><span data-stu-id="9e12c-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="9e12c-119">La definición de tipo está en RTM. h.</span><span class="sxs-lookup"><span data-stu-id="9e12c-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e12c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e12c-120">Requirements</span></span>



| <span data-ttu-id="9e12c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e12c-121">Requirement</span></span> | <span data-ttu-id="9e12c-122">Value</span><span class="sxs-lookup"><span data-stu-id="9e12c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9e12c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e12c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9e12c-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9e12c-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="9e12c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e12c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9e12c-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e12c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e12c-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9e12c-127">End of server support</span></span><br/>    | <span data-ttu-id="9e12c-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e12c-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="9e12c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e12c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e12c-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e12c-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e12c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e12c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e12c-132">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9e12c-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9e12c-133">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9e12c-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="9e12c-134">**\_red IP**</span><span class="sxs-lookup"><span data-stu-id="9e12c-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="9e12c-135">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="9e12c-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





