---
description: Se utiliza para determinar si WMI libera un puntero IWbemUnboundObjectSink de proveedores de consumidor de eventos.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697650"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="07306-103">\_\_Clase EventSinkCacheControl</span><span class="sxs-lookup"><span data-stu-id="07306-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="07306-104">La clase del sistema **\_ \_ EventSinkCacheControl** se usa para determinar cuándo el WMI libera un puntero [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) del proveedor del consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="07306-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="07306-105">La clase **\_ \_ EventSinkCacheControl** es una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="07306-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="07306-106">Solo se encuentra en el \\ espacio de nombres raíz.</span><span class="sxs-lookup"><span data-stu-id="07306-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="07306-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="07306-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="07306-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="07306-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07306-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07306-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="07306-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="07306-110">Members</span></span>

<span data-ttu-id="07306-111">La clase **\_ \_ EventSinkCacheControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="07306-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="07306-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="07306-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07306-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="07306-113">Properties</span></span>

<span data-ttu-id="07306-114">La clase **\_ \_ EventSinkCacheControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="07306-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07306-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="07306-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07306-116">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07306-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07306-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="07306-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07306-118">Intervalo de tiempo después del cual WMI libera un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="07306-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="07306-119">Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="07306-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="07306-120">La hora está en [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="07306-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07306-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07306-121">Remarks</span></span>

<span data-ttu-id="07306-122">La clase **\_ \_ EventSinkCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="07306-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="07306-123">Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="07306-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07306-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07306-124">Requirements</span></span>



| <span data-ttu-id="07306-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07306-125">Requirement</span></span> | <span data-ttu-id="07306-126">Value</span><span class="sxs-lookup"><span data-stu-id="07306-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="07306-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07306-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07306-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07306-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="07306-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07306-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07306-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07306-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="07306-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07306-131">Namespace</span></span><br/>                | <span data-ttu-id="07306-132">Root</span><span class="sxs-lookup"><span data-stu-id="07306-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="07306-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="07306-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07306-134">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="07306-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




