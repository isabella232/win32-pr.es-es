---
description: Registra proveedores de propiedades en WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: __PropertyProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545766"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="57be6-103">\_\_Clase PropertyProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="57be6-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="57be6-104">La clase del sistema **\_ \_ PropertyProviderRegistration** registra proveedores de propiedades en WMI.</span><span class="sxs-lookup"><span data-stu-id="57be6-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="57be6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="57be6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="57be6-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="57be6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57be6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57be6-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="57be6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="57be6-108">Members</span></span>

<span data-ttu-id="57be6-109">La clase **\_ \_ PropertyProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="57be6-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="57be6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57be6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57be6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57be6-111">Properties</span></span>

<span data-ttu-id="57be6-112">La clase **\_ \_ PropertyProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="57be6-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57be6-113">**presta**</span><span class="sxs-lookup"><span data-stu-id="57be6-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57be6-114">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="57be6-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="57be6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57be6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57be6-116">Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa la ruta de acceso del objeto del proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="57be6-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="57be6-117">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="57be6-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="57be6-118">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="57be6-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57be6-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="57be6-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57be6-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="57be6-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="57be6-121">Describe si el proveedor de clase o instancia admite la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="57be6-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="57be6-122">True</span><span class="sxs-lookup"><span data-stu-id="57be6-122">True</span></span>
</dt> <dd>

<span data-ttu-id="57be6-123">El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="57be6-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="57be6-124">False</span><span class="sxs-lookup"><span data-stu-id="57be6-124">False</span></span>
</dt> <dd>

<span data-ttu-id="57be6-125">El proveedor no admite la recuperación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ compatible** con [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="57be6-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57be6-126">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="57be6-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57be6-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="57be6-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57be6-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="57be6-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="57be6-129">Describe si el proveedor de clase o instancia admite la modificación de datos.</span><span class="sxs-lookup"><span data-stu-id="57be6-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="57be6-130">True</span><span class="sxs-lookup"><span data-stu-id="57be6-130">True</span></span>
</dt> <dd>

<span data-ttu-id="57be6-131">El proveedor admite la modificación de la clase o la instancia implementando uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="57be6-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="57be6-132">[**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases)</span><span class="sxs-lookup"><span data-stu-id="57be6-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="57be6-133">[**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases)</span><span class="sxs-lookup"><span data-stu-id="57be6-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="57be6-134">False</span><span class="sxs-lookup"><span data-stu-id="57be6-134">False</span></span>
</dt> <dd>

<span data-ttu-id="57be6-135">El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="57be6-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57be6-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57be6-136">Remarks</span></span>

<span data-ttu-id="57be6-137">La clase **\_ \_ PropertyProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="57be6-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="57be6-138">Solo los administradores pueden registrar un proveedor de propiedades mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ PropertyProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="57be6-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="57be6-139">Solo los administradores pueden eliminar un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="57be6-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="57be6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57be6-140">Requirements</span></span>



| <span data-ttu-id="57be6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="57be6-141">Requirement</span></span> | <span data-ttu-id="57be6-142">Value</span><span class="sxs-lookup"><span data-stu-id="57be6-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="57be6-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57be6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="57be6-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57be6-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="57be6-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57be6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="57be6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57be6-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="57be6-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57be6-147">Namespace</span></span><br/>                | <span data-ttu-id="57be6-148">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="57be6-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="57be6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="57be6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57be6-150">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="57be6-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="57be6-151">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="57be6-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="57be6-152">Registrar un proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="57be6-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

