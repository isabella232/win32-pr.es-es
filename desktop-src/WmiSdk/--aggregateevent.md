---
description: Representa un evento de agregado de varios eventos intrínsecos o extrínsecos individuales.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688408"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="85182-103">\_\_Clase AggregateEvent</span><span class="sxs-lookup"><span data-stu-id="85182-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="85182-104">La clase del sistema **\_ \_ AggregateEvent** representa un evento agregado de varios eventos intrínsecos o extrínsecos individuales.</span><span class="sxs-lookup"><span data-stu-id="85182-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="85182-105">WMI genera una instancia de **\_ \_ AggregateEvent** en lugar de un [**\_ \_ evento**](--event.md) cuando los consumidores se registran con la cláusula [Group Within](group-clause.md) en su consulta de eventos.</span><span class="sxs-lookup"><span data-stu-id="85182-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="85182-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="85182-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="85182-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="85182-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85182-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85182-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="85182-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="85182-109">Members</span></span>

<span data-ttu-id="85182-110">La clase **\_ \_ AggregateEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="85182-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="85182-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85182-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85182-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85182-112">Properties</span></span>

<span data-ttu-id="85182-113">La clase **\_ \_ AggregateEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="85182-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85182-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="85182-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85182-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85182-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85182-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85182-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85182-117">Número de eventos combinados para producir este evento de Resumen único.</span><span class="sxs-lookup"><span data-stu-id="85182-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="85182-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="85182-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85182-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="85182-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="85182-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85182-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85182-121">Copia de uno de los eventos entregados en el intervalo de agregación.</span><span class="sxs-lookup"><span data-stu-id="85182-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="85182-122">Por ejemplo, si un consumidor se ha registrado para eventos de cambio de clave del registro del proveedor de eventos del registro, **representador** contendría una instancia de la clase **RegistryKeyChangeEvent** .</span><span class="sxs-lookup"><span data-stu-id="85182-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85182-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85182-123">Remarks</span></span>

<span data-ttu-id="85182-124">La clase **\_ \_ AggregateEvent** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="85182-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="85182-125">Los proveedores de eventos nunca generan eventos agregados.</span><span class="sxs-lookup"><span data-stu-id="85182-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="85182-126">Deben pasar por alto la cláusula GROUP WITHIN en el procesamiento de consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="85182-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="85182-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85182-127">Requirements</span></span>



| <span data-ttu-id="85182-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="85182-128">Requirement</span></span> | <span data-ttu-id="85182-129">Value</span><span class="sxs-lookup"><span data-stu-id="85182-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="85182-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85182-130">Minimum supported client</span></span><br/> | <span data-ttu-id="85182-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85182-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="85182-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85182-132">Minimum supported server</span></span><br/> | <span data-ttu-id="85182-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85182-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="85182-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85182-134">Namespace</span></span><br/>                | <span data-ttu-id="85182-135">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="85182-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="85182-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="85182-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85182-137">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="85182-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="85182-138">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="85182-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="85182-139">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="85182-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

