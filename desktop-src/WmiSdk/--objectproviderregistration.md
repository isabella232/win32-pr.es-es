---
description: Actúa como clase primaria para las clases que se utilizan para registrar proveedores de clases y de instancias en WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: __ObjectProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360779"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="d1824-103">\_\_Clase ObjectProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="d1824-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="d1824-104">La clase de sistema abstracta **\_ \_ ObjectProviderRegistration** actúa como clase primaria para las clases que se usan para registrar proveedores de clases y de instancias en WMI.</span><span class="sxs-lookup"><span data-stu-id="d1824-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="d1824-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d1824-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1824-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d1824-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1824-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1824-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="d1824-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1824-108">Members</span></span>

<span data-ttu-id="d1824-109">La clase **\_ \_ ObjectProviderRegistration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1824-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="d1824-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1824-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1824-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1824-111">Properties</span></span>

<span data-ttu-id="d1824-112">La clase **\_ \_ ObjectProviderRegistration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1824-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1824-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="d1824-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-114">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d1824-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-116">Indica si el proveedor de clase o instancia proporciona sus propios datos o si se basa en WMI y en el repositorio Modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="d1824-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="d1824-117">Los proveedores de extracción admiten el acceso dinámico a sus datos, y los proveedores de inserción almacenan sus datos en el repositorio CIM y dependen de WMI para proporcionar acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="d1824-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="d1824-118">Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="d1824-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="d1824-119">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d1824-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="d1824-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Extracción** (0)</span><span class="sxs-lookup"><span data-stu-id="d1824-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d1824-121">El proveedor es un proveedor de extracción.</span><span class="sxs-lookup"><span data-stu-id="d1824-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="d1824-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Inserte** (1)</span><span class="sxs-lookup"><span data-stu-id="d1824-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1824-123">El proveedor es un proveedor de inserciones.</span><span class="sxs-lookup"><span data-stu-id="d1824-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="d1824-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="d1824-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1824-125">El proveedor es un proveedor de comprobación de inserciones.</span><span class="sxs-lookup"><span data-stu-id="d1824-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="d1824-126">Tenga en cuenta que en este momento no se admite la comprobación de inserciones.</span><span class="sxs-lookup"><span data-stu-id="d1824-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1824-127">**presta**</span><span class="sxs-lookup"><span data-stu-id="d1824-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-128">Tipo de datos: **\_ \_ proveedor**</span><span class="sxs-lookup"><span data-stu-id="d1824-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1824-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1824-130">Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa una ruta de acceso de objeto al proveedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d1824-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="d1824-131">Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="d1824-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1824-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="d1824-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d1824-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1824-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-135">Matriz de los tipos de compatibilidad incluida en el proveedor para el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="d1824-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="d1824-136">Los proveedores de clases no admiten ningún tipo de consultas.</span><span class="sxs-lookup"><span data-stu-id="d1824-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="d1824-137">Los proveedores de instancias pueden establecer **QuerySupportLevels** en **null** si no admiten el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="d1824-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="d1824-138">Los proveedores que admiten consultas implementan el método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes (el tipo de propiedad es una matriz).</span><span class="sxs-lookup"><span data-stu-id="d1824-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="d1824-139">"WQL: UnarySelect"</span><span class="sxs-lookup"><span data-stu-id="d1824-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="d1824-140">"WQL: References"</span><span class="sxs-lookup"><span data-stu-id="d1824-140">"WQL:References"</span></span>

<span data-ttu-id="d1824-141">"WQL: Associatorsrs"</span><span class="sxs-lookup"><span data-stu-id="d1824-141">"WQL:Associators"</span></span>

<span data-ttu-id="d1824-142">"WQL: V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="d1824-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="d1824-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="d1824-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d1824-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1824-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="d1824-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-150">Si **es true**, el proveedor admite la eliminación de datos.</span><span class="sxs-lookup"><span data-stu-id="d1824-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="d1824-151">True</span><span class="sxs-lookup"><span data-stu-id="d1824-151">True</span></span>
</dt> <dd>

<span data-ttu-id="d1824-152">El proveedor admite la eliminación de la clase o la instancia implementando uno de los [**eleteclassasync de IWbemServices::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="d1824-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1824-153">False</span><span class="sxs-lookup"><span data-stu-id="d1824-153">False</span></span>
</dt> <dd>

<span data-ttu-id="d1824-154">El proveedor no admite la eliminación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="d1824-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1824-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="d1824-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-156">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-158">Si **es true**, el proveedor admite la enumeración de datos.</span><span class="sxs-lookup"><span data-stu-id="d1824-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="d1824-159">True</span><span class="sxs-lookup"><span data-stu-id="d1824-159">True</span></span>
</dt> <dd>

<span data-ttu-id="d1824-160">El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (clase) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).</span><span class="sxs-lookup"><span data-stu-id="d1824-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1824-161">False</span><span class="sxs-lookup"><span data-stu-id="d1824-161">False</span></span>
</dt> <dd>

