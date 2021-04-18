---
description: A continuación se enumeran los calificadores estándar específicos de WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Calificadores WMI estándar
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706650"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="3f3d6-103">Calificadores WMI estándar</span><span class="sxs-lookup"><span data-stu-id="3f3d6-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="3f3d6-104">A continuación se enumeran los calificadores estándar específicos de WMI.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="3f3d6-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Corrección**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-106">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-106">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-107">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-107">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-108">Indica que una clase contiene calificadores corregidos que están localizados.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="3f3d6-109">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-109">The default is **TRUE**.</span></span>

<span data-ttu-id="3f3d6-110">La clase asociada se puede traducir.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-110">The associated class can be translated.</span></span> <span data-ttu-id="3f3d6-111">Para tener acceso a la versión traducida, use el identificador de configuración regional para construir un nombre de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Omitir \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-113">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-114">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="3f3d6-114">Applies to: methods</span></span>

<span data-ttu-id="3f3d6-115">Indica que la llamada al método debe pasar directamente a la llamada **ExecMethodAsync** del proveedor en lugar de que el proveedor realice primero una llamada a **GetObject** para validar la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="3f3d6-116">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-116">The default is **FALSE**.</span></span> <span data-ttu-id="3f3d6-117">El uso de **bypass \_ GetObject** puede mejorar significativamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="3f3d6-118">Antes de usar **bypass \_ GetObject**, asegúrese de que no se realiza ninguna de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="3f3d6-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="3f3d6-119">Derive una clase de la clase.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="3f3d6-120">Invalide el método que tiene el calificador **\_ GetObject bypass** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="3f3d6-121">Si no se siguen estas precauciones, se puede invocar la implementación del método de la clase primaria en lugar de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="3f3d6-122">Para obtener más información, vea usar el \_ calificador de omisión de GetObject.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Clave CIM**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-124">Tipo de datos: **CIM \_ booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="3f3d6-125">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-125">Applies to: properties</span></span>

<span data-ttu-id="3f3d6-126">Indica que la propiedad asociada es una propiedad clave en CIM pero no en WMI.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-128">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-129">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3d6-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="3f3d6-130">Contiene el texto que describe el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-132">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-133">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-133">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-134">Indica que una clase tiene instancias asociadas a más información de forma dinámica y proporcionada por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**En desuso**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-136">Tipo de datos: **CIM \_ booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="3f3d6-137">Se aplica a: propiedades, clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-137">Applies to: properties, classes</span></span>

<span data-ttu-id="3f3d6-138">Indica que la propiedad ha sido reemplazada por otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Muestra**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-140">Se aplica a: clases, propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-140">Applies to: classes, properties</span></span>

<span data-ttu-id="3f3d6-141">**UUID** de la clase asociada.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinámica**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-143">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-144">Se aplica a: clases, propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-144">Applies to: classes, properties</span></span>

<span data-ttu-id="3f3d6-145">Indica una clase cuyas instancias se crean dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="3f3d6-146">El valor de este calificador debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-148">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-149">Se aplica a: clases, instancias</span><span class="sxs-lookup"><span data-stu-id="3f3d6-149">Applies to: classes, instances</span></span>

<span data-ttu-id="3f3d6-150">Indica que una instancia contiene los valores proporcionados por los proveedores de propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="3f3d6-151">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-151">The default is **TRUE**.</span></span>

<span data-ttu-id="3f3d6-152">Debe especificar este calificador en una instancia de este tipo.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="3f3d6-153">Solo se permite el valor **true** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Resuelto**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-155">Tipo de datos: **CIM \_ booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="3f3d6-156">Se aplica a: instancias</span><span class="sxs-lookup"><span data-stu-id="3f3d6-156">Applies to: instances</span></span>

