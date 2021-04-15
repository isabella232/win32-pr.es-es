---
description: WMI proporciona una interfaz uniforme para todas las aplicaciones o scripts locales o remotos que obtienen datos de administración de un sistema informático, una red o una empresa.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Arquitectura de WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570163"
---
# <a name="wmi-architecture"></a><span data-ttu-id="20cb1-103">Arquitectura de WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-103">WMI Architecture</span></span>

<span data-ttu-id="20cb1-104">WMI proporciona una interfaz uniforme para todas las aplicaciones o scripts locales o remotos que obtienen datos de administración de un sistema informático, una red o una empresa.</span><span class="sxs-lookup"><span data-stu-id="20cb1-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="20cb1-105">La interfaz uniforme está diseñada para que las aplicaciones de cliente WMI y los scripts no tengan que llamar a una amplia variedad de interfaces de programación de aplicaciones (API) del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="20cb1-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="20cb1-106">No se puede llamar a muchas API mediante clientes de automatización como scripts o aplicaciones Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="20cb1-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="20cb1-107">Otras API no realizan llamadas a equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="20cb1-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="20cb1-108">Para obtener datos de WMI, escriba un script o una aplicación de cliente que tenga acceso a [las clases WMI](wmi-classes.md) o proporcione datos a WMI escribiendo un [*proveedor WMI*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="20cb1-109">Para obtener más información, vea [usar WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="20cb1-110">Objetos, consumidores y infraestructura de WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="20cb1-111">En el diagrama siguiente se muestra la relación entre la infraestructura WMI y los proveedores WMI y los objetos administrados, y también se muestra la relación entre la infraestructura WMI y los consumidores WMI.</span><span class="sxs-lookup"><span data-stu-id="20cb1-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![relación entre la infraestructura de WMI, los proveedores de WMI y los objetos administrados](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="20cb1-113">Componentes WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-113">WMI Components</span></span>

<span data-ttu-id="20cb1-114">En la lista siguiente se describen los componentes clave de WMI:</span><span class="sxs-lookup"><span data-stu-id="20cb1-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="20cb1-115">Objetos administrados y proveedores de WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="20cb1-116">Un proveedor WMI es un objeto COM que supervisa uno o más [*objetos administrados*](gloss-m.md) para WMI.</span><span class="sxs-lookup"><span data-stu-id="20cb1-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="20cb1-117">Un objeto administrado es un componente de empresa físico o lógico, como una unidad de disco duro, un adaptador de red, un sistema de base de datos, un sistema operativo, un proceso o un servicio.</span><span class="sxs-lookup"><span data-stu-id="20cb1-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="20cb1-118">De forma similar a un controlador, un proveedor proporciona a WMI datos de un objeto administrado y controla los mensajes de WMI en el objeto administrado.</span><span class="sxs-lookup"><span data-stu-id="20cb1-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="20cb1-119">Los proveedores WMI constan de un archivo DLL y un archivo [*Managed Object Format (MOF)*](gloss-m.md) que define las clases para las que el proveedor devuelve datos y realiza operaciones.</span><span class="sxs-lookup"><span data-stu-id="20cb1-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="20cb1-120">Los proveedores, como las aplicaciones de C++ de WMI, utilizan la [API de com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="20cb1-121">Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="20cb1-122">Un ejemplo de un proveedor es el [proveedor del registro](/previous-versions/windows/desktop/regprov/system-registry-provider)preinstalado, que tiene acceso a los datos del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="20cb1-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="20cb1-123">El proveedor del registro tiene una [*clase WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), con muchos métodos pero sin propiedades.</span><span class="sxs-lookup"><span data-stu-id="20cb1-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="20cb1-124">Otros proveedores preinstalados, como el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider), suelen tener clases con muchas propiedades, pero con pocos métodos, como el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) o el [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="20cb1-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="20cb1-125">El archivo DLL del proveedor del registro, Stdprov.dll, contiene el código que devuelve datos dinámicamente cuando los solicitan las aplicaciones o scripts de cliente.</span><span class="sxs-lookup"><span data-stu-id="20cb1-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="20cb1-126">Los archivos MOF y DLL de WMI se encuentran en% WINDIR% \\ system32 \\ WBEM, junto con las [herramientas de Command-Line de wmi](wmi-command-line-tools.md), como [**Winmgmt.exe**](winmgmt.md) y [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="20cb1-127">Las clases de proveedor, como [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), se definen en archivos MOF y, a continuación, se compilan en el repositorio WMI al iniciarse el sistema.</span><span class="sxs-lookup"><span data-stu-id="20cb1-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="20cb1-128">Infraestructura WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="20cb1-129">La infraestructura WMI es un componente del sistema operativo Microsoft Windows conocido como servicio WMI (WinMgmt).</span><span class="sxs-lookup"><span data-stu-id="20cb1-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="20cb1-130">La infraestructura WMI tiene dos componentes: el núcleo WMI y el [*repositorio WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="20cb1-131">El repositorio WMI está organizado por [*espacios de nombres*](gloss-n.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="20cb1-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="20cb1-132">El servicio WMI crea algunos espacios de nombres como \\ la raíz predeterminada, la raíz \\ cimv2 y \\ la suscripción raíz al iniciar el sistema y preinstala un conjunto predeterminado de definiciones de clase, incluidas las [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider), las [clases del sistema WMI](wmi-system-classes.md)y otras.</span><span class="sxs-lookup"><span data-stu-id="20cb1-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="20cb1-133">El resto de los espacios de nombres que se encuentran en el sistema se crean mediante proveedores para otras partes del sistema operativo o de los productos.</span><span class="sxs-lookup"><span data-stu-id="20cb1-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="20cb1-134">Para obtener más información y una lista de los proveedores de WMI que se encuentran en la mayoría de las versiones del sistema operativo, consulte [proveedores de WMI](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="20cb1-135">El servicio WMI actúa como intermediario entre los proveedores, las aplicaciones de administración y el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="20cb1-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="20cb1-136">Solo los datos estáticos sobre objetos se almacenan en el repositorio, como las clases definidas por los proveedores.</span><span class="sxs-lookup"><span data-stu-id="20cb1-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="20cb1-137">WMI obtiene la mayoría de los datos dinámicamente del proveedor cuando un cliente lo solicita.</span><span class="sxs-lookup"><span data-stu-id="20cb1-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="20cb1-138">También puede configurar suscripciones para recibir notificaciones de eventos de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="20cb1-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="20cb1-139">Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="20cb1-140">Consumidores de WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-140">WMI consumers</span></span>

    <span data-ttu-id="20cb1-141">Un consumidor WMI es una aplicación de administración o un script que interactúa con la infraestructura WMI.</span><span class="sxs-lookup"><span data-stu-id="20cb1-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="20cb1-142">Una aplicación de administración puede consultar, enumerar datos, ejecutar métodos de proveedor o suscribirse a eventos mediante una llamada a la [API com para WMI](com-api-for-wmi.md) o la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="20cb1-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="20cb1-143">Los únicos datos o acciones disponibles para un objeto administrado, como una unidad de disco o un servicio, son los que proporciona un proveedor.</span><span class="sxs-lookup"><span data-stu-id="20cb1-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20cb1-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20cb1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20cb1-145">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="20cb1-146">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="20cb1-147">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="20cb1-148">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="20cb1-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="20cb1-149">Proporcionar datos a WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="20cb1-150">Clases WMI</span><span class="sxs-lookup"><span data-stu-id="20cb1-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="20cb1-151">Supervisión de eventos</span><span class="sxs-lookup"><span data-stu-id="20cb1-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="20cb1-152">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="20cb1-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
