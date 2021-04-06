---
title: Estructura de IP_NETWORK (RTM. h)
description: La \_ estructura de red IP describe una dirección de red IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK de la estructura RAS
- PIP_NETWORK de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803008"
---
# <a name="ip_network-structure"></a><span data-ttu-id="12572-105">\_Estructura de red IP</span><span class="sxs-lookup"><span data-stu-id="12572-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="12572-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="12572-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="12572-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="12572-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="12572-108">La estructura de **\_ red IP** describe una dirección de red IP.</span><span class="sxs-lookup"><span data-stu-id="12572-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="12572-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12572-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="12572-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="12572-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="12572-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="12572-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="12572-112">Especifica el número de red IP expresado como una dirección IP en orden de bytes de la máquina.</span><span class="sxs-lookup"><span data-stu-id="12572-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="12572-113">**\_Máscara de máscara**</span><span class="sxs-lookup"><span data-stu-id="12572-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="12572-114">Especifica la máscara de red.</span><span class="sxs-lookup"><span data-stu-id="12572-114">Specifies the network mask.</span></span> <span data-ttu-id="12572-115">Aplique esta máscara a la dirección IP para extraer la dirección de red.</span><span class="sxs-lookup"><span data-stu-id="12572-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="12572-116">La máscara de red está en orden de bytes de la máquina.</span><span class="sxs-lookup"><span data-stu-id="12572-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12572-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12572-117">Requirements</span></span>



| <span data-ttu-id="12572-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="12572-118">Requirement</span></span> | <span data-ttu-id="12572-119">Value</span><span class="sxs-lookup"><span data-stu-id="12572-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12572-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12572-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12572-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="12572-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="12572-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12572-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12572-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12572-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12572-124">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="12572-124">End of server support</span></span><br/>    | <span data-ttu-id="12572-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12572-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="12572-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12572-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12572-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="12572-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12572-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="12572-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12572-129">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="12572-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="12572-130">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="12572-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="12572-131">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="12572-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





