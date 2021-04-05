---
title: URI de recursos
description: Un URI de recurso es un identificador de un tipo distinto de operación de administración o valor utilizado por los servicios de administración que implementan el protocolo WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533196"
---
# <a name="resource-uris"></a><span data-ttu-id="62a3d-103">URI de recursos</span><span class="sxs-lookup"><span data-stu-id="62a3d-103">Resource URIs</span></span>

<span data-ttu-id="62a3d-104">Un [*URI de recurso*](windows-remote-management-glossary.md) es un identificador de un tipo distinto de operación de administración o valor utilizado por los servicios de administración que implementan el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="62a3d-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="62a3d-105">Un valor de administración podría ser la temperatura dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="62a3d-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="62a3d-106">Un ejemplo de una operación de administración es iniciar un servicio detenido o establecer una cuota de usuario del volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="62a3d-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="62a3d-107">Formato de URI de recurso</span><span class="sxs-lookup"><span data-stu-id="62a3d-107">Resource URI Format</span></span>

<span data-ttu-id="62a3d-108">Un URI consta de un prefijo y una ruta de acceso a un recurso, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="62a3d-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="62a3d-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="62a3d-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="62a3d-110">Esta especificación del esquema indica que el URI se basa en la versión 1 del protocolo oficial WS-Management y que el recurso es [**un \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres "root cimv2" del repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="62a3d-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="62a3d-111">Los prefijos de URI contienen una especificación de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" y un tipo específico de recurso, como el **\_ LogicalDisk de Win32**.</span><span class="sxs-lookup"><span data-stu-id="62a3d-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="62a3d-112">Para obtener más información sobre cómo identificar una instancia específica de una clase WMI, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="62a3d-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="62a3d-113">Para obtener más información, vea [prefijos de URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="62a3d-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="62a3d-114">Tipos de URI de recurso</span><span class="sxs-lookup"><span data-stu-id="62a3d-114">Types of Resource URIs</span></span>

