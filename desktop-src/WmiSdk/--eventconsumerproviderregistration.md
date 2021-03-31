---
description: Registra proveedores de consumidores de eventos con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911974"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="15d38-103">\_\_Clase EventConsumerProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="15d38-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="15d38-104">La clase del sistema **\_ \_ EventConsumerProviderRegistration** registra proveedores de consumidores de eventos con WMI.</span><span class="sxs-lookup"><span data-stu-id="15d38-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="15d38-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="15d38-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="15d38-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="15d38-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d38-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15d38-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="15d38-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="15d38-108">Members</span></span>

<span data-ttu-id="15d38-109">La clase **\_ \_ EventConsumerProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15d38-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="15d38-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15d38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15d38-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15d38-111">Properties</span></span>

<span data-ttu-id="15d38-112">La clase **\_ \_ EventConsumerProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15d38-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15d38-113">**ConsumerClassNames**</span><span class="sxs-lookup"><span data-stu-id="15d38-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d38-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="15d38-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15d38-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15d38-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15d38-116">Matriz de nombres de las clases de consumidor lógicas que admite el proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="15d38-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="15d38-117">**presta**</span><span class="sxs-lookup"><span data-stu-id="15d38-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15d38-118">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="15d38-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="15d38-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15d38-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15d38-120">Ruta de acceso del objeto al proveedor.</span><span class="sxs-lookup"><span data-stu-id="15d38-120">Object path to the provider.</span></span> <span data-ttu-id="15d38-121">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="15d38-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15d38-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15d38-122">Remarks</span></span>

<span data-ttu-id="15d38-123">La clase **\_ \_ EventConsumerProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="15d38-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15d38-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d38-124">Requirements</span></span>



| <span data-ttu-id="15d38-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d38-125">Requirement</span></span> | <span data-ttu-id="15d38-126">Value</span><span class="sxs-lookup"><span data-stu-id="15d38-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="15d38-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15d38-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15d38-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15d38-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="15d38-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15d38-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15d38-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15d38-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="15d38-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15d38-131">Namespace</span></span><br/>                | <span data-ttu-id="15d38-132">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="15d38-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="15d38-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="15d38-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d38-134">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="15d38-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="15d38-135">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="15d38-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="15d38-136">Registrar un proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="15d38-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="15d38-137">Escribir un proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="15d38-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

