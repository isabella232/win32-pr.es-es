---
description: Es una clase base abstracta que se utiliza en el registro de un consumidor de eventos permanente.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003110"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="19ff6-103">\_\_Clase EventConsumer</span><span class="sxs-lookup"><span data-stu-id="19ff6-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="19ff6-104">La clase del sistema **\_ \_ EventConsumer** es una clase base abstracta que se utiliza en el registro de un consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="19ff6-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="19ff6-105">Puede derivar una nueva clase de consumidor de eventos de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="19ff6-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="19ff6-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="19ff6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19ff6-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="19ff6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ff6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19ff6-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="19ff6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="19ff6-109">Members</span></span>

<span data-ttu-id="19ff6-110">La clase **\_ \_ EventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19ff6-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="19ff6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19ff6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19ff6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19ff6-112">Properties</span></span>

<span data-ttu-id="19ff6-113">La clase **\_ \_ EventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="19ff6-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19ff6-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="19ff6-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ff6-115">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="19ff6-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="19ff6-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19ff6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19ff6-117">Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="19ff6-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="19ff6-118">WMI almacena el SID del usuario que crea una instancia de **\_ \_ EventConsumer** o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="19ff6-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="19ff6-119">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="19ff6-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="19ff6-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ff6-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="19ff6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ff6-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19ff6-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19ff6-123">Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.</span><span class="sxs-lookup"><span data-stu-id="19ff6-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="19ff6-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ff6-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19ff6-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="19ff6-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19ff6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19ff6-127">Cola máxima para un consumidor específico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="19ff6-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19ff6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ff6-128">Remarks</span></span>

<span data-ttu-id="19ff6-129">La clase **\_ \_ EventConsumer** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="19ff6-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="19ff6-130">Los consumidores permanentes definen nuevas clases de consumidor para describir una acción que se realizará y los datos se procesarán cuando los consumidores reciban notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="19ff6-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="19ff6-131">Los consumidores permanentes tienen problemas de seguridad especiales.</span><span class="sxs-lookup"><span data-stu-id="19ff6-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="19ff6-132">Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="19ff6-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19ff6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ff6-133">Requirements</span></span>



| <span data-ttu-id="19ff6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ff6-134">Requirement</span></span> | <span data-ttu-id="19ff6-135">Value</span><span class="sxs-lookup"><span data-stu-id="19ff6-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="19ff6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ff6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="19ff6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19ff6-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="19ff6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19ff6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="19ff6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19ff6-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="19ff6-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19ff6-140">Namespace</span></span><br/>                | <span data-ttu-id="19ff6-141">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="19ff6-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="19ff6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ff6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ff6-143">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="19ff6-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="19ff6-144">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="19ff6-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="19ff6-145">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="19ff6-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="19ff6-146">Crear una nueva clase de consumidor de eventos permanente</span><span class="sxs-lookup"><span data-stu-id="19ff6-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="19ff6-147">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="19ff6-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="19ff6-148">Proteger eventos WMI</span><span class="sxs-lookup"><span data-stu-id="19ff6-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

