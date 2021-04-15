---
title: Estructura de IPX_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ estructura de \_ dirección de próximo salto IPX \_ contiene la dirección del enrutador de próximo salto para una ruta IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS de la estructura RAS
- PIPX_NEXT_HOP_ADDRESS de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488950"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="653a4-105">\_Estructura de dirección de próximo salto de IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="653a4-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="653a4-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="653a4-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="653a4-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="653a4-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="653a4-108">La estructura de **\_ dirección de próximo \_ salto \_ IPX** contiene la dirección del enrutador de próximo salto para una ruta IPX.</span><span class="sxs-lookup"><span data-stu-id="653a4-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="653a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="653a4-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="653a4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="653a4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="653a4-111">**\_Mac Nha**</span><span class="sxs-lookup"><span data-stu-id="653a4-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="653a4-112">Especifica la dirección MAC del enrutador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="653a4-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="653a4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653a4-113">Requirements</span></span>



| <span data-ttu-id="653a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="653a4-114">Requirement</span></span> | <span data-ttu-id="653a4-115">Value</span><span class="sxs-lookup"><span data-stu-id="653a4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="653a4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653a4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="653a4-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="653a4-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="653a4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653a4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="653a4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="653a4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="653a4-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="653a4-120">End of server support</span></span><br/>    | <span data-ttu-id="653a4-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="653a4-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="653a4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="653a4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="653a4-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="653a4-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653a4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="653a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653a4-125">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="653a4-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="653a4-126">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="653a4-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="653a4-127">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="653a4-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





