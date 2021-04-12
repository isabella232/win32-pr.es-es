---
description: Actúa como clase primaria para las clases de registro para varios tipos de proveedores.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: __ProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156617"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="c2e11-103">\_\_Clase ProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="c2e11-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="c2e11-104">La clase de sistema abstracta **\_ \_ ProviderRegistration** actúa como clase primaria para las clases de registro para varios tipos de proveedores.</span><span class="sxs-lookup"><span data-stu-id="c2e11-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="c2e11-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c2e11-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c2e11-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c2e11-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e11-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2e11-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="c2e11-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2e11-108">Members</span></span>

<span data-ttu-id="c2e11-109">La clase **\_ \_ ProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2e11-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c2e11-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2e11-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2e11-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2e11-111">Properties</span></span>

<span data-ttu-id="c2e11-112">La clase **\_ \_ ProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2e11-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2e11-113">**presta**</span><span class="sxs-lookup"><span data-stu-id="c2e11-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e11-114">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="c2e11-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="c2e11-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2e11-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e11-116">Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa la ruta de acceso del objeto al proveedor.</span><span class="sxs-lookup"><span data-stu-id="c2e11-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2e11-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2e11-117">Remarks</span></span>

<span data-ttu-id="c2e11-118">La clase **\_ \_ ProviderRegistration** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2e11-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="c2e11-119">Nunca se crean instancias de la clase del sistema **\_ \_ ProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="c2e11-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="c2e11-120">Las clases que los proveedores utilizan para crear instancias para el registro derivan directa o indirectamente de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c2e11-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="c2e11-121">Estas clases son:</span><span class="sxs-lookup"><span data-stu-id="c2e11-121">These classes are:</span></span>

[<span data-ttu-id="c2e11-122">**\_\_ClassProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="c2e11-123">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="c2e11-124">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="c2e11-125">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="c2e11-126">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="c2e11-127">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="c2e11-128">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c2e11-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="c2e11-129">Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y su registro.</span><span class="sxs-lookup"><span data-stu-id="c2e11-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e11-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e11-130">Requirements</span></span>



| <span data-ttu-id="c2e11-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e11-131">Requirement</span></span> | <span data-ttu-id="c2e11-132">Value</span><span class="sxs-lookup"><span data-stu-id="c2e11-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c2e11-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2e11-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e11-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2e11-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c2e11-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2e11-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e11-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2e11-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c2e11-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2e11-137">Namespace</span></span><br/>                | <span data-ttu-id="c2e11-138">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="c2e11-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c2e11-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2e11-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e11-140">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="c2e11-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="c2e11-141">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="c2e11-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c2e11-142">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="c2e11-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

