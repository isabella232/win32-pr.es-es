---
description: Registra proveedores de clase en WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: __ClassProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
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
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818971"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="e826b-103">\_\_Clase ClassProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="e826b-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="e826b-104">La clase del sistema **\_ \_ ClassProviderRegistration** registra los proveedores de clases en WMI.</span><span class="sxs-lookup"><span data-stu-id="e826b-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="e826b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e826b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e826b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e826b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e826b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e826b-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="e826b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e826b-108">Members</span></span>

<span data-ttu-id="e826b-109">La clase **\_ \_ ClassProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e826b-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="e826b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e826b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e826b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e826b-111">Properties</span></span>

<span data-ttu-id="e826b-112">La clase **\_ \_ ClassProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e826b-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e826b-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="e826b-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-114">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e826b-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-117">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="e826b-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e826b-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-120">Indica si el proveedor de clase o instancia proporciona datos o si se basa en WMI y en el repositorio Modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="e826b-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="e826b-121">Los proveedores de extracción admiten el acceso dinámico a los datos, y los proveedores de inserción almacenan los datos en el repositorio CIM y se basan en WMI para proporcionar acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="e826b-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="e826b-122">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="e826b-122">The default value is 0 (zero).</span></span> <span data-ttu-id="e826b-123">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="e826b-124">Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="e826b-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Extracción** (0)</span><span class="sxs-lookup"><span data-stu-id="e826b-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-126">El proveedor es un proveedor de extracción.</span><span class="sxs-lookup"><span data-stu-id="e826b-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="e826b-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Inserte** (1)</span><span class="sxs-lookup"><span data-stu-id="e826b-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-128">El proveedor es un proveedor de inserciones.</span><span class="sxs-lookup"><span data-stu-id="e826b-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="e826b-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="e826b-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-130">El proveedor es un proveedor de comprobación de inserciones.</span><span class="sxs-lookup"><span data-stu-id="e826b-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="e826b-131">Tenga en cuenta que en este momento no se admiten los proveedores de **PushVerify** .</span><span class="sxs-lookup"><span data-stu-id="e826b-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-132">**PerUserSchema**</span><span class="sxs-lookup"><span data-stu-id="e826b-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-135">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-136">**presta**</span><span class="sxs-lookup"><span data-stu-id="e826b-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-137">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="e826b-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e826b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e826b-139">Ruta de acceso del objeto a un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="e826b-139">Object path to a class provider.</span></span> <span data-ttu-id="e826b-140">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="e826b-141">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="e826b-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-142">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e826b-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e826b-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-144">Matriz de los tipos de compatibilidad incluida en el proveedor para el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="e826b-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="e826b-145">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="e826b-146">Se requieren proveedores de clases para admitir al menos un tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="e826b-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="e826b-147">Los proveedores de instancias pueden establecer **QuerySupportLevels** en **null** si no admiten el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="e826b-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="e826b-148">Los proveedores que admiten consultas implementan el método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e826b-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="e826b-149">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="e826b-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e826b-150">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="e826b-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e826b-151">("WQL: Associatorsers")</span><span class="sxs-lookup"><span data-stu-id="e826b-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e826b-152">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="e826b-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-153">**ReferencedSetQueries**</span><span class="sxs-lookup"><span data-stu-id="e826b-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-154">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e826b-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e826b-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-156">Una o más consultas que describen el conjunto de clases a las que se hace referencia que admite un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="e826b-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="e826b-157">Los proveedores que pueden proporcionar clases de asociación deben incluir al menos una consulta en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e826b-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-158">**ResultSetQueries**</span><span class="sxs-lookup"><span data-stu-id="e826b-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-159">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e826b-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e826b-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-161">Una o más consultas que describen el conjunto de todas las clases que puede proporcionar el proveedor de clases o un superconjunto de esas clases.</span><span class="sxs-lookup"><span data-stu-id="e826b-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="e826b-162">Esta propiedad nunca especifica un subconjunto de clases admitidas.</span><span class="sxs-lookup"><span data-stu-id="e826b-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-163">**ReSynchroniseOnNamespaceOpen**</span><span class="sxs-lookup"><span data-stu-id="e826b-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-164">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-166">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-167">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="e826b-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-170">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-170">Not used.</span></span>