<span data-ttu-id="3f3d6-157">Indica que el valor de esta propiedad no puede cambiar durante la duración de la instancia.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-158"><span id="ID"></span><span id="id"></span>**SESIÓN**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-159">Tipo de datos: **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="3f3d6-160">Se aplica a: propiedades, parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3d6-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="3f3d6-161">Identifica y secuencia de forma única un parámetro de propiedad o de método cuando se generan automáticamente instrucciones de MOF.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="3f3d6-162">Este calificador solo es necesario para los parámetros de método.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="3f3d6-163">Al crear parámetros para un método, los diseñadores de clases deben comenzar con el identificador (0) para el primer parámetro y usar cada entero sucesivo para cada parámetro sucesivo.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="3f3d6-164">Si los calificadores de **identificador** se omiten involuntariamente, el compilador MOF genera automáticamente calificadores de **identificador** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Ha**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-166">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-166">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-167">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="3f3d6-167">Applies to: methods</span></span>

<span data-ttu-id="3f3d6-168">Indica que un método tiene una implementación proporcionada por un proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-170">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-171">Se aplica a: instancias</span><span class="sxs-lookup"><span data-stu-id="3f3d6-171">Applies to: instances</span></span>

<span data-ttu-id="3f3d6-172">Indica que una instancia contiene los valores proporcionados por un proveedor de propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="3f3d6-173">El valor se pasa al proveedor de propiedades como argumento al método [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-175">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-176">Se aplica a: clases o instancias</span><span class="sxs-lookup"><span data-stu-id="3f3d6-176">Applies to: classes or instances</span></span>

<span data-ttu-id="3f3d6-177">Especifica el idioma de origen de una clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="3f3d6-178">Para obtener más información sobre los valores de configuración regional, consulte [códigos de configuración regional](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-180">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-180">Data type: **string array**</span></span>

<span data-ttu-id="3f3d6-181">Se aplica a: instancias de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f3d6-181">Applies to: namespace instances</span></span>

<span data-ttu-id="3f3d6-182">Especifica un descriptor de seguridad para el espacio de nombres en formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="3f3d6-183">Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="3f3d6-184">WMI procesa la cadena SDDL para establecer la seguridad del espacio de nombres, pero no se almacena como una cadena.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="3f3d6-185">Si no se especifica ningún descriptor de seguridad, se usa la seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="3f3d6-186">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Opta**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-188">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-188">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-189">Se aplica a: parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3d6-189">Applies to: parameters</span></span>

<span data-ttu-id="3f3d6-190">Indica que un parámetro no es necesario y que tiene un valor predeterminado con el comportamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privilegios**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-192">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-192">Data type: **string array**</span></span>

<span data-ttu-id="3f3d6-193">Se aplica a: propiedades, métodos</span><span class="sxs-lookup"><span data-stu-id="3f3d6-193">Applies to: properties, methods</span></span>

<span data-ttu-id="3f3d6-194">Conjunto de valores que se usa para informar al cliente de los privilegios necesarios para crear instancias, rellenar propiedades o realizar métodos.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="3f3d6-195">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-197">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-198">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-198">Applies to: properties</span></span>

<span data-ttu-id="3f3d6-199">Indica que una propiedad de instancia contiene los valores proporcionados por los proveedores de propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="3f3d6-200">Debe especificar este calificador en una propiedad de este tipo.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="3f3d6-201">El valor se pasa al proveedor de propiedades como argumento a [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-203">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-204">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-204">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-205">El valor de este calificador es el nombre del proveedor dinámico que proporciona instancias de clase y actualiza los datos de instancia.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="3f3d6-206">Este nombre se debe registrar con WMI mediante la creación de una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) con la propiedad **Name** que contiene este nombre.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="3f3d6-207">Cuando se especifica este calificador en una clase cuyas instancias se proporcionan dinámicamente, también se debe especificar el calificador **dinámico** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-209">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-209">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-210">Se aplica a: instancias de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f3d6-210">Applies to: namespace instances</span></span>

<span data-ttu-id="3f3d6-211">Si se establece en **true**, **RequiresEncryption** marca un espacio de nombres para que las aplicaciones cliente y los scripts se deben conectar con la autenticación cifrada.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="3f3d6-212">El nivel de autenticación debe establecerse **en \_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C en C++.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="3f3d6-213">En scripting o Visual Basic, el nivel de autenticación debe establecerse en **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="3f3d6-214">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="3f3d6-215">El calificador se utiliza en [*MOF*](gloss-m.md) con el comando de preprocesador de espacio de nombres pragma.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="3f3d6-216">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante C++](setting-the-default-process-security-level-using-c-.md) o [establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="3f3d6-217">Los niveles de autenticación de scripting se definen en [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Simple**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-219">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-220">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-220">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-221">Designa una clase que solo puede tener una instancia y que no contiene propiedades de clave.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="3f3d6-222">Solo se permite el valor **true** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="3f3d6-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Estático**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-224">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-224">Data type: **boolean**</span></span>

<span data-ttu-id="3f3d6-225">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="3f3d6-225">Applies to: methods</span></span>

<span data-ttu-id="3f3d6-226">Indica si se puede llamar a un método utilizando la definición de clase o sus instancias.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="3f3d6-227">No se puede invocar el método desde una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-229">Tipo de datos: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="3f3d6-230">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-230">Applies to: properties</span></span>

<span data-ttu-id="3f3d6-231">Indica que una propiedad de tipo **\_ DateTime de CIM** representa un intervalo de tiempo en lugar de una hora específica.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="3f3d6-232">Para identificar la propiedad como un intervalo, el valor de este calificador debe ser "Interval".</span><span class="sxs-lookup"><span data-stu-id="3f3d6-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="3f3d6-233">El resto de los valores de este calificador se reservan para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-235">Data type: **string**</span></span>

<span data-ttu-id="3f3d6-236">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-236">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-237">Identificador único universal que se aplica a la clase.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-239">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-239">Data type: **string**</span></span>

<span data-ttu-id="3f3d6-240">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="3f3d6-240">Applies to: classes</span></span>

<span data-ttu-id="3f3d6-241">Número de versión del objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-241">The version number of the class object.</span></span> <span data-ttu-id="3f3d6-242">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-242">The default is **NULL**.</span></span> <span data-ttu-id="3f3d6-243">El número de versión se incrementa cuando se realizan cambios en la clase.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="3f3d6-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="3f3d6-245">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="3f3d6-245">Data type: **string array**</span></span>

<span data-ttu-id="3f3d6-246">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="3f3d6-246">Applies to: properties</span></span>

<span data-ttu-id="3f3d6-247">Conjunto de valores que indican qué privilegios del sistema deben estar disponibles y habilitados para una operación de escritura correcta.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f3d6-248">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f3d6-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="3f3d6-249">Códigos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="3f3d6-249">Locale Codes</span></span>

<span data-ttu-id="3f3d6-250">Un código de configuración regional tiene el formato "MS \_ <Three Digit Language ID> ".</span><span class="sxs-lookup"><span data-stu-id="3f3d6-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="3f3d6-251">Por ejemplo, la configuración regional en inglés es MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="3f3d6-252">En la tabla siguiente se enumeran los identificadores de idioma.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="3f3d6-253">Idioma</span><span class="sxs-lookup"><span data-stu-id="3f3d6-253">Language</span></span>              | <span data-ttu-id="3f3d6-254">IDENTIFICADOR de idioma (hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="3f3d6-255">Árabe</span><span class="sxs-lookup"><span data-stu-id="3f3d6-255">Arabic</span></span>                | <span data-ttu-id="3f3d6-256">401</span><span class="sxs-lookup"><span data-stu-id="3f3d6-256">401</span></span>                       |
| <span data-ttu-id="3f3d6-257">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="3f3d6-258">416</span><span class="sxs-lookup"><span data-stu-id="3f3d6-258">416</span></span>                       |
| <span data-ttu-id="3f3d6-259">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="3f3d6-260">804</span><span class="sxs-lookup"><span data-stu-id="3f3d6-260">804</span></span>                       |
| <span data-ttu-id="3f3d6-261">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-261">Chinese (Traditional)</span></span> | <span data-ttu-id="3f3d6-262">404</span><span class="sxs-lookup"><span data-stu-id="3f3d6-262">404</span></span>                       |
| <span data-ttu-id="3f3d6-263">Checo</span><span class="sxs-lookup"><span data-stu-id="3f3d6-263">Czech</span></span>                 | <span data-ttu-id="3f3d6-264">405</span><span class="sxs-lookup"><span data-stu-id="3f3d6-264">405</span></span>                       |
| <span data-ttu-id="3f3d6-265">Danés</span><span class="sxs-lookup"><span data-stu-id="3f3d6-265">Danish</span></span>                | <span data-ttu-id="3f3d6-266">406</span><span class="sxs-lookup"><span data-stu-id="3f3d6-266">406</span></span>                       |
| <span data-ttu-id="3f3d6-267">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="3f3d6-267">Dutch</span></span>                 | <span data-ttu-id="3f3d6-268">413</span><span class="sxs-lookup"><span data-stu-id="3f3d6-268">413</span></span>                       |
| <span data-ttu-id="3f3d6-269">Inglés (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-269">English (default)</span></span>     | <span data-ttu-id="3f3d6-270">409</span><span class="sxs-lookup"><span data-stu-id="3f3d6-270">409</span></span>                       |
| <span data-ttu-id="3f3d6-271">Finés</span><span class="sxs-lookup"><span data-stu-id="3f3d6-271">Finnish</span></span>               | <span data-ttu-id="3f3d6-272">40b</span><span class="sxs-lookup"><span data-stu-id="3f3d6-272">40b</span></span>                       |
| <span data-ttu-id="3f3d6-273">Francés</span><span class="sxs-lookup"><span data-stu-id="3f3d6-273">French</span></span>                | <span data-ttu-id="3f3d6-274">40c</span><span class="sxs-lookup"><span data-stu-id="3f3d6-274">40c</span></span>                       |
| <span data-ttu-id="3f3d6-275">Alemán</span><span class="sxs-lookup"><span data-stu-id="3f3d6-275">German</span></span>                | <span data-ttu-id="3f3d6-276">407</span><span class="sxs-lookup"><span data-stu-id="3f3d6-276">407</span></span>                       |
| <span data-ttu-id="3f3d6-277">Griego</span><span class="sxs-lookup"><span data-stu-id="3f3d6-277">Greek</span></span>                 | <span data-ttu-id="3f3d6-278">408</span><span class="sxs-lookup"><span data-stu-id="3f3d6-278">408</span></span>                       |
| <span data-ttu-id="3f3d6-279">Hebreo</span><span class="sxs-lookup"><span data-stu-id="3f3d6-279">Hebrew</span></span>                | <span data-ttu-id="3f3d6-280">40d</span><span class="sxs-lookup"><span data-stu-id="3f3d6-280">40d</span></span>                       |
| <span data-ttu-id="3f3d6-281">Húngaro</span><span class="sxs-lookup"><span data-stu-id="3f3d6-281">Hungarian</span></span>             | <span data-ttu-id="3f3d6-282">40e</span><span class="sxs-lookup"><span data-stu-id="3f3d6-282">40e</span></span>                       |
| <span data-ttu-id="3f3d6-283">Italiano</span><span class="sxs-lookup"><span data-stu-id="3f3d6-283">Italian</span></span>               | <span data-ttu-id="3f3d6-284">410</span><span class="sxs-lookup"><span data-stu-id="3f3d6-284">410</span></span>                       |
| <span data-ttu-id="3f3d6-285">Japonés</span><span class="sxs-lookup"><span data-stu-id="3f3d6-285">Japanese</span></span>              | <span data-ttu-id="3f3d6-286">411</span><span class="sxs-lookup"><span data-stu-id="3f3d6-286">411</span></span>                       |
| <span data-ttu-id="3f3d6-287">Coreano</span><span class="sxs-lookup"><span data-stu-id="3f3d6-287">Korean</span></span>                | <span data-ttu-id="3f3d6-288">412</span><span class="sxs-lookup"><span data-stu-id="3f3d6-288">412</span></span>                       |
| <span data-ttu-id="3f3d6-289">Noruego</span><span class="sxs-lookup"><span data-stu-id="3f3d6-289">Norwegian</span></span>             | <span data-ttu-id="3f3d6-290">414</span><span class="sxs-lookup"><span data-stu-id="3f3d6-290">414</span></span>                       |
| <span data-ttu-id="3f3d6-291">Polaco</span><span class="sxs-lookup"><span data-stu-id="3f3d6-291">Polish</span></span>                | <span data-ttu-id="3f3d6-292">415</span><span class="sxs-lookup"><span data-stu-id="3f3d6-292">415</span></span>                       |
| <span data-ttu-id="3f3d6-293">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="3f3d6-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="3f3d6-294">816</span><span class="sxs-lookup"><span data-stu-id="3f3d6-294">816</span></span>                       |
| <span data-ttu-id="3f3d6-295">Ruso</span><span class="sxs-lookup"><span data-stu-id="3f3d6-295">Russian</span></span>               | <span data-ttu-id="3f3d6-296">419</span><span class="sxs-lookup"><span data-stu-id="3f3d6-296">419</span></span>                       |
| <span data-ttu-id="3f3d6-297">Español</span><span class="sxs-lookup"><span data-stu-id="3f3d6-297">Spanish</span></span>               | <span data-ttu-id="3f3d6-298">c0a</span><span class="sxs-lookup"><span data-stu-id="3f3d6-298">c0a</span></span>                       |
| <span data-ttu-id="3f3d6-299">Sueco</span><span class="sxs-lookup"><span data-stu-id="3f3d6-299">Swedish</span></span>               | <span data-ttu-id="3f3d6-300">41D</span><span class="sxs-lookup"><span data-stu-id="3f3d6-300">41D</span></span>                       |
| <span data-ttu-id="3f3d6-301">Turco</span><span class="sxs-lookup"><span data-stu-id="3f3d6-301">Turkish</span></span>               | <span data-ttu-id="3f3d6-302">41f</span><span class="sxs-lookup"><span data-stu-id="3f3d6-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="3f3d6-303">Usar el \_ calificador de GetObject bypass</span><span class="sxs-lookup"><span data-stu-id="3f3d6-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="3f3d6-304">El uso del calificador **\_ GetObject bypass** en un método puede generar resultados confusos.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="3f3d6-305">En el ejemplo siguiente se definen las clases de **forma** y **círculo** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="3f3d6-306">Tenga en cuenta que la clase **Circle** se deriva de la clase **Shape** .</span><span class="sxs-lookup"><span data-stu-id="3f3d6-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="3f3d6-307">La siguiente llamada a **ExecMethod** usa un objeto **Circle** denominado "Circle" para dibujar un círculo.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="3f3d6-308">En el escenario anterior, WMI llama a **GetObject**; detecta que "Shape. name = ' Circle '" es un **círculo**; y ejecutan la implementación del **círculo** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="3f3d6-309">Sin embargo, si usa el calificador **bypass \_ GetObject** en **DrawIt**, WMI no llama a **GetObject**, no detecta que "Shape. name = ' Circle '" es un **círculo** y ejecuta la implementación de la **forma** de **DrawIt** en lugar de la implementación de **Circle** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="3f3d6-310">La siguiente llamada a **ExecMethod** siempre invoca la implementación correcta de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="3f3d6-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="3f3d6-311">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3d6-311">Requirements</span></span>



| <span data-ttu-id="3f3d6-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f3d6-312">Requirement</span></span> | <span data-ttu-id="3f3d6-313">Value</span><span class="sxs-lookup"><span data-stu-id="3f3d6-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3f3d6-314">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f3d6-314">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3d6-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f3d6-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3f3d6-316">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f3d6-316">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3d6-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f3d6-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f3d6-318">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f3d6-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3d6-319">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="3f3d6-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="3f3d6-320">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="3f3d6-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="3f3d6-321">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="3f3d6-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

