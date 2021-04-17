---
description: Controla cuándo se descarga un proveedor de clase o instancia.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: __ObjectProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707106"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="17afb-103">\_\_Clase ObjectProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="17afb-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="17afb-104">La clase del sistema **\_ \_ ObjectProviderCacheControl** controla cuándo se descarga un proveedor de clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="17afb-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="17afb-105">Solo se encuentra en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="17afb-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="17afb-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17afb-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="17afb-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="17afb-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17afb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17afb-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="17afb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="17afb-109">Members</span></span>

<span data-ttu-id="17afb-110">La clase **\_ \_ ObjectProviderCacheControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17afb-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="17afb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17afb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17afb-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17afb-112">Properties</span></span>

<span data-ttu-id="17afb-113">La clase **\_ \_ ObjectProviderCacheControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17afb-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17afb-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="17afb-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17afb-115">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17afb-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17afb-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="17afb-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="17afb-117">Intervalo de tiempo después del cual WMI libera una instancia, una clase o un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="17afb-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="17afb-118">La hora está en [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="17afb-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17afb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17afb-119">Remarks</span></span>

<span data-ttu-id="17afb-120">La clase **\_ \_ ObjectProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="17afb-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="17afb-121">Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17afb-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17afb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17afb-122">Requirements</span></span>



| <span data-ttu-id="17afb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="17afb-123">Requirement</span></span> | <span data-ttu-id="17afb-124">Value</span><span class="sxs-lookup"><span data-stu-id="17afb-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="17afb-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17afb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17afb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17afb-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="17afb-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17afb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17afb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17afb-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="17afb-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17afb-129">Namespace</span></span><br/>                | <span data-ttu-id="17afb-130">Root</span><span class="sxs-lookup"><span data-stu-id="17afb-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="17afb-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="17afb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17afb-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="17afb-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="17afb-133">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="17afb-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="17afb-134">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="17afb-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

