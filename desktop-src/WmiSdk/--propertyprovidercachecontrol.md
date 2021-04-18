---
description: Controla la memoria caché cuando se descarga un proveedor de propiedades.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277130"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="fc62d-103">\_\_Clase PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="fc62d-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="fc62d-104">La clase **\_ \_ PropertyProviderCacheControl** controla la memoria caché cuando se descarga un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc62d-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="fc62d-105">Esta clase solo existe en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="fc62d-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="fc62d-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fc62d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fc62d-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="fc62d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc62d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc62d-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="fc62d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc62d-109">Members</span></span>

<span data-ttu-id="fc62d-110">La clase **\_ \_ PropertyProviderCacheControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc62d-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="fc62d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc62d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc62d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc62d-112">Properties</span></span>

<span data-ttu-id="fc62d-113">La clase **\_ \_ PropertyProviderCacheControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc62d-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc62d-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="fc62d-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc62d-115">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc62d-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc62d-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc62d-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fc62d-117">Intervalo de tiempo después de que WMI libera un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc62d-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="fc62d-118">La hora está en el formato de intervalo.</span><span class="sxs-lookup"><span data-stu-id="fc62d-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc62d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc62d-119">Remarks</span></span>

<span data-ttu-id="fc62d-120">La clase **\_ \_ PropertyProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="fc62d-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="fc62d-121">Para obtener más información, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fc62d-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc62d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc62d-122">Requirements</span></span>



| <span data-ttu-id="fc62d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc62d-123">Requirement</span></span> | <span data-ttu-id="fc62d-124">Value</span><span class="sxs-lookup"><span data-stu-id="fc62d-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fc62d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc62d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fc62d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc62d-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fc62d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc62d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fc62d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc62d-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fc62d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc62d-129">Namespace</span></span><br/>                | <span data-ttu-id="fc62d-130">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="fc62d-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fc62d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc62d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc62d-132">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="fc62d-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




