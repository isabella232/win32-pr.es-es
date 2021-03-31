---
title: Estructura de IPX_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica de IPX \_ contiene datos específicos de IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA de la estructura RAS
- PIPX_SPECIFIC_DATA de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995901"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="8c9e7-105">\_Estructura de datos específica de IPX \_</span><span class="sxs-lookup"><span data-stu-id="8c9e7-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="8c9e7-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="8c9e7-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="8c9e7-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="8c9e7-108">La estructura de **\_ \_ datos específica de IPX** contiene datos específicos de IPX.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c9e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c9e7-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="8c9e7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c9e7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c9e7-111">**Marcas de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="8c9e7-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8c9e7-112">Especifica las marcas que describen la ruta.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="8c9e7-113">Actualmente, este miembro es cero o el siguiente valor de marca.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="8c9e7-114">Value</span><span class="sxs-lookup"><span data-stu-id="8c9e7-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="8c9e7-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8c9e7-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="8c9e7-116"><dt>**\_ \_ ruta WAN de cliente global \_ de \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="8c9e7-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="8c9e7-117">Especifica que esta ruta es para la red global asignada a todos los clientes WAN.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c9e7-118">**FSD \_ TickCount**</span><span class="sxs-lookup"><span data-stu-id="8c9e7-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="8c9e7-119">Especifica el número de pasos que se tarda en llegar a la red de destino.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="8c9e7-120">Los protocolos de enrutamiento que no sean RIP deben convertir sus métricas en pasos.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e7-121">**FSD \_ HopCount**</span><span class="sxs-lookup"><span data-stu-id="8c9e7-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="8c9e7-122">Especifica el recuento de saltos asociado a la ruta.</span><span class="sxs-lookup"><span data-stu-id="8c9e7-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c9e7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c9e7-123">Requirements</span></span>



| <span data-ttu-id="8c9e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c9e7-124">Requirement</span></span> | <span data-ttu-id="8c9e7-125">Value</span><span class="sxs-lookup"><span data-stu-id="8c9e7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8c9e7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c9e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9e7-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c9e7-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="8c9e7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c9e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9e7-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c9e7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8c9e7-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8c9e7-130">End of server support</span></span><br/>    | <span data-ttu-id="8c9e7-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c9e7-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="8c9e7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c9e7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9e7-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9e7-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9e7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c9e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9e7-135">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8c9e7-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="8c9e7-136">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8c9e7-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="8c9e7-137">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="8c9e7-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





