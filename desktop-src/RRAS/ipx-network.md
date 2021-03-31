---
title: Estructura de IPX_NETWORK (RTM. h)
description: La \_ estructura de red IPX describe una dirección de red IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- IPX_NETWORK de la estructura RAS
- PIPX_NETWORK de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995902"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="5ff8d-105">\_Estructura de red IPX</span><span class="sxs-lookup"><span data-stu-id="5ff8d-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="5ff8d-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5ff8d-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5ff8d-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="5ff8d-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5ff8d-108">La estructura de **\_ red IPX** describe una dirección de red IPX.</span><span class="sxs-lookup"><span data-stu-id="5ff8d-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff8d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ff8d-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="5ff8d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ff8d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ff8d-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="5ff8d-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5ff8d-112">Contiene el número de red IPX en el orden de bytes de la máquina.</span><span class="sxs-lookup"><span data-stu-id="5ff8d-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ff8d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ff8d-113">Requirements</span></span>



| <span data-ttu-id="5ff8d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff8d-114">Requirement</span></span> | <span data-ttu-id="5ff8d-115">Value</span><span class="sxs-lookup"><span data-stu-id="5ff8d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5ff8d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ff8d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff8d-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ff8d-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="5ff8d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ff8d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff8d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ff8d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5ff8d-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5ff8d-120">End of server support</span></span><br/>    | <span data-ttu-id="5ff8d-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ff8d-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5ff8d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ff8d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff8d-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff8d-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff8d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ff8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff8d-125">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="5ff8d-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5ff8d-126">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="5ff8d-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="5ff8d-127">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="5ff8d-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





