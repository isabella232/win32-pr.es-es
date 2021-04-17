---
description: Proporciona reglas para asignar clases WMI a Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Asignar Active Directory clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716431"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="cc7af-103">Asignar Active Directory clases</span><span class="sxs-lookup"><span data-stu-id="cc7af-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="cc7af-104">Dado que Active Directory tiene una amplia variedad de objetos posibles, WMI no puede crear una asignación unívoca directa.</span><span class="sxs-lookup"><span data-stu-id="cc7af-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="cc7af-105">En su lugar, el proveedor de servicios de directorio utiliza reglas para asignar clases entre las dos tecnologías.</span><span class="sxs-lookup"><span data-stu-id="cc7af-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="cc7af-106">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="cc7af-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="cc7af-107">Clases de asignación</span><span class="sxs-lookup"><span data-stu-id="cc7af-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="cc7af-108">Atributos de asignación</span><span class="sxs-lookup"><span data-stu-id="cc7af-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="cc7af-109">Clases de asociación</span><span class="sxs-lookup"><span data-stu-id="cc7af-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="cc7af-110">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="cc7af-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="cc7af-111">Clases de asignación</span><span class="sxs-lookup"><span data-stu-id="cc7af-111">Mapping Classes</span></span>

<span data-ttu-id="cc7af-112">En la lista siguiente se describen las instrucciones que usa el proveedor de servicios de directorio para asignar Active Directory clases a clases WMI:</span><span class="sxs-lookup"><span data-stu-id="cc7af-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="cc7af-113">Cada clase abstracta del esquema de Active Directory se asigna a una clase abstracta en el esquema de WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="cc7af-114">En el esquema de WMI, cada clase abstracta tiene el prefijo DS \_ .</span><span class="sxs-lookup"><span data-stu-id="cc7af-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="cc7af-115">Por ejemplo, la clase **Person** del esquema Active Directory se asigna a la clase WMI **\_ Person de DS** .</span><span class="sxs-lookup"><span data-stu-id="cc7af-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="cc7af-116">Cada clase no abstracta del esquema de Active Directory se asigna a las dos clases siguientes en el esquema de WMI:</span><span class="sxs-lookup"><span data-stu-id="cc7af-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="cc7af-117">La primera clase asignada tiene como prefijo ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="cc7af-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="cc7af-118">Se trata de clases abstractas asignadas según las reglas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc7af-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="cc7af-119">La segunda clase asignada es una clase no abstracta con el \_ Prefijo de nombre de DS.</span><span class="sxs-lookup"><span data-stu-id="cc7af-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="cc7af-120">Esta clase se deriva de la \_ clase abstracta ADS, con la adición del calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="cc7af-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="cc7af-121">Por ejemplo, la clase de **usuario** de la Active Directory esquema se asigna a dos clases.</span><span class="sxs-lookup"><span data-stu-id="cc7af-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="cc7af-122">La primera clase es la clase abstracta de **\_ usuario ADS** , asignada según las reglas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc7af-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="cc7af-123">La segunda clase es la clase no abstracta **\_ usuario de DS** .</span><span class="sxs-lookup"><span data-stu-id="cc7af-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="cc7af-124">Se deriva del **\_ usuario ADS** y tiene el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) agregado.</span><span class="sxs-lookup"><span data-stu-id="cc7af-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="cc7af-125">A menos que se especifique lo contrario, el nombre de una clase asignada es el valor alterado de la propiedad **LDAP-Display-Name** en la clase Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc7af-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="cc7af-126">Si la **subclase de** la propiedad está presente en la clase Active Directory, la clase asignada por WMI se deriva de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="cc7af-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="cc7af-127">Si no está presente la **subclase de** la propiedad, la clase asignada por WMI se deriva de la clase de **\_ \_ \_ clase raíz DS LDAP** , tal y como se especifica en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="cc7af-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="cc7af-128">Esta clase tiene la propiedad clave **ADSIPath** , con un tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="cc7af-129">Esta es la ruta de acceso ADSI única que identifica esta instancia.</span><span class="sxs-lookup"><span data-stu-id="cc7af-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="cc7af-130">Active Directory solo admite la herencia única, por lo que funciona.</span><span class="sxs-lookup"><span data-stu-id="cc7af-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="cc7af-131">Se crea un calificador **dinámico** de tipo **VT \_ bool** y Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` establecido en **true** para cada clase.</span><span class="sxs-lookup"><span data-stu-id="cc7af-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="cc7af-132">Se trata de un calificador WMI estándar que indica que las instancias de esta clase se proporcionan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="cc7af-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="cc7af-133">Si la clase no es abstracta, el proveedor crea un calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) de tipo **VT \_ BSTR bool** y el tipo de calificador `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` establecido en "proveedor de instancia de DS" para cada clase.</span><span class="sxs-lookup"><span data-stu-id="cc7af-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="cc7af-134">Se trata de un calificador WMI estándar que indica el nombre del proveedor que proporciona de forma dinámica las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="cc7af-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="cc7af-135">El resto de las propiedades ADSI se asignan a los calificadores y propiedades de clase según las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc7af-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="cc7af-136">Todos los calificadores se asignan con un valor de marca de calificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="cc7af-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="cc7af-137">A continuación se enumera la información de asignación de la clase Active Directory, que muestra el calificador WMI y el tipo de calificador WMI para cada propiedad Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc7af-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="cc7af-138">**Nombre común**</span><span class="sxs-lookup"><span data-stu-id="cc7af-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="cc7af-140">Se asigna directamente desde el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="cc7af-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-141">**Default-Object-Category**</span><span class="sxs-lookup"><span data-stu-id="cc7af-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-142">**DefaultObjectCategory** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="cc7af-143">Se asigna directamente desde el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="cc7af-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-144">**Default-Security-Descriptor**</span><span class="sxs-lookup"><span data-stu-id="cc7af-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="cc7af-146">Se asigna directamente desde el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="cc7af-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-147">**Controla el identificador**</span><span class="sxs-lookup"><span data-stu-id="cc7af-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="cc7af-149">Asignada a partir de la representación de cadena del OID; por ejemplo, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="cc7af-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-150">**Clase de objeto**</span><span class="sxs-lookup"><span data-stu-id="cc7af-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-151">N/D</span><span class="sxs-lookup"><span data-stu-id="cc7af-151">N/A</span></span>

<span data-ttu-id="cc7af-152">No asignado.</span><span class="sxs-lookup"><span data-stu-id="cc7af-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-153">**Objeto-clase-categoría**</span><span class="sxs-lookup"><span data-stu-id="cc7af-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-154">**ObjectClassCategory** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="cc7af-155">Se asigna directamente desde el valor entero.</span><span class="sxs-lookup"><span data-stu-id="cc7af-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="cc7af-156">Además, si el valor es abstracto (2), también se crea el calificador de CIM de **VT \_** estándar, denominado calificador **"abstracto"** .</span><span class="sxs-lookup"><span data-stu-id="cc7af-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="cc7af-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-158">**RDNATTID** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="cc7af-159">Asignada a partir de la representación de cadena del valor de OID; por ejemplo, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="cc7af-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="cc7af-160">Además, la propiedad identificada aquí se anota con el calificador de CIM **indexado** estándar establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-161">**Solo del sistema**</span><span class="sxs-lookup"><span data-stu-id="cc7af-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-162">**SystemOnly** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="cc7af-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="cc7af-163">Se asigna directamente desde el valor booleano.</span><span class="sxs-lookup"><span data-stu-id="cc7af-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="cc7af-164">A continuación se enumeran las propiedades de clase de Active Directory asignadas a las propiedades de clase WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc7af-165">**Puede contener**</span><span class="sxs-lookup"><span data-stu-id="cc7af-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-166">Cada propiedad de esta lista se asigna a una propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-167">**Debe contener**</span><span class="sxs-lookup"><span data-stu-id="cc7af-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-168">Cada propiedad de esta lista se asigna a una propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="cc7af-169">Se crea el calificador de CIM estándar **not \_ null** para cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="cc7af-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-170">**Sistema: puede contener**</span><span class="sxs-lookup"><span data-stu-id="cc7af-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-171">Cada propiedad de esta lista se asigna a una propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="cc7af-172">Además, cada propiedad se anota con un calificador **del sistema** , establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="cc7af-173">**Sistema: debe contener**</span><span class="sxs-lookup"><span data-stu-id="cc7af-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="cc7af-174">Cada propiedad de esta lista se asigna a una propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="cc7af-175">Se crea el calificador de CIM estándar **not \_ null** para cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="cc7af-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="cc7af-176">Además, cada propiedad se anota con un calificador **del sistema** , establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="cc7af-177">Atributos de asignación</span><span class="sxs-lookup"><span data-stu-id="cc7af-177">Mapping Attributes</span></span>

<span data-ttu-id="cc7af-178">El proveedor de servicios de directorio asigna cada atributo de una clase Active Directory a exactamente una propiedad de la clase WMI correspondiente según las reglas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="cc7af-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="cc7af-179">En general, el proveedor de servicios de directorio denomina la propiedad WMI como la versión alterada del valor **LDAP-Display-Name** del atributo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc7af-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="cc7af-180">Si la propiedad Active Directory **tiene el valor** **false**, esta propiedad WMI se combina con el operador OR con una **\_ \_ matriz de marca CIM**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="cc7af-181">Tenga en cuenta que cada propiedad se etiqueta con el calificador **\_ BSTR de VT** , **ADSyntax**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="cc7af-182">Representa la sintaxis de Active Directory subyacente.</span><span class="sxs-lookup"><span data-stu-id="cc7af-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="cc7af-183">En la tabla siguiente se muestra la asignación de la sintaxis de Active Directory al tipo de datos de la propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="cc7af-184">Elemento Active Directory</span><span class="sxs-lookup"><span data-stu-id="cc7af-184">Active Directory element</span></span>                                      | <span data-ttu-id="cc7af-185">Tipo de datos WMI</span><span class="sxs-lookup"><span data-stu-id="cc7af-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="cc7af-186">**Punto de acceso**</span><span class="sxs-lookup"><span data-stu-id="cc7af-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="cc7af-187">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="cc7af-188">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="cc7af-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="cc7af-189">**\_BOOLEANO CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="cc7af-190">**Cadena sin distinción entre mayúsculas y minúsculas**</span><span class="sxs-lookup"><span data-stu-id="cc7af-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="cc7af-191">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="cc7af-192">**Cadena que distingue mayúsculas de minúsculas**</span><span class="sxs-lookup"><span data-stu-id="cc7af-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="cc7af-193">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="cc7af-194">**Nombre distintivo**</span><span class="sxs-lookup"><span data-stu-id="cc7af-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="cc7af-195">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="cc7af-196">**DN: binario**</span><span class="sxs-lookup"><span data-stu-id="cc7af-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="cc7af-197">Objeto incrustado de la clase **DN \_ con el \_ binario** definido a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="cc7af-198">**Cadena DN**</span><span class="sxs-lookup"><span data-stu-id="cc7af-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="cc7af-199">Objeto incrustado de la clase **DN \_ con la \_ cadena** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="cc7af-200">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="cc7af-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="cc7af-201">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="cc7af-202">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="cc7af-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="cc7af-203">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="cc7af-204">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc7af-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="cc7af-205">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="cc7af-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="cc7af-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="cc7af-207">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="cc7af-208">Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="cc7af-208">Security Descriptor</span></span>                                           | <span data-ttu-id="cc7af-209">Objeto incrustado de la clase **, uint8array** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="cc7af-210">Cadena numérica</span><span class="sxs-lookup"><span data-stu-id="cc7af-210">Numeric String</span></span>                                                | <span data-ttu-id="cc7af-211">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="cc7af-212">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="cc7af-212">Object ID</span></span>                                                     | <span data-ttu-id="cc7af-213">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="cc7af-214">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="cc7af-214">Octet String</span></span>                                                  | <span data-ttu-id="cc7af-215">Objeto incrustado de la clase **, uint8array** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="cc7af-216">O nombre</span><span class="sxs-lookup"><span data-stu-id="cc7af-216">OR Name</span></span>                                                       | <span data-ttu-id="cc7af-217">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="cc7af-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="cc7af-218">Presentation-Address</span></span>                                          | <span data-ttu-id="cc7af-219">Objeto incrustado de la clase **, uint8array** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="cc7af-220">Cadena de caso de impresión</span><span class="sxs-lookup"><span data-stu-id="cc7af-220">Print Case String</span></span>                                             | <span data-ttu-id="cc7af-221">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="cc7af-222">Vínculo de réplica</span><span class="sxs-lookup"><span data-stu-id="cc7af-222">Replica Link</span></span>                                                  | <span data-ttu-id="cc7af-223">Objeto incrustado de la clase **, uint8array** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="cc7af-224">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="cc7af-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="cc7af-225">Objeto incrustado de la clase **, uint8array** que se define a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc7af-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="cc7af-226">Hora</span><span class="sxs-lookup"><span data-stu-id="cc7af-226">Time</span></span>                                                          | <span data-ttu-id="cc7af-227">**\_fecha y hora de CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="cc7af-228">Hora codificada UTC</span><span class="sxs-lookup"><span data-stu-id="cc7af-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="cc7af-229">**\_fecha y hora de CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="cc7af-230">Cadena Unicode</span><span class="sxs-lookup"><span data-stu-id="cc7af-230">Unicode String</span></span>                                                | <span data-ttu-id="cc7af-231">**\_cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="cc7af-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="cc7af-232">La sintaxis de la cadena de octetos, que hace referencia a una matriz de valores **Uint8** , presenta un problema cuando se asigna a WMI porque WMI permite propiedades de tipos **Uint8** y matrices de **Uint8**, mientras que Active Directory permite propiedades de tipo cadena de octetos, así como matrices de cadenas de octetos.</span><span class="sxs-lookup"><span data-stu-id="cc7af-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="cc7af-233">En el ejemplo siguiente se muestra la clase de proveedor de servicios de directorio que se usa para asignar una matriz de propiedades de tipo de cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="cc7af-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="cc7af-234">WMI asigna todas las cadenas de octetos Active Directory valores de propiedad a las instancias incrustadas de **, uint8array**.</span><span class="sxs-lookup"><span data-stu-id="cc7af-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="cc7af-235">Del mismo modo, WMI asigna matrices de cadenas de octetos a matrices de objetos **, uint8array** insertados.</span><span class="sxs-lookup"><span data-stu-id="cc7af-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="cc7af-236">En el ejemplo siguiente se muestran las clases asignadas por WMI para DN-Binary y DN-String los valores de propiedad de DS.</span><span class="sxs-lookup"><span data-stu-id="cc7af-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="cc7af-237">En la tabla siguiente se muestra cómo asigna WMI el resto de las propiedades de la interfaz de atributo de Active Directory a los calificadores de propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="cc7af-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="cc7af-238">Active Directory nombre de propiedad de atributo</span><span class="sxs-lookup"><span data-stu-id="cc7af-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="cc7af-239">Calificador de WMI</span><span class="sxs-lookup"><span data-stu-id="cc7af-239">WMI Qualifier</span></span>       | <span data-ttu-id="cc7af-240">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cc7af-240">Data type</span></span>    | <span data-ttu-id="cc7af-241">Información de asignación</span><span class="sxs-lookup"><span data-stu-id="cc7af-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="cc7af-242">**Sintaxis de atributo**</span><span class="sxs-lookup"><span data-stu-id="cc7af-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="cc7af-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="cc7af-243">**AttributeSyntax**</span></span> | <span data-ttu-id="cc7af-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="cc7af-244">**VT\_BSTR**</span></span> | <span data-ttu-id="cc7af-245">Asignada a partir de la representación de cadena del OID.</span><span class="sxs-lookup"><span data-stu-id="cc7af-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="cc7af-246">**Nombre común**</span><span class="sxs-lookup"><span data-stu-id="cc7af-246">**Common-Name**</span></span>                          | <span data-ttu-id="cc7af-247">**CN**</span><span class="sxs-lookup"><span data-stu-id="cc7af-247">**CN**</span></span>              | <span data-ttu-id="cc7af-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="cc7af-248">**VT\_BSTR**</span></span> | <span data-ttu-id="cc7af-249">Asignado desde el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="cc7af-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="cc7af-250">**Solo del sistema**</span><span class="sxs-lookup"><span data-stu-id="cc7af-250">**System-Only**</span></span>                          | <span data-ttu-id="cc7af-251">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="cc7af-251">**System**</span></span>          | <span data-ttu-id="cc7af-252">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cc7af-252">**VT\_BOOL**</span></span> | <span data-ttu-id="cc7af-253">Asignado desde el valor booleano.</span><span class="sxs-lookup"><span data-stu-id="cc7af-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="cc7af-254">WMI asigna todos los calificadores de Active Directory con los `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` tipos de calificador.</span><span class="sxs-lookup"><span data-stu-id="cc7af-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="cc7af-255">Clases de asociación</span><span class="sxs-lookup"><span data-stu-id="cc7af-255">Association Classes</span></span>

<span data-ttu-id="cc7af-256">El servicio de directorio es esencialmente un almacén jerárquico de objetos.</span><span class="sxs-lookup"><span data-stu-id="cc7af-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="cc7af-257">Los objetos que pueden aparecer en un nivel no hoja en la jerarquía se denominan "contenedores".</span><span class="sxs-lookup"><span data-stu-id="cc7af-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="cc7af-258">La estructura de esta jerarquía se controla más en las propiedades "Poss-superior" y "System-Poss-superior" de una clase en el esquema.</span><span class="sxs-lookup"><span data-stu-id="cc7af-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="cc7af-259">En conjunto, se especifica el conjunto de clases cuyas instancias pueden estar contenidas en una instancia de una clase contenedora.</span><span class="sxs-lookup"><span data-stu-id="cc7af-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="cc7af-260">En el ejemplo siguiente se modela una asociación CIM como instancias de la clase de asociación estática [**\_ \_ \_ contención de clase LDAP de DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span><span class="sxs-lookup"><span data-stu-id="cc7af-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="cc7af-261">El proveedor de clases de asociación admite los métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) y [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="cc7af-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