<span data-ttu-id="62a3d-115">Mientras [*instrumental de administración de Windows (WMI)*](windows-remote-management-glossary.md) es el origen principal de los datos de administración para los sistemas operativos basados en Windows, también existen otros orígenes de esquema de administración.</span><span class="sxs-lookup"><span data-stu-id="62a3d-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="62a3d-116">En la siguiente lista se describen varios tipos de URI de recursos usados por Administración remota de Windows:</span><span class="sxs-lookup"><span data-stu-id="62a3d-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="62a3d-117">URI de WMI</span><span class="sxs-lookup"><span data-stu-id="62a3d-117">WMI URIs</span></span>

    <span data-ttu-id="62a3d-118">Este grupo de URI representa una ruta de acceso de clase [*modelo de información común*](/windows/desktop/WmiSdk/gloss-c) que incluye el espacio de nombres y la clase.</span><span class="sxs-lookup"><span data-stu-id="62a3d-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="62a3d-119">Los URI de WMI se pueden usar en:</span><span class="sxs-lookup"><span data-stu-id="62a3d-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="62a3d-120">Métodos de [**sesión**](session.md)</span><span class="sxs-lookup"><span data-stu-id="62a3d-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="62a3d-121">Métodos [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="62a3d-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="62a3d-122">Métodos [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) o [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="62a3d-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="62a3d-123">Métodos [**ResourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="62a3d-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="62a3d-124">URI de IPMI</span><span class="sxs-lookup"><span data-stu-id="62a3d-124">IPMI URIs</span></span>

    <span data-ttu-id="62a3d-125">Este grupo de URI representan los URI estándar del sector basados en la versión 2,9 de CIM.</span><span class="sxs-lookup"><span data-stu-id="62a3d-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="62a3d-126">Los URI de IPMI se pueden usar en métodos de [**sesión**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="62a3d-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="62a3d-127">Un ejemplo es https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="62a3d-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="62a3d-128">Este recurso se define según el esquema CIM de [DMTF.org](https://www.dmtf.org/home) .</span><span class="sxs-lookup"><span data-stu-id="62a3d-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="62a3d-129">URI de configuración de WinRM</span><span class="sxs-lookup"><span data-stu-id="62a3d-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="62a3d-130">Este grupo de URI son operaciones de configuración para la configuración del [*agente de escucha*](windows-remote-management-glossary.md) de WinRM.</span><span class="sxs-lookup"><span data-stu-id="62a3d-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="62a3d-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener se puede usar en métodos de [**sesión**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)y [**Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="62a3d-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="62a3d-132">Uri [*del registro de eventos del sistema*](windows-remote-management-glossary.md) (SEL)</span><span class="sxs-lookup"><span data-stu-id="62a3d-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="62a3d-133">Este grupo de URI se suscribe a eventos del recopilador de eventos desde el BMC.</span><span class="sxs-lookup"><span data-stu-id="62a3d-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="62a3d-134">Puede suscribirse a estos eventos mediante la herramienta de línea de comandos **wevtutil** .</span><span class="sxs-lookup"><span data-stu-id="62a3d-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="62a3d-135">Para más información, consulte https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="62a3d-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="62a3d-136">Distinción entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="62a3d-136">Case Sensitivity</span></span>

<span data-ttu-id="62a3d-137">El [*complemento WMI*](windows-remote-management-glossary.md) conserva el caso del URI de recurso recibido en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="62a3d-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="62a3d-138">Sin embargo, para garantizar la interoperabilidad con otras implementaciones del protocolo WS-Management, use el caso correcto para el recurso solicitado en el URI del recurso.</span><span class="sxs-lookup"><span data-stu-id="62a3d-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="62a3d-139">El caso correcto es el corrector ortográfico definido por el proveedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="62a3d-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="62a3d-140">Aunque los URI de recursos no requieren distinción de mayúsculas y minúsculas, XML de [*fragmento*](windows-remote-management-glossary.md) sí.</span><span class="sxs-lookup"><span data-stu-id="62a3d-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="62a3d-141">Un fragmento especifica solo una propiedad, en lugar del conjunto completo de propiedades de un recurso.</span><span class="sxs-lookup"><span data-stu-id="62a3d-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="62a3d-142">En el caso de los recursos WMI, la sintaxis de fragmentos obtiene una propiedad de una instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="62a3d-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="62a3d-143">Por ejemplo, la obtención de la propiedad **version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requiere el uso de un fragmento.</span><span class="sxs-lookup"><span data-stu-id="62a3d-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="62a3d-144">Para obtener más información acerca de los fragmentos, vea "agregar un selector a un objeto ResourceLocator o IWSManResourceLocator" en [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="62a3d-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="62a3d-145">En los siguientes estándares XML y [*XPath*](windows-remote-management-glossary.md) , el [*complemento WMI*](windows-remote-management-glossary.md) aplica la distinción de mayúsculas y minúsculas para los fragmentos y XML que define los parámetros de entrada de un método.</span><span class="sxs-lookup"><span data-stu-id="62a3d-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="62a3d-146">La distinción de mayúsculas y minúsculas es necesaria para admitir el estándar XPath 1.0/nivel 1.</span><span class="sxs-lookup"><span data-stu-id="62a3d-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="62a3d-147">Para obtener datos de WMI a través de WinRM, la distinción de mayúsculas y minúsculas significa que los nombres de las clases, las propiedades y los métodos de WMI deben coincidir con las mayúsculas y minúsculas del nombre que se encuentra en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="62a3d-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="62a3d-148">Para obtener más información, vea [Sintaxis de XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="62a3d-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="62a3d-149">Ejemplos de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="62a3d-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="62a3d-150">Por ejemplo, un script que obtiene la propiedad **del \_ descriptor de seguridad** de una instancia de la clase de [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) de WMI no puede usar mayúsculas para los nombres de la ruta de acceso del fragmento, solo el URI.</span><span class="sxs-lookup"><span data-stu-id="62a3d-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="62a3d-151">El [*complemento de WMI*](windows-remote-management-glossary.md) de WinRM devuelve un error para el siguiente ejemplo de VBScript porque el XML de XPath proporcionado para **FragmentPath** no utiliza las mayúsculas y minúsculas correctas.</span><span class="sxs-lookup"><span data-stu-id="62a3d-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="62a3d-152">En el repositorio WMI, la clase está escrita como " \_ servicio Win32".</span><span class="sxs-lookup"><span data-stu-id="62a3d-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="62a3d-153">La siguiente versión del mismo ejemplo muestra el uso correcto de Case para la clase [**de \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) y la propiedad **\_ descriptor de seguridad** .</span><span class="sxs-lookup"><span data-stu-id="62a3d-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="62a3d-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62a3d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62a3d-155">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="62a3d-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="62a3d-156">Administración remota de hardware</span><span class="sxs-lookup"><span data-stu-id="62a3d-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="62a3d-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="62a3d-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 