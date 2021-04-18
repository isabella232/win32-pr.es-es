---
description: Determina cuándo debe publicar WMI un proveedor de consumidor de eventos.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707413"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="f7459-103">\_\_Clase EventConsumerProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="f7459-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="f7459-104">La clase del sistema **\_ \_ EventConsumerProviderCacheControl** determina cuándo debe liberar WMI un proveedor de consumidores de eventos.</span><span class="sxs-lookup"><span data-stu-id="f7459-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="f7459-105">La clase **\_ \_ EventConsumerProviderCacheControl** es una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="f7459-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="f7459-106">Solo se encuentra en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="f7459-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="f7459-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f7459-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f7459-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f7459-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7459-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7459-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="f7459-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7459-110">Members</span></span>

<span data-ttu-id="f7459-111">La clase **\_ \_ EventConsumerProviderCacheControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f7459-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="f7459-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f7459-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7459-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f7459-113">Properties</span></span>

<span data-ttu-id="f7459-114">La clase **\_ \_ EventConsumerProviderCacheControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f7459-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7459-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="f7459-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7459-116">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7459-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7459-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f7459-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7459-118">Intervalo de tiempo después del cual WMI libera un proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f7459-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="f7459-119">Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f7459-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="f7459-120">La hora está en [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="f7459-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7459-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7459-121">Remarks</span></span>

<span data-ttu-id="f7459-122">La clase **\_ \_ EventConsumerProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="f7459-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="f7459-123">Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f7459-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7459-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7459-124">Requirements</span></span>



| <span data-ttu-id="f7459-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7459-125">Requirement</span></span> | <span data-ttu-id="f7459-126">Value</span><span class="sxs-lookup"><span data-stu-id="f7459-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f7459-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7459-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7459-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7459-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f7459-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7459-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7459-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7459-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f7459-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f7459-131">Namespace</span></span><br/>                | <span data-ttu-id="f7459-132">Root</span><span class="sxs-lookup"><span data-stu-id="f7459-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f7459-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7459-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7459-134">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f7459-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




