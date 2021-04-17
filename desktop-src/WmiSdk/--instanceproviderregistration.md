---
description: Registra proveedores de instancias en WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706769"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="22675-103">\_\_Clase InstanceProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="22675-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="22675-104">La clase del sistema **\_ \_ InstanceProviderRegistration** registra los proveedores de instancias en WMI.</span><span class="sxs-lookup"><span data-stu-id="22675-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="22675-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="22675-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="22675-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="22675-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22675-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22675-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="22675-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="22675-108">Members</span></span>

<span data-ttu-id="22675-109">La clase **\_ \_ InstanceProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22675-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="22675-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22675-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22675-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22675-111">Properties</span></span>

<span data-ttu-id="22675-112">La clase **\_ \_ InstanceProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22675-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22675-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="22675-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-114">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="22675-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="22675-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-116">Indica que un proveedor de clase o instancia proporciona datos o recupera datos de WMI y del repositorio de Modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="22675-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="22675-117">Los proveedores de extracción admiten el acceso dinámico a sus datos; y los proveedores de inserciones almacenan sus datos en el repositorio CIM y utilizan WMI para proporcionar acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="22675-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="22675-118">Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="22675-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="22675-119">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="22675-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="22675-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Extracción** (0)</span><span class="sxs-lookup"><span data-stu-id="22675-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="22675-121">El proveedor es un proveedor de extracción.</span><span class="sxs-lookup"><span data-stu-id="22675-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="22675-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Inserte** (1)</span><span class="sxs-lookup"><span data-stu-id="22675-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22675-123">El proveedor es un proveedor de inserciones.</span><span class="sxs-lookup"><span data-stu-id="22675-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="22675-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="22675-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="22675-125">El proveedor es un proveedor de comprobación de inserciones.</span><span class="sxs-lookup"><span data-stu-id="22675-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="22675-126">Tenga en cuenta que los proveedores de comprobación de la instalación no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="22675-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-127">**presta**</span><span class="sxs-lookup"><span data-stu-id="22675-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-128">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="22675-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="22675-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22675-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22675-130">Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa la ruta de acceso del objeto al proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="22675-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="22675-131">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="22675-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="22675-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="22675-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="22675-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22675-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-135">Matriz de los tipos de compatibilidad incluida en el proveedor para el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="22675-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="22675-136">Los proveedores de clases no admiten todos los tipos de consultas.</span><span class="sxs-lookup"><span data-stu-id="22675-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="22675-137">Los proveedores de instancias pueden establecer **QuerySupportLevels** en **null** si no admiten el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="22675-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="22675-138">Los proveedores que admiten consultas implementan el método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="22675-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="22675-139">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="22675-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="22675-140">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="22675-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="22675-141">("WQL: Associatorsers")</span><span class="sxs-lookup"><span data-stu-id="22675-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="22675-142">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="22675-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="22675-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="22675-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="22675-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="22675-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-150">Si **es true**, el proveedor admite la eliminación de datos.</span><span class="sxs-lookup"><span data-stu-id="22675-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="22675-151">True</span><span class="sxs-lookup"><span data-stu-id="22675-151">True</span></span>
</dt> <dd>

<span data-ttu-id="22675-152">El proveedor admite la eliminación de la clase o la instancia implementando [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="22675-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="22675-153">False</span><span class="sxs-lookup"><span data-stu-id="22675-153">False</span></span>
</dt> <dd>

<span data-ttu-id="22675-154">El proveedor no admite la eliminación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="22675-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="22675-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-156">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-158">Si **es true**, el proveedor admite la enumeración de datos.</span><span class="sxs-lookup"><span data-stu-id="22675-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="22675-159">Reales</span><span class="sxs-lookup"><span data-stu-id="22675-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="22675-160">El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (clase) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="22675-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="22675-161">Es</span><span class="sxs-lookup"><span data-stu-id="22675-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="22675-162">El proveedor no admite la enumeración de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="22675-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="22675-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-164">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-166">Si **es true**, el proveedor de la clase o la instancia admite la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="22675-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="22675-167">True</span><span class="sxs-lookup"><span data-stu-id="22675-167">True</span></span>
</dt> <dd>

<span data-ttu-id="22675-168">El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="22675-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="22675-169">False</span><span class="sxs-lookup"><span data-stu-id="22675-169">False</span></span>
</dt> <dd>

<span data-ttu-id="22675-170">El proveedor no admite la recuperación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ compatible** con [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="22675-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="22675-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-174">Si **es true**, el proveedor de clase o instancia admite la modificación de datos.</span><span class="sxs-lookup"><span data-stu-id="22675-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="22675-175">Reales</span><span class="sxs-lookup"><span data-stu-id="22675-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="22675-176">El proveedor admite la modificación de la clase o la instancia implementando uno de los métodos siguientes: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).</span><span class="sxs-lookup"><span data-stu-id="22675-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="22675-177">Es</span><span class="sxs-lookup"><span data-stu-id="22675-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="22675-178">El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="22675-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22675-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="22675-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22675-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22675-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22675-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="22675-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22675-182">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="22675-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22675-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22675-183">Remarks</span></span>

<span data-ttu-id="22675-184">La clase **\_ \_ InstanceProviderRegistration** se deriva de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="22675-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="22675-185">Solo los administradores pueden registrar un proveedor de instancias mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ InstanceProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="22675-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="22675-186">Solo los administradores pueden eliminar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="22675-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="22675-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22675-187">Requirements</span></span>



| <span data-ttu-id="22675-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="22675-188">Requirement</span></span> | <span data-ttu-id="22675-189">Value</span><span class="sxs-lookup"><span data-stu-id="22675-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="22675-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22675-190">Minimum supported client</span></span><br/> | <span data-ttu-id="22675-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22675-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="22675-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22675-192">Minimum supported server</span></span><br/> | <span data-ttu-id="22675-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22675-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="22675-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22675-194">Namespace</span></span><br/>                | <span data-ttu-id="22675-195">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="22675-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="22675-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="22675-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22675-197">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="22675-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="22675-198">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="22675-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="22675-199">Registrar un proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="22675-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="22675-200">Registrar un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="22675-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