<span data-ttu-id="d1824-162">El proveedor no admite la enumeración de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="d1824-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1824-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="d1824-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-164">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-166">Si **es true**, el proveedor de la clase o la instancia admite la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="d1824-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="d1824-167">True</span><span class="sxs-lookup"><span data-stu-id="d1824-167">True</span></span>
</dt> <dd>

<span data-ttu-id="d1824-168">El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="d1824-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="d1824-169">False</span><span class="sxs-lookup"><span data-stu-id="d1824-169">False</span></span>
</dt> <dd>

<span data-ttu-id="d1824-170">El proveedor no admite la recuperación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ compatible** con [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="d1824-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1824-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="d1824-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-174">Si **es true**, el proveedor de clase o instancia admite la modificación de datos.</span><span class="sxs-lookup"><span data-stu-id="d1824-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="d1824-175">True</span><span class="sxs-lookup"><span data-stu-id="d1824-175">True</span></span>
</dt> <dd>

<span data-ttu-id="d1824-176">El proveedor admite la modificación de la clase o la instancia implementando uno de los [**utclassasync de IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).</span><span class="sxs-lookup"><span data-stu-id="d1824-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="d1824-177">False</span><span class="sxs-lookup"><span data-stu-id="d1824-177">False</span></span>
</dt> <dd>

<span data-ttu-id="d1824-178">El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="d1824-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1824-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="d1824-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1824-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1824-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1824-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1824-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1824-182">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d1824-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1824-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1824-183">Remarks</span></span>

<span data-ttu-id="d1824-184">La clase **\_ \_ ObjectProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="d1824-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="d1824-185">Los proveedores de clases deben establecer la propiedad **SupportsEnumeration** en **true** , ya que los proveedores deben ser capaces de proporcionar a WMI una lista de sus clases.</span><span class="sxs-lookup"><span data-stu-id="d1824-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="d1824-186">Si un proveedor de clases intenta establecer esta propiedad en **false**, WMI marca el registro como no válido.</span><span class="sxs-lookup"><span data-stu-id="d1824-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="d1824-187">No es necesario que los proveedores de instancias admitan la enumeración y puede elegir establecer **SupportsEnumeration** en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="d1824-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="d1824-188">Un proveedor que establece **QuerySupportLevels** en "WQL: UnarySelect" puede aceptar una consulta que consta de la instrucción SELECT básica, tal como se admite en la versión 1,0 de WMI.</span><span class="sxs-lookup"><span data-stu-id="d1824-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="d1824-189">Se espera que los proveedores de clase y de instancia puedan controlar la propiedad del sistema de **\_ \_ clase** .</span><span class="sxs-lookup"><span data-stu-id="d1824-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="d1824-190">También se espera que los proveedores de clases procesen la propiedad del sistema de la **\_ \_ superclase** y el operador ISA.</span><span class="sxs-lookup"><span data-stu-id="d1824-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="d1824-191">El operador ISA se usa para expandir un conjunto de resultados a clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="d1824-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="d1824-192">Si a un proveedor se le proporciona una consulta que no puede interpretar, solicita que WMI lo controle devolviendo el valor de error de **WBEM \_ E \_ demasiado \_ complejo** .</span><span class="sxs-lookup"><span data-stu-id="d1824-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="d1824-193">Para obtener una descripción de la sintaxis válida de WQL, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="d1824-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="d1824-194">Un proveedor que establece **QuerySupportLevels** en **WQL: V1ProviderDefined** puede intentar admitir un conjunto mayor de sintaxis SQL bajo su propio riesgo, como la `ORDER BY` cláusula.</span><span class="sxs-lookup"><span data-stu-id="d1824-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="d1824-195">WMI no interpreta las cláusulas adicionales o intenta asegurarse de que el conjunto de resultados es correcto.</span><span class="sxs-lookup"><span data-stu-id="d1824-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="d1824-196">Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y su registro.</span><span class="sxs-lookup"><span data-stu-id="d1824-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1824-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1824-197">Requirements</span></span>



| <span data-ttu-id="d1824-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1824-198">Requirement</span></span> | <span data-ttu-id="d1824-199">Value</span><span class="sxs-lookup"><span data-stu-id="d1824-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d1824-200">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1824-200">Minimum supported client</span></span><br/> | <span data-ttu-id="d1824-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1824-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d1824-202">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1824-202">Minimum supported server</span></span><br/> | <span data-ttu-id="d1824-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1824-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d1824-204">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1824-204">Namespace</span></span><br/>                | <span data-ttu-id="d1824-205">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="d1824-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d1824-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1824-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1824-207">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d1824-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="d1824-208">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d1824-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d1824-209">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="d1824-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

