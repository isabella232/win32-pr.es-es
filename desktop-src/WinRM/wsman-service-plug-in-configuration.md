---
title: Configuración del complemento de servicio WinRM
description: Un complemento de Administración remota de Windows (WinRM) debe estar registrado en el catálogo de WinRM para permitir que la infraestructura determine dinámicamente el conjunto de complementos disponibles y los URI de recurso que admiten.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104359507"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="05fe9-103">Configuración del complemento de servicio WinRM</span><span class="sxs-lookup"><span data-stu-id="05fe9-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="05fe9-104">Un complemento de Administración remota de Windows (WinRM) debe estar registrado en el catálogo de WinRM para permitir que la infraestructura determine dinámicamente el conjunto de complementos disponibles y los [*URI de recurso*](windows-remote-management-glossary.md) que admiten.</span><span class="sxs-lookup"><span data-stu-id="05fe9-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="05fe9-105">Todos los [*URI de recursos*](windows-remote-management-glossary.md) de los complementos de WinRM deben ajustarse al formato que se define en RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ).</span><span class="sxs-lookup"><span data-stu-id="05fe9-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="05fe9-106">La configuración se realiza a través del servicio WinRM principal.</span><span class="sxs-lookup"><span data-stu-id="05fe9-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="05fe9-107">El comando siguiente registra una configuración de complemento con el servicio WinRM:</span><span class="sxs-lookup"><span data-stu-id="05fe9-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="05fe9-108">El servicio WinRM debe reiniciarse para exponer los complementos recién registrados.</span><span class="sxs-lookup"><span data-stu-id="05fe9-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="05fe9-109">La configuración del complemento se especifica en XML.</span><span class="sxs-lookup"><span data-stu-id="05fe9-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="05fe9-110">A continuación se muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="05fe9-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="05fe9-111">La lista siguiente describe los elementos XML con más detalle y va seguido del esquema de configuración especificado como XSD.</span><span class="sxs-lookup"><span data-stu-id="05fe9-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="05fe9-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**</span><span class="sxs-lookup"><span data-stu-id="05fe9-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-113">Especifica el nombre de archivo del complemento de operaciones.</span><span class="sxs-lookup"><span data-stu-id="05fe9-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="05fe9-114">Las variables de entorno que se colocan en esta entrada se expandirán en el contexto de los usuarios cuando llegue una solicitud.</span><span class="sxs-lookup"><span data-stu-id="05fe9-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="05fe9-115">Cada usuario puede tener una versión diferente de la misma variable de entorno, por lo que cada usuario podría acabar con otro complemento.</span><span class="sxs-lookup"><span data-stu-id="05fe9-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="05fe9-116">Esta entrada no puede estar en blanco y debe apuntar a un complemento válido.</span><span class="sxs-lookup"><span data-stu-id="05fe9-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nombre** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-118">Especifica el nombre para mostrar que se va a utilizar para el complemento.</span><span class="sxs-lookup"><span data-stu-id="05fe9-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="05fe9-119">Si el complemento devuelve un error, este nombre se colocará en el XML de error que se devuelve a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="05fe9-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="05fe9-120">El nombre no es específico de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="05fe9-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Arquitectura** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-122">Especifica si el complemento de operaciones es de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05fe9-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="05fe9-123">Si no se especifica este elemento, el valor predeterminado será "32" en los sistemas x86 y en "64" en los sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05fe9-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="05fe9-124">En los sistemas x86, el único valor válido es "32".</span><span class="sxs-lookup"><span data-stu-id="05fe9-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="05fe9-125">Si el valor es "32" en un sistema de 64 bits, es necesario tener en cuenta la redirección de WOW64 al escribir la información del **nombre de archivo** .</span><span class="sxs-lookup"><span data-stu-id="05fe9-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="05fe9-126">El sistema de archivos subyacente usará la redirección de WOW64 para traducir system32 a SysWow64.</span><span class="sxs-lookup"><span data-stu-id="05fe9-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="05fe9-127">Por ejemplo, si el **nombre de archivo** es "% WINDIR% \\ system32 \\myplugin.dll" y la **arquitectura** es "32", el archivo de complemento real se encuentra en "% WINDIR% \\ SysWow64 \\myplugin.dll".</span><span class="sxs-lookup"><span data-stu-id="05fe9-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**</span><span class="sxs-lookup"><span data-stu-id="05fe9-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-129">Configura el formato en el que se pasa el XML a los complementos a través del objeto de [**\_ datos WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) .</span><span class="sxs-lookup"><span data-stu-id="05fe9-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="05fe9-130">Los siguientes tipos están disponibles:</span><span class="sxs-lookup"><span data-stu-id="05fe9-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="05fe9-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita</span><span class="sxs-lookup"><span data-stu-id="05fe9-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-132">Los datos XML entrantes se encuentran en una \_ estructura de texto de tipo de datos WSMAN \_ \_ , que representa el XML como un búfer de memoria **PCWSTR** .</span><span class="sxs-lookup"><span data-stu-id="05fe9-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span><span class="sxs-lookup"><span data-stu-id="05fe9-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-134">Los datos XML entrantes se encuentran en un \_ tipo de datos WSMAN \_ \_ \_ \_ estructura del lector XML de WS, que representa el XML como un objeto **XmlReader** , que se define en el archivo de encabezado webservices. h.</span><span class="sxs-lookup"><span data-stu-id="05fe9-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="05fe9-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**</span><span class="sxs-lookup"><span data-stu-id="05fe9-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-136">Este nodo es opcional y permite a un complemento configurar XML adicional que se pasará al método [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).</span><span class="sxs-lookup"><span data-stu-id="05fe9-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="05fe9-137">La mayoría de los complementos no necesitarán esta información adicional, pero si es necesario usar un complemento en más de un escenario que requiera una semántica diferente en tiempo de ejecución, este XML proporcionará al complemento la flexibilidad necesaria para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="05fe9-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Recursos** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-139">Especifica una lista de [*URI de recurso*](windows-remote-management-glossary.md)que este complemento admite.</span><span class="sxs-lookup"><span data-stu-id="05fe9-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="05fe9-140">Se debe especificar al menos una entrada **ResourceUri**; de lo contrario, se rechazará el XML.</span><span class="sxs-lookup"><span data-stu-id="05fe9-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Recursos** / de **Recurso** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-142">Representa una configuración de [*URI de recurso*](windows-remote-management-glossary.md)único.</span><span class="sxs-lookup"><span data-stu-id="05fe9-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="05fe9-143">El atributo **SupportsOptions** se puede establecer en false.</span><span class="sxs-lookup"><span data-stu-id="05fe9-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="05fe9-144">Si **SupportsOptions** se establece en false, este atributo no se muestra cuando se enumera el recurso.</span><span class="sxs-lookup"><span data-stu-id="05fe9-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="05fe9-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Recursos** / de **Recurso** / de **ResourceUri**</span><span class="sxs-lookup"><span data-stu-id="05fe9-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-146">Especifica un [*URI de recurso*](windows-remote-management-glossary.md) único en su totalidad o como una cadena de coincidencia parcial basada en el atributo **ExactMatch** .</span><span class="sxs-lookup"><span data-stu-id="05fe9-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="05fe9-147">Si **ExactMatch** no está presente, el valor predeterminado es **false**, lo que significa que el procesador SOAP de WinRM realizará una coincidencia parcial con el inicio del *URI del recurso* y, si hay una coincidencia, la pasará al complemento.</span><span class="sxs-lookup"><span data-stu-id="05fe9-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="05fe9-148">El atributo **SupportsOptions** se puede especificar si se permite que se pasen opciones a este *URI de recurso* .</span><span class="sxs-lookup"><span data-stu-id="05fe9-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="05fe9-149">De forma predeterminada, no se admiten opciones y, si hay alguna presente en la solicitud de cliente, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="05fe9-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="05fe9-150">Si el complemento admite las opciones, es importante que el complemento devuelva el error correcto si hay una opción que indica que el complemento no entiende si la marca **MustUnderstand** está establecida en **true**...</span><span class="sxs-lookup"><span data-stu-id="05fe9-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Recursos** / de **Recurso** / de **Funcionalidad** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-152">Especifica una funcionalidad que está disponible en este [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-153">Habrá una entrada para cada tipo de operación que admita.</span><span class="sxs-lookup"><span data-stu-id="05fe9-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="05fe9-154">Están disponibles las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="05fe9-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="05fe9-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Obtener</span><span class="sxs-lookup"><span data-stu-id="05fe9-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-156">Las operaciones GET se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-157">El atributo **SupportFragment** se usa si la operación Get admite el concepto.</span><span class="sxs-lookup"><span data-stu-id="05fe9-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="05fe9-158">El atributo **SupportFiltering** no es válido y debe establecerse en false.</span><span class="sxs-lookup"><span data-stu-id="05fe9-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="05fe9-159">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Pondrán</span><span class="sxs-lookup"><span data-stu-id="05fe9-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-161">Las operaciones put se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-162">El atributo **SupportFragment** se usa si la operación PUT es compatible con el concepto.</span><span class="sxs-lookup"><span data-stu-id="05fe9-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="05fe9-163">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-164">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>A</span><span class="sxs-lookup"><span data-stu-id="05fe9-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-166">Las operaciones de creación se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-167">El atributo **SupportFragment** se usa si la operación de creación es compatible con el concepto.</span><span class="sxs-lookup"><span data-stu-id="05fe9-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="05fe9-168">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-169">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Elimínelos</span><span class="sxs-lookup"><span data-stu-id="05fe9-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-171">Las operaciones de eliminación se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-172">El atributo **SupportFragment** se usa si la operación de eliminación admite el concepto.</span><span class="sxs-lookup"><span data-stu-id="05fe9-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="05fe9-173">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-174">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Vocó</span><span class="sxs-lookup"><span data-stu-id="05fe9-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-176">Las operaciones de invocación se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-177">El atributo **SupportFragment** no se admite para las operaciones de invocación y debe establecerse en false.</span><span class="sxs-lookup"><span data-stu-id="05fe9-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="05fe9-178">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-179">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerar</span><span class="sxs-lookup"><span data-stu-id="05fe9-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-181">Las operaciones de enumeración se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-182">El atributo **SupportFragment** no se admite para las operaciones de enumeración y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="05fe9-183">El atributo **SupportFiltering** es válido y, si el complemento admite el filtrado, este atributo debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="05fe9-184">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>ID</span><span class="sxs-lookup"><span data-stu-id="05fe9-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-186">Se admiten las operaciones subscribe en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-187">El atributo **SupportFragment** no se admite para las operaciones subscribe y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="05fe9-188">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-189">Esta funcionalidad no es válida para un *URI de recurso* si también se admiten las operaciones de Shell.</span><span class="sxs-lookup"><span data-stu-id="05fe9-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="05fe9-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Interfaz</span><span class="sxs-lookup"><span data-stu-id="05fe9-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-191">Las operaciones de Shell se admiten en el [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="05fe9-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="05fe9-192">El atributo **SupportFragment** no se admite para las operaciones de Shell y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="05fe9-193">El atributo **SupportFiltering** no es válido y debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="05fe9-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="05fe9-194">Esta funcionalidad no es válida para un *URI de recurso* si también se admite cualquier otra funcionalidad de operación.</span><span class="sxs-lookup"><span data-stu-id="05fe9-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="05fe9-195">Si se configura una funcionalidad de operación de Shell para un *URI de recurso*, las operaciones GET, Put, Create, Delete, Invoke y Enumerate se procesan internamente dentro del servicio WinRm para administrar los shells.</span><span class="sxs-lookup"><span data-stu-id="05fe9-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="05fe9-196">Como resultado, el complemento no puede tratar con las propias operaciones.</span><span class="sxs-lookup"><span data-stu-id="05fe9-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="05fe9-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Recursos** / de **Recurso** / de **Seguridad** de</span><span class="sxs-lookup"><span data-stu-id="05fe9-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="05fe9-198">Este elemento define el descriptor de seguridad (a través del atributo **SDDL** ) que debe aplicarse para determinar el acceso a un [*URI de recurso*](windows-remote-management-glossary.md) determinado (a través del atributo **URI** ).</span><span class="sxs-lookup"><span data-stu-id="05fe9-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="05fe9-199">Si **ExactMatch** no está presente, el elemento de **seguridad** tiene como valor predeterminado **false**, lo que significa que el **SDDL** se aplica a todos los *URI de recursos* que comparten el **URI** como prefijo.</span><span class="sxs-lookup"><span data-stu-id="05fe9-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="05fe9-200">Si **ExactMatch** se establece en true, el **SDDL** solo se aplica al **URI** exacto especificado.</span><span class="sxs-lookup"><span data-stu-id="05fe9-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="05fe9-201">Si hay varias entradas de **seguridad** que se pueden aplicar a un *URI de recurso* determinado, la coincidencia de prefijo más largo se utiliza para determinar el **SDDL** adecuado.</span><span class="sxs-lookup"><span data-stu-id="05fe9-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="05fe9-202">Como resultado de la coincidencia de prefijo más largo, si existe una entrada de **URI** de coincidencia exacta, siempre se elegirá como el elemento de seguridad adecuado.</span><span class="sxs-lookup"><span data-stu-id="05fe9-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="05fe9-203">A continuación se indica el esquema de configuración del complemento especificado como XSD.</span><span class="sxs-lookup"><span data-stu-id="05fe9-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




