---
description: La clase es la clase base abstracta para las clases que se utilizan para determinar cuándo debe liberar WMI un objeto de modelo de objetos componentes (COM).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687800"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="95d30-103">\_\_CacheControl (clase)</span><span class="sxs-lookup"><span data-stu-id="95d30-103">\_\_CacheControl class</span></span>

<span data-ttu-id="95d30-104">La clase del sistema **\_ \_ CacheControl** es la clase base abstracta para las clases que se utilizan para determinar cuándo debe liberar WMI un objeto de modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="95d30-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="95d30-105">Nunca se crean instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="95d30-105">Instances of this class are never created.</span></span> <span data-ttu-id="95d30-106">La clase **\_ \_ CacheControl** solo se encuentra en el espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="95d30-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="95d30-107">Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="95d30-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="95d30-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="95d30-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="95d30-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="95d30-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d30-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95d30-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="95d30-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="95d30-111">Members</span></span>

<span data-ttu-id="95d30-112">La clase **\_ \_ CacheControl** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="95d30-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d30-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95d30-113">Remarks</span></span>

<span data-ttu-id="95d30-114">La clase **\_ \_ CacheControl** se deriva de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="95d30-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95d30-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d30-115">Requirements</span></span>



| <span data-ttu-id="95d30-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d30-116">Requirement</span></span> | <span data-ttu-id="95d30-117">Value</span><span class="sxs-lookup"><span data-stu-id="95d30-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="95d30-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d30-118">Minimum supported client</span></span><br/> | <span data-ttu-id="95d30-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d30-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="95d30-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d30-120">Minimum supported server</span></span><br/> | <span data-ttu-id="95d30-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d30-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="95d30-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95d30-122">Namespace</span></span><br/>                | <span data-ttu-id="95d30-123">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="95d30-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="95d30-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d30-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d30-125">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="95d30-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="95d30-126">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="95d30-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="95d30-127">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="95d30-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="95d30-128">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="95d30-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="95d30-129">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="95d30-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="95d30-130">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="95d30-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="95d30-131">\_\_PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="95d30-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="95d30-132">Descargar un proveedor</span><span class="sxs-lookup"><span data-stu-id="95d30-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