<span data-ttu-id="e826b-171">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="e826b-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="e826b-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-173">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-175">Si **es true**, el proveedor admite la eliminación de datos.</span><span class="sxs-lookup"><span data-stu-id="e826b-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="e826b-176">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="e826b-177">Reales</span><span class="sxs-lookup"><span data-stu-id="e826b-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-178">El proveedor admite la eliminación de la clase o la instancia implementando uno de los [**eleteclassasync de IWbemServices::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="e826b-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="e826b-179">Es</span><span class="sxs-lookup"><span data-stu-id="e826b-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-180">El proveedor no admite la eliminación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="e826b-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-181">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="e826b-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-182">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-184">Si **es true**, el proveedor admite la enumeración de datos.</span><span class="sxs-lookup"><span data-stu-id="e826b-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="e826b-185">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="e826b-186">Reales</span><span class="sxs-lookup"><span data-stu-id="e826b-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-187">El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (clase) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="e826b-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="e826b-188">Es</span><span class="sxs-lookup"><span data-stu-id="e826b-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-189">El proveedor no admite la enumeración de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="e826b-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-190">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="e826b-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-191">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-193">Si **es true**, el proveedor de la clase o la instancia admite la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="e826b-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="e826b-194">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="e826b-195">Reales</span><span class="sxs-lookup"><span data-stu-id="e826b-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-196">El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="e826b-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="e826b-197">Es</span><span class="sxs-lookup"><span data-stu-id="e826b-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-198">El proveedor no admite la recuperación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ compatible** con [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="e826b-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-199">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="e826b-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-200">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-201">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-202">Si **es true**, el proveedor de clase o instancia admite la modificación de datos.</span><span class="sxs-lookup"><span data-stu-id="e826b-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="e826b-203">Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="e826b-204">Reales</span><span class="sxs-lookup"><span data-stu-id="e826b-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-205">El proveedor admite la modificación de la clase o la instancia implementando uno de los [**utclassasync de IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).</span><span class="sxs-lookup"><span data-stu-id="e826b-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="e826b-206">Es</span><span class="sxs-lookup"><span data-stu-id="e826b-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="e826b-207">El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="e826b-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e826b-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="e826b-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-209">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-210">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-211">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-212">**SuppportsBatching**</span><span class="sxs-lookup"><span data-stu-id="e826b-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-213">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e826b-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-215">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e826b-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-216">**UnsupportedQueries**</span><span class="sxs-lookup"><span data-stu-id="e826b-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-217">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e826b-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e826b-218">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-219">Una o más consultas que describen el conjunto de clases que no admite el proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="e826b-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="e826b-220">Utilice esta propiedad para restar del conjunto de clases implícitas por **ResultSetQueries**.</span><span class="sxs-lookup"><span data-stu-id="e826b-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="e826b-221">**Versión**</span><span class="sxs-lookup"><span data-stu-id="e826b-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e826b-222">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e826b-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e826b-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e826b-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e826b-224">Versión de este proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="e826b-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e826b-225">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e826b-225">Remarks</span></span>

<span data-ttu-id="e826b-226">La clase **\_ \_ ClassProviderRegistration** se deriva de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="e826b-227">Las propiedades heredadas de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indican si el proveedor de clases admite o no la recuperación de datos, la modificación, la eliminación, la enumeración y el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="e826b-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="e826b-228">La propiedad **InteractionType** especifica si el proveedor de clases está diseñado como un proveedor de extracción o de inserción.</span><span class="sxs-lookup"><span data-stu-id="e826b-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="e826b-229">Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="e826b-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="e826b-230">La clase [**\_ \_ ProviderRegistration**](--providerregistration.md) define la propiedad del [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="e826b-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="e826b-231">Solo los administradores pueden registrar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ ClassProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="e826b-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="e826b-232">Solo los administradores pueden eliminar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="e826b-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="e826b-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e826b-233">Requirements</span></span>



| <span data-ttu-id="e826b-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="e826b-234">Requirement</span></span> | <span data-ttu-id="e826b-235">Value</span><span class="sxs-lookup"><span data-stu-id="e826b-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e826b-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e826b-236">Minimum supported client</span></span><br/> | <span data-ttu-id="e826b-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e826b-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e826b-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e826b-238">Minimum supported server</span></span><br/> | <span data-ttu-id="e826b-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e826b-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e826b-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e826b-240">Namespace</span></span><br/>                | <span data-ttu-id="e826b-241">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="e826b-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e826b-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="e826b-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e826b-243">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="e826b-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="e826b-244">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="e826b-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e826b-245">Registrar un proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="e826b-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="e826b-246">Registrar un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="e826b-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="e826b-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="e826b-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

