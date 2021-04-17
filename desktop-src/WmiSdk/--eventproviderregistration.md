---
description: Se utiliza para registrar proveedores de eventos con Instrumental de administración de Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697370"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="b727f-103">\_\_Clase EventProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="b727f-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="b727f-104">La clase del sistema **\_ \_ EventProviderRegistration** se utiliza para registrar proveedores de eventos con instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b727f-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="b727f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b727f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b727f-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b727f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b727f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b727f-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="b727f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b727f-108">Members</span></span>

<span data-ttu-id="b727f-109">La clase **\_ \_ EventProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b727f-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="b727f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b727f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b727f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b727f-111">Properties</span></span>

<span data-ttu-id="b727f-112">La clase **\_ \_ EventProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b727f-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b727f-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="b727f-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b727f-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b727f-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b727f-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b727f-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b727f-116">Una o más consultas del lenguaje de consulta de Instrumental de administración de Windows (WQL) que describen los eventos que admite el proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="b727f-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="b727f-117">**presta**</span><span class="sxs-lookup"><span data-stu-id="b727f-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b727f-118">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="b727f-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="b727f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b727f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b727f-120">Ruta de acceso del objeto al proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="b727f-120">Object path to the event provider.</span></span> <span data-ttu-id="b727f-121">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b727f-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b727f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b727f-122">Remarks</span></span>

<span data-ttu-id="b727f-123">Solo los administradores pueden registrar o eliminar un proveedor de eventos mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b727f-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="b727f-124">La clase **\_ \_ EventProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b727f-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b727f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b727f-125">Requirements</span></span>



| <span data-ttu-id="b727f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b727f-126">Requirement</span></span> | <span data-ttu-id="b727f-127">Value</span><span class="sxs-lookup"><span data-stu-id="b727f-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b727f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b727f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b727f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b727f-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b727f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b727f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b727f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b727f-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b727f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b727f-132">Namespace</span></span><br/>                | <span data-ttu-id="b727f-133">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="b727f-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b727f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b727f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b727f-135">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="b727f-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="b727f-136">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b727f-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b727f-137">Registrar un proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="b727f-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="b727f-138">Escribir un proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="b727f-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

