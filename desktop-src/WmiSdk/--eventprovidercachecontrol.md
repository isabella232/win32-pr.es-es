---
description: Controla cuándo se descarga un proveedor de eventos.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277710"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="7ebc9-103">\_\_Clase EventProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="7ebc9-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="7ebc9-104">La clase del sistema **\_ \_ EventProviderCacheControl** controla cuándo se descarga un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="7ebc9-105">Solo se encuentra en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="7ebc9-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7ebc9-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebc9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ebc9-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="7ebc9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ebc9-109">Members</span></span>

<span data-ttu-id="7ebc9-110">La clase **\_ \_ EventProviderCacheControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ebc9-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="7ebc9-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ebc9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ebc9-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ebc9-112">Properties</span></span>

<span data-ttu-id="7ebc9-113">La clase **\_ \_ EventProviderCacheControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ebc9-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="7ebc9-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ebc9-115">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7ebc9-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ebc9-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7ebc9-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ebc9-117">El intervalo de tiempo después de que Instrumental de administración de Windows (WMI) libera un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="7ebc9-118">La hora está en [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="7ebc9-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="7ebc9-119">Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ebc9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ebc9-120">Remarks</span></span>

<span data-ttu-id="7ebc9-121">La clase **\_ \_ EventProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="7ebc9-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="7ebc9-122">Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7ebc9-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebc9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ebc9-123">Requirements</span></span>



| <span data-ttu-id="7ebc9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ebc9-124">Requirement</span></span> | <span data-ttu-id="7ebc9-125">Value</span><span class="sxs-lookup"><span data-stu-id="7ebc9-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7ebc9-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ebc9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebc9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ebc9-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7ebc9-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ebc9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebc9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ebc9-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7ebc9-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7ebc9-130">Namespace</span></span><br/>                | <span data-ttu-id="7ebc9-131">Root</span><span class="sxs-lookup"><span data-stu-id="7ebc9-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7ebc9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ebc9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebc9-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="7ebc9-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="7ebc9-134">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="7ebc9-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

