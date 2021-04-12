---
title: Tipo complejo de ProviderType
description: Define un proveedor y los metadatos que usa para definir sus eventos. | Tipo complejo de ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Registro de eventos de tipo complejo de ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362273"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="14ec9-105">Tipo complejo de ProviderType</span><span class="sxs-lookup"><span data-stu-id="14ec9-105">ProviderType Complex Type</span></span>

<span data-ttu-id="14ec9-106">Define un proveedor y los metadatos que usa para definir sus eventos.</span><span class="sxs-lookup"><span data-stu-id="14ec9-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="14ec9-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14ec9-107">Child elements</span></span>



| <span data-ttu-id="14ec9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="14ec9-108">Element</span></span>                                                                       | <span data-ttu-id="14ec9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="14ec9-109">Type</span></span>                                                                         | <span data-ttu-id="14ec9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="14ec9-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14ec9-111">**circuitos**</span><span class="sxs-lookup"><span data-stu-id="14ec9-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="14ec9-112">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="14ec9-113">Define una lista de canales en los que los proveedores pueden registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="14ec9-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="14ec9-114">**ceso**</span><span class="sxs-lookup"><span data-stu-id="14ec9-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="14ec9-115">**DefinitionType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="14ec9-116">Define una lista de definiciones de eventos de los eventos que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="14ec9-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="14ec9-117">**complementa**</span><span class="sxs-lookup"><span data-stu-id="14ec9-117">**filters**</span></span>                                                                   | [<span data-ttu-id="14ec9-118">**FilterListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="14ec9-119">Define una lista de filtros que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="14ec9-120">Puede usar los filtros, como lo haría con las palabras clave y, para determinar si desea escribir un evento.</span><span class="sxs-lookup"><span data-stu-id="14ec9-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="14ec9-121">**Windows Server 2008 y Windows Vista:** No se admite hasta Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14ec9-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="14ec9-122">**palabra**</span><span class="sxs-lookup"><span data-stu-id="14ec9-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="14ec9-123">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="14ec9-124">Define una lista de palabras clave que clasifican eventos.</span><span class="sxs-lookup"><span data-stu-id="14ec9-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="14ec9-125">**niveles**</span><span class="sxs-lookup"><span data-stu-id="14ec9-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="14ec9-126">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="14ec9-127">Define una lista de niveles que especifican la gravedad de un evento.</span><span class="sxs-lookup"><span data-stu-id="14ec9-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="14ec9-128">**Maps**</span><span class="sxs-lookup"><span data-stu-id="14ec9-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="14ec9-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="14ec9-130">Define una lista de pares de nombre/valor a los que se puede hacer referencia en la sección de plantilla del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14ec9-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="14ec9-131">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="14ec9-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="14ec9-132">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="14ec9-133">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="14ec9-133">Not used.</span></span> <span data-ttu-id="14ec9-134">Define una lista de consultas con nombre que consultan la cadena de mensaje de evento de un valor y realizan una acción especificada si se encuentran.</span><span class="sxs-lookup"><span data-stu-id="14ec9-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="14ec9-135">**códigos**</span><span class="sxs-lookup"><span data-stu-id="14ec9-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="14ec9-136">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="14ec9-137">Define una lista de códigos de tareas que se pueden usar para agrupar eventos dentro de una tarea.</span><span class="sxs-lookup"><span data-stu-id="14ec9-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="14ec9-138">**tareas**</span><span class="sxs-lookup"><span data-stu-id="14ec9-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="14ec9-139">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="14ec9-140">Define una lista de tareas que un proveedor puede usar para agrupar los eventos.</span><span class="sxs-lookup"><span data-stu-id="14ec9-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="14ec9-141">Normalmente, se usan tareas para agrupar los eventos de una característica o componente del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="14ec9-142">**templa**</span><span class="sxs-lookup"><span data-stu-id="14ec9-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="14ec9-143">**TemplateListType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="14ec9-144">Define una lista de plantillas que especifican los datos que se van a incluir con los eventos.</span><span class="sxs-lookup"><span data-stu-id="14ec9-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="14ec9-145">Atributos</span><span class="sxs-lookup"><span data-stu-id="14ec9-145">Attributes</span></span>



