---
description: La \_ clase CIM SoftwareFeature representa una función o funcionalidad determinada de un sistema de aplicaciones o productos.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: CIM_SoftwareFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659370"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="ab122-103">\_Clase SoftwareFeature de CIM</span><span class="sxs-lookup"><span data-stu-id="ab122-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="ab122-104">La clase **CIM \_ SoftwareFeature** representa una función o funcionalidad determinada de un sistema de aplicaciones o productos.</span><span class="sxs-lookup"><span data-stu-id="ab122-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="ab122-105">Esta clase refleja un nivel de granularidad que es significativo para un usuario de un producto en lugar de las unidades que reflejan cómo se compila o empaqueta el producto (capturado mediante una clase [**\_ SoftwareElement de CIM**](cim-softwareelement.md) ).</span><span class="sxs-lookup"><span data-stu-id="ab122-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="ab122-106">Cuando una característica de software puede existir en varias plataformas o sistemas operativos, la característica de software es una colección de los elementos de software para las distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="ab122-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="ab122-107">En ese caso, los usuarios del modelo estarán interesados normalmente en una subcolección de los elementos de software necesarios para una plataforma determinada.</span><span class="sxs-lookup"><span data-stu-id="ab122-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="ab122-108">Dado que las características se entregan a través de los productos, las características de software siempre se definen en el contexto de una clase de [**\_ producto CIM**](cim-product.md) mediante la Asociación [**\_ ProductSoftwareFeatures de CIM**](cim-productsoftwarefeatures.md) .</span><span class="sxs-lookup"><span data-stu-id="ab122-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="ab122-109">Opcionalmente, las características de software de uno o varios productos pueden organizarse en sistemas de aplicación mediante la Asociación [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="ab122-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab122-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ab122-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab122-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ab122-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab122-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ab122-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ab122-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ab122-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab122-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab122-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="ab122-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab122-115">Members</span></span>

<span data-ttu-id="ab122-116">La clase **CIM \_ SoftwareFeature** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab122-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="ab122-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab122-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab122-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab122-118">Properties</span></span>

<span data-ttu-id="ab122-119">La clase **CIM \_ SoftwareFeature** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab122-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab122-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ab122-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-123">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ab122-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-124">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ab122-124">Short textual description of the object.</span></span>

<span data-ttu-id="ab122-125">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab122-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab122-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-129">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="ab122-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-130">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ab122-130">Textual description of the object.</span></span>

<span data-ttu-id="ab122-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab122-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="ab122-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-135">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**IdentifyingNumber**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="ab122-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-136">Identificación del producto, como un número de serie en software o un número de matriz en un chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="ab122-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="ab122-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ab122-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab122-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="ab122-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-141">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="ab122-141">Date and time the object was installed.</span></span> <span data-ttu-id="ab122-142">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ab122-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ab122-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab122-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ab122-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-147">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ab122-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab122-148">Etiqueta por la que se conoce el objeto fuera del sistema de procesamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="ab122-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="ab122-149">La etiqueta es un nombre legible que identifica de forma única el elemento en el contexto del espacio de nombres del elemento.</span><span class="sxs-lookup"><span data-stu-id="ab122-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="ab122-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab122-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="ab122-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-154">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Name**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="ab122-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-155">Nombre de producto usado comúnmente.</span><span class="sxs-lookup"><span data-stu-id="ab122-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="ab122-156">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ab122-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-159">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ab122-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-160">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ab122-160">Current status of the object.</span></span>

<span data-ttu-id="ab122-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ab122-162">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab122-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ab122-163">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="ab122-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ab122-164">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="ab122-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ab122-165">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ab122-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ab122-166">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ab122-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ab122-167">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="ab122-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ab122-168">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="ab122-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ab122-169">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="ab122-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ab122-170">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="ab122-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ab122-171">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="ab122-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ab122-172">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ab122-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ab122-173">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="ab122-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ab122-174">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="ab122-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab122-175">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="ab122-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-178">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Vendor**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="ab122-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-179">Nombre del proveedor del producto, que corresponde a la propiedad **Vendor** en el objeto Product del estándar de intercambio de soluciones DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab122-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="ab122-180">**Versión**</span><span class="sxs-lookup"><span data-stu-id="ab122-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab122-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ab122-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab122-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab122-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab122-183">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Versión**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ab122-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ab122-184">Información de versión del producto, que corresponde a la propiedad **version** en el objeto Product del estándar de intercambio de soluciones DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab122-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab122-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab122-185">Remarks</span></span>

<span data-ttu-id="ab122-186">La clase **CIM \_ SoftwareFeature** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="ab122-187">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ab122-187">WMI does not implement this class.</span></span> <span data-ttu-id="ab122-188">Para las clases WMI derivadas de **CIM \_ SoftwareFeature**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ab122-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ab122-189">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab122-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab122-190">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ab122-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab122-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab122-191">Requirements</span></span>



| <span data-ttu-id="ab122-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab122-192">Requirement</span></span> | <span data-ttu-id="ab122-193">Value</span><span class="sxs-lookup"><span data-stu-id="ab122-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab122-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab122-194">Minimum supported client</span></span><br/> | <span data-ttu-id="ab122-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab122-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab122-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab122-196">Minimum supported server</span></span><br/> | <span data-ttu-id="ab122-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab122-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab122-198">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab122-198">Namespace</span></span><br/>                | <span data-ttu-id="ab122-199">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab122-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab122-200">MOF</span><span class="sxs-lookup"><span data-stu-id="ab122-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab122-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab122-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab122-202">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab122-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab122-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab122-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab122-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab122-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab122-205">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ab122-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

