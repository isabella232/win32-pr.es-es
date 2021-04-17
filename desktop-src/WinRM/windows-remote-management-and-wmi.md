---
title: Administración remota de Windows y WMI
description: Administración remota de Windows se puede utilizar para recuperar los datos expuestos por Instrumental de administración de Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105698032"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="1357a-103">Administración remota de Windows y WMI</span><span class="sxs-lookup"><span data-stu-id="1357a-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="1357a-104">Administración remota de Windows se puede utilizar para recuperar los datos expuestos por Instrumental de administración de Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) y [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span><span class="sxs-lookup"><span data-stu-id="1357a-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="1357a-105">Puede obtener datos de WMI con scripts o aplicaciones que usan la [API de scripting de WinRM](winrm-scripting-api.md) o a través de la herramienta de línea de comandos de **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="1357a-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="1357a-106">WinRM es compatible con la mayoría de las clases y operaciones de WMI conocidas, incluidos los objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="1357a-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="1357a-107">WinRM puede aprovechar WMI para recopilar datos acerca de [*los recursos*](windows-remote-management-glossary.md) o para administrar recursos en un sistema operativo basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="1357a-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="1357a-108">Esto significa que puede obtener datos sobre objetos como discos, adaptadores de red, servicios o procesos de su empresa a través del conjunto existente de [clases WMI](/windows/desktop/WmiSdk/wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="1357a-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="1357a-109">También puede tener acceso a los datos de hardware que están disponibles en el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)estándar de WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="1357a-110">Identificar un recurso WMI</span><span class="sxs-lookup"><span data-stu-id="1357a-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="1357a-111">Puede hacer referencia a una clase WMI como un [*recurso*](windows-remote-management-glossary.md) en WinRM y en el protocolo WS-Management: un tipo de entidad administrada, como un servicio o un disco.</span><span class="sxs-lookup"><span data-stu-id="1357a-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="1357a-112">Una clase o un método WMI se identifica mediante un [*URI*](windows-remote-management-glossary.md), al igual que cualquier otro recurso cuando se usa el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="1357a-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="1357a-113">El URI puede especificar un recurso de WMI (clase), una acción de WMI (método) o identificar una instancia específica de una clase en [*los mensajes*](windows-remote-management-glossary.md) enviados a través de una red.</span><span class="sxs-lookup"><span data-stu-id="1357a-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="1357a-114">Para obtener más información, vea [URI de recursos](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="1357a-115">Construir el prefijo URI para clases WMI</span><span class="sxs-lookup"><span data-stu-id="1357a-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="1357a-116">El prefijo URI contiene una parte fija y el espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="1357a-117">Por ejemplo, el prefijo URI en Windows Server que contiene la parte fija del prefijo es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="1357a-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="1357a-118">Esto permite generar el prefijo de URI para cualquier espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="1357a-119">Por ejemplo, para tener acceso al espacio de nombres WMI **\\ predeterminado raíz** , use el siguiente prefijo de URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="1357a-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="1357a-120">La mayoría de las clases WMI para la administración se encuentran en el espacio de nombres **root \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="1357a-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="1357a-121">Para tener acceso a las clases e instancias del espacio de nombres **root \\ cimv2** , use el prefijo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="1357a-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="1357a-122">Para obtener más información, vea [URI de recursos](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="1357a-123">Generar un URI completo para clases WMI</span><span class="sxs-lookup"><span data-stu-id="1357a-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="1357a-124">El URI que proporcione, ya sea a la herramienta de línea de comandos de **WinRM** o a un script, consta del prefijo más la especificación de recursos.</span><span class="sxs-lookup"><span data-stu-id="1357a-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="1357a-125">En el procedimiento siguiente se describe cómo generar un URI de recurso para obtener una clase WMI o para usarla en una operación de enumeración.</span><span class="sxs-lookup"><span data-stu-id="1357a-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="1357a-126">**Para generar un URI de recurso para una clase WMI**</span><span class="sxs-lookup"><span data-stu-id="1357a-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="1357a-127">Comience con el prefijo que indica que se debe usar el esquema de protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="1357a-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="1357a-128">El prefijo de URI de recurso para las clases WMI siempre es el mismo.</span><span class="sxs-lookup"><span data-stu-id="1357a-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="1357a-129">Para obtener más información, vea [prefijos de URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="1357a-130">Agregue el espacio de nombres WMI al prefijo.</span><span class="sxs-lookup"><span data-stu-id="1357a-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="1357a-131">Agregue el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="1357a-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="1357a-132">Para establecer el valor de una propiedad, o para invocar un método específico, agregue el valor o los valores de clave necesarios para la clase.</span><span class="sxs-lookup"><span data-stu-id="1357a-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="1357a-133">Si deja el valor de clave en blanco, no modificará el valor de la propiedad original.</span><span class="sxs-lookup"><span data-stu-id="1357a-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="1357a-134">Si se deja el valor de clave en blanco, el valor de la propiedad se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="1357a-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="1357a-135">Localizar un recurso WMI con WinRM</span><span class="sxs-lookup"><span data-stu-id="1357a-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="1357a-136">Puede obtener datos de WMI a través de la herramienta de línea de comandos, **WinRM** o a través de un script de Visual Basic que use la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="1357a-137">No se usa una [ruta de acceso WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) para buscar un recurso.</span><span class="sxs-lookup"><span data-stu-id="1357a-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="1357a-138">En su lugar, convierta el espacio de nombres y la jerarquía de WMI a un [*URI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="1357a-139">El URI de WinRM de una clase WMI contiene dos partes: el [Prefijo de URI](uri-prefixes.md) y la clase a la que desea obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="1357a-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="1357a-140">Por ejemplo, se puede proporcionar el siguiente URI al método [**Session. Enumerate**](session-enumerate.md) para enumerar todos los servicios de un equipo.</span><span class="sxs-lookup"><span data-stu-id="1357a-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="1357a-141">El prefijo URI es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` y la clase es [**el \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="1357a-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="1357a-142">En WMI, enumere los datos de todas las instancias de un recurso o clase de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="1357a-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="1357a-143">Una consulta para todas las instancias de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="1357a-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="1357a-144">Una llamada a [**SWbemServices. instances**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject. \_ instances**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="1357a-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="1357a-145">En WinRM, hay una manera de enumerar todas las instancias de un recurso: [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="1357a-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="1357a-146">Buscar una instancia específica de un recurso WMI</span><span class="sxs-lookup"><span data-stu-id="1357a-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="1357a-147">En WMI, puede designar una instancia determinada de una clase especificando valores para las propiedades de clave o consultando una instancia que coincida con una lista de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1357a-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="1357a-148">Las propiedades de clave tienen el [**calificador de clave**](/windows/desktop/WmiSdk/key-qualifier)de WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="1357a-149">Puede obtener una instancia específica de una clase de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="1357a-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="1357a-150">Una llamada a [**Session. Enumerate**](session-enumerate.md) con los parámetros *Filter* y *Dialect* para crear una consulta.</span><span class="sxs-lookup"><span data-stu-id="1357a-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="1357a-151">Una llamada a [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="1357a-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="1357a-152">Para [**Session. Get**](session-get.md), debe proporcionar uno o varios valores de clave específicos, precedidos de un signo de interrogación (?).</span><span class="sxs-lookup"><span data-stu-id="1357a-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="1357a-153">El formato del URI para una instancia específica es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="1357a-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="1357a-154">Una clase WMI puede tener más de una clave.</span><span class="sxs-lookup"><span data-stu-id="1357a-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="1357a-155">Los pares de nombre y valor de clave se separan con un signo "+".</span><span class="sxs-lookup"><span data-stu-id="1357a-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="1357a-156">En ese caso, el formato es: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="1357a-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="1357a-157">La sintaxis de WinRM para obtener un objeto WMI singleton es diferente de la de WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="1357a-158">Un singleton es una clase WMI definida para que solo se permita una instancia.</span><span class="sxs-lookup"><span data-stu-id="1357a-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="1357a-159">[**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) son ejemplos de una clase singleton de WMI.</span><span class="sxs-lookup"><span data-stu-id="1357a-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="1357a-160">La sintaxis de WMI para singletons se muestra en el siguiente ejemplo de código de VBScript.</span><span class="sxs-lookup"><span data-stu-id="1357a-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="1357a-161">En el ejemplo siguiente se muestra la sintaxis singleton de WinRM que no usa "@".</span><span class="sxs-lookup"><span data-stu-id="1357a-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="1357a-162">Agregar un [*selector*](windows-remote-management-glossary.md) a un objeto [**ResourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .</span><span class="sxs-lookup"><span data-stu-id="1357a-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="1357a-163">En el ejemplo de código de VBScript siguiente se muestra cómo utilizar un selector para obtener una instancia específica del [**\_ procesador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="1357a-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1357a-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1357a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1357a-165">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="1357a-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="1357a-166">Prefijos de URI</span><span class="sxs-lookup"><span data-stu-id="1357a-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="1357a-167">URI de recursos</span><span class="sxs-lookup"><span data-stu-id="1357a-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="1357a-168">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="1357a-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