| <span data-ttu-id="14ec9-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="14ec9-146">Name</span></span>                                | <span data-ttu-id="14ec9-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="14ec9-147">Type</span></span>                                                              | <span data-ttu-id="14ec9-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="14ec9-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ec9-149">guid</span><span class="sxs-lookup"><span data-stu-id="14ec9-149">guid</span></span>                                | [<span data-ttu-id="14ec9-150">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="14ec9-151">GUID que identifica de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="14ec9-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="14ec9-152">helpLink</span></span>                            | <span data-ttu-id="14ec9-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="14ec9-153">anyURI</span></span>                                                            | <span data-ttu-id="14ec9-154">La dirección URL o el vínculo de ayuda de MS a contenido que proporciona información sobre los eventos que genera el proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="14ec9-155">message</span><span class="sxs-lookup"><span data-stu-id="14ec9-155">message</span></span>                             | [<span data-ttu-id="14ec9-156">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="14ec9-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="14ec9-157">Nombre para mostrar localizado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-157">The localized display name for the provider.</span></span> <span data-ttu-id="14ec9-158">La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14ec9-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="14ec9-159">messageFileName</span><span class="sxs-lookup"><span data-stu-id="14ec9-159">messageFileName</span></span>                     | [<span data-ttu-id="14ec9-160">**filePath**</span><span class="sxs-lookup"><span data-stu-id="14ec9-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="14ec9-161">Ruta de acceso completa al archivo que contiene los recursos localizados del mensaje del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="14ec9-162">El archivo puede ser un archivo ejecutable o un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="14ec9-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="14ec9-163">name</span><span class="sxs-lookup"><span data-stu-id="14ec9-163">name</span></span>                                | <span data-ttu-id="14ec9-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="14ec9-164">anyURI</span></span>                                                            | <span data-ttu-id="14ec9-165">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-165">The name of the provider.</span></span> <span data-ttu-id="14ec9-166">El nombre debe tener el formato, componente de producto de *empresa* -  - .</span><span class="sxs-lookup"><span data-stu-id="14ec9-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="14ec9-167">El nombre no puede tener más de 255 caracteres y no puede contener los caracteres: ' > ', ' < ', ' & ', ' "', ' \| ', ' \\ ', ': ', ' ', '? ', ' \* ' ni caracteres con códigos inferiores a 31.</span><span class="sxs-lookup"><span data-stu-id="14ec9-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="14ec9-168">Además, el nombre debe seguir las restricciones generales de los nombres de clave del registro y del archivo.</span><span class="sxs-lookup"><span data-stu-id="14ec9-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="14ec9-169">Estas restricciones se pueden encontrar en nombres de [archivos](/windows/desktop/FileIO/naming-a-file)y [límites de tamaño de elementos del registro](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="14ec9-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="14ec9-170">parameterFileName</span><span class="sxs-lookup"><span data-stu-id="14ec9-170">parameterFileName</span></span>                   | [<span data-ttu-id="14ec9-171">**filePath**</span><span class="sxs-lookup"><span data-stu-id="14ec9-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="14ec9-172">Ruta de acceso completa al archivo que contiene los recursos de cadena de parámetro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="14ec9-173">El archivo puede ser un archivo ejecutable o un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="14ec9-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="14ec9-174">Puede especificar más de un archivo de parámetros separado por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="14ec9-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="14ec9-175">Se busca en el archivo cuando la cadena de mensaje de un evento contiene una cadena de parámetro.</span><span class="sxs-lookup"><span data-stu-id="14ec9-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="14ec9-176">Los parámetros permiten proporcionar cadenas de inserción localizables.</span><span class="sxs-lookup"><span data-stu-id="14ec9-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="14ec9-177">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="14ec9-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="14ec9-178">Nombrearchivorecursos</span><span class="sxs-lookup"><span data-stu-id="14ec9-178">resourceFileName</span></span>                    | [<span data-ttu-id="14ec9-179">**filePath**</span><span class="sxs-lookup"><span data-stu-id="14ec9-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="14ec9-180">Ruta de acceso completa al archivo que contiene los recursos de metadatos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="14ec9-181">El archivo puede ser un archivo ejecutable o un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="14ec9-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="14ec9-182">source</span><span class="sxs-lookup"><span data-stu-id="14ec9-182">source</span></span>                              |                                                                   | <span data-ttu-id="14ec9-183">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="14ec9-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="14ec9-184">símbolo</span><span class="sxs-lookup"><span data-stu-id="14ec9-184">symbol</span></span>                              | [<span data-ttu-id="14ec9-185">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="14ec9-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="14ec9-186">Símbolo que se va a usar para hacer referencia al GUID del proveedor en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14ec9-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="14ec9-187">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el GUID del proveedor en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="14ec9-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="14ec9-188">warnOnApplicationCompatibilityError</span><span class="sxs-lookup"><span data-stu-id="14ec9-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="14ec9-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="14ec9-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="14ec9-190">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="14ec9-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="14ec9-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14ec9-191">Remarks</span></span>

<span data-ttu-id="14ec9-192">El Visor de eventos de Windows (Eventvwr.exe) utilizará la cadena de mensaje localizada si está disponible; de lo contrario, utiliza la cadena del atributo name.</span><span class="sxs-lookup"><span data-stu-id="14ec9-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="14ec9-193">Las rutas de acceso de Nombrearchivorecursos, messageFileName y parameterFileName pueden contener variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="14ec9-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="14ec9-194">Si define una nueva variable de entorno para usar en la ruta de acceso, debe reiniciar el equipo para que el servicio registro de eventos pueda recoger la nueva variable. de lo contrario, el servicio no podrá encontrar los recursos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="14ec9-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="14ec9-195">La cadena de mensaje de un evento puede contener cadenas de inserción y cadenas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="14ec9-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="14ec9-196">Una cadena de inserción tiene el formato%*n*, donde *n* es un índice basado en uno que identifica un elemento de datos de la plantilla de datos del evento que desea insertar en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="14ec9-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="14ec9-197">Una cadena de parámetro (vea el atributo **parameterFileName** ) tiene el formato%%*n*, donde n es el identificador de un mensaje en la tabla de mensajes.</span><span class="sxs-lookup"><span data-stu-id="14ec9-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="14ec9-198">Si la cadena de mensaje del evento contenía "%1% %11 = %2% %12" y los valores de los elementos de datos de %1 y %2 eran 8 y 2, respectivamente, y las cadenas de parámetros de% %11 y% %12 eran "cuartos de galón" y "galones", respectivamente, la cadena con formato sería "8 cuartos de</span><span class="sxs-lookup"><span data-stu-id="14ec9-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="14ec9-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14ec9-199">Requirements</span></span>



| <span data-ttu-id="14ec9-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ec9-200">Requirement</span></span> | <span data-ttu-id="14ec9-201">Value</span><span class="sxs-lookup"><span data-stu-id="14ec9-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14ec9-202">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14ec9-202">Minimum supported client</span></span><br/> | <span data-ttu-id="14ec9-203">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14ec9-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14ec9-204">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14ec9-204">Minimum supported server</span></span><br/> | <span data-ttu-id="14ec9-205">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="14ec9-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

