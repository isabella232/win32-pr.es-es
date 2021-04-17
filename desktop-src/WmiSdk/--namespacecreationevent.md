---
description: Notifica un evento de creación de espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se agrega un nuevo espacio de nombres al espacio de nombres actual.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: __NamespaceCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678049"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="cf9ca-103">\_\_Clase NamespaceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="cf9ca-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="cf9ca-104">La clase del sistema **\_ \_ NamespaceCreationEvent** informa de un evento de creación de espacio de nombres, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega un nuevo espacio de nombres al espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="cf9ca-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cf9ca-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf9ca-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="cf9ca-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf9ca-108">Members</span></span>

<span data-ttu-id="cf9ca-109">La clase **\_ \_ NamespaceCreationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cf9ca-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="cf9ca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf9ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf9ca-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf9ca-111">Properties</span></span>

<span data-ttu-id="cf9ca-112">La clase **\_ \_ NamespaceCreationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf9ca-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf9ca-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="cf9ca-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cf9ca-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf9ca-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf9ca-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="cf9ca-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf9ca-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf9ca-119">Tipo de datos: **\_ \_ espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="cf9ca-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf9ca-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf9ca-121">Copia de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) que se creó.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="cf9ca-122">La propiedad **Name** de la instancia de **\_ \_ espacio de nombres** indica qué espacio de nombres se ha creado.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="cf9ca-123">Esta propiedad se hereda de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf9ca-124">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf9ca-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf9ca-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf9ca-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf9ca-127">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="cf9ca-128">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="cf9ca-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="cf9ca-129">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="cf9ca-130">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="cf9ca-131">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf9ca-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf9ca-132">Remarks</span></span>

<span data-ttu-id="cf9ca-133">La clase **\_ \_ NamespaceCreationEvent** se deriva de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ca-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9ca-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf9ca-134">Requirements</span></span>



| <span data-ttu-id="cf9ca-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf9ca-135">Requirement</span></span> | <span data-ttu-id="cf9ca-136">Value</span><span class="sxs-lookup"><span data-stu-id="cf9ca-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cf9ca-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf9ca-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9ca-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf9ca-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cf9ca-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf9ca-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9ca-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf9ca-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cf9ca-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf9ca-141">Namespace</span></span><br/>                | <span data-ttu-id="cf9ca-142">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="cf9ca-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cf9ca-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf9ca-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9ca-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="cf9ca-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="cf9ca-145">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="cf9ca-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

