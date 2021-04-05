---
title: Estructura de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica del protocolo \_ contiene memoria reservada para los datos específicos de un protocolo de enrutamiento determinado.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA de la estructura RAS
- PPROTOCOL_SPECIFIC_DATA de puntero de estructura RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802792"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="dd2ff-105">\_Estructura de datos específica del protocolo \_</span><span class="sxs-lookup"><span data-stu-id="dd2ff-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="dd2ff-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dd2ff-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="dd2ff-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="dd2ff-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="dd2ff-108">La estructura de **\_ \_ datos específica del protocolo** contiene memoria reservada para los datos específicos de un protocolo de enrutamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="dd2ff-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2ff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd2ff-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="dd2ff-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd2ff-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd2ff-111">**\_Datos PSD**</span><span class="sxs-lookup"><span data-stu-id="dd2ff-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="dd2ff-112">Especifica una matriz de variables **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dd2ff-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="dd2ff-113">Esta memoria está reservada para los datos específicos de los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="dd2ff-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd2ff-114">Requirements</span></span>



| <span data-ttu-id="dd2ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd2ff-115">Requirement</span></span> | <span data-ttu-id="dd2ff-116">Value</span><span class="sxs-lookup"><span data-stu-id="dd2ff-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dd2ff-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2ff-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dd2ff-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="dd2ff-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2ff-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd2ff-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd2ff-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="dd2ff-121">End of server support</span></span><br/>    | <span data-ttu-id="dd2ff-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd2ff-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="dd2ff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd2ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2ff-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2ff-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2ff-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd2ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2ff-126">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="dd2ff-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="dd2ff-127">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="dd2ff-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="dd2ff-128">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="dd2ff-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="dd2ff-129">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="dd2ff-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





