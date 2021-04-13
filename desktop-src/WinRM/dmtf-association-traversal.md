---
title: Detección de perfiles DMTF a través de cruce seguro de asociaciones
description: Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421519"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="9fc76-103">Detección de perfiles DMTF a través de cruce seguro de asociaciones</span><span class="sxs-lookup"><span data-stu-id="9fc76-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="9fc76-104">Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema.</span><span class="sxs-lookup"><span data-stu-id="9fc76-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="9fc76-105">El modelo se ajusta a un estándar mantenido por el equipo de tareas de administración de escritorio ([DMTF](https://www.dmtf.org/standards/wsman)) y se conoce como modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="9fc76-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="9fc76-106">Algunas clases del modelo, como archivo de [ \_ archivos CIM](../cimwin32prov/cim-datafile.md) o [ \_ proceso de Win32](../cimwin32prov/win32-process.md), se corresponden directamente con entidades administrables.</span><span class="sxs-lookup"><span data-stu-id="9fc76-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="9fc76-107">Otras clases del modelo, como SystemServices de [Win32 \_ ](../cimwin32prov/win32-systemservices.md), representan las relaciones entre las entidades administrables.</span><span class="sxs-lookup"><span data-stu-id="9fc76-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="9fc76-108">Estas clases de modelado de relaciones se conocen como clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="9fc76-109">Mediante el lenguaje de consulta específico de WMI, WQL, puede recuperar instancias de clases que representan entidades administrables o instancias de clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="9fc76-110">Pero WQL es específico de la implementación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-110">But WQL is implementation specific.</span></span> <span data-ttu-id="9fc76-111">Solo funciona con la implementación de Windows del estándar DMTF (WMI).</span><span class="sxs-lookup"><span data-stu-id="9fc76-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="9fc76-112">Además, la sintaxis de WQL para recuperar clases de asociación es bastante complicada.</span><span class="sxs-lookup"><span data-stu-id="9fc76-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="9fc76-113">La infraestructura de Administración remota de Windows (WinRM) proporciona una manera excelente de aprovechar la funcionalidad de WMI.</span><span class="sxs-lookup"><span data-stu-id="9fc76-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="9fc76-114">Las primeras versiones de WinRM tenían que usar WQL para recuperar instancias de clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="9fc76-115">WinRM 2,0 incluye una nueva característica conocida como detección de perfiles de DMTF a través de cruce seguro de asociaciones.</span><span class="sxs-lookup"><span data-stu-id="9fc76-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="9fc76-116">El cruce seguro de asociaciones permite que un usuario de WinRM recupere instancias de clases de asociación mediante un mecanismo de filtrado estándar, el dialecto AssociationFilter, definido en la especificación de enlace CIM de DMTF.</span><span class="sxs-lookup"><span data-stu-id="9fc76-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="9fc76-117">Para obtener más información sobre el recorrido de asociación, vea el WS-Management especificación de enlace de CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="9fc76-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="9fc76-118">La utilidad WinRM proporciona un mecanismo sencillo para atravesar la Asociación adecuada y recuperar un perfil de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fc76-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="9fc76-119">Detalles de la implementación de configuración</span><span class="sxs-lookup"><span data-stu-id="9fc76-119">Configuration Implementation Details</span></span>

<span data-ttu-id="9fc76-120">La utilidad WinRM admite ahora un dialecto para la solicitud de asociación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="9fc76-121">Se puede especificar el URI o el alias mediante la utilidad WinRM.</span><span class="sxs-lookup"><span data-stu-id="9fc76-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="9fc76-122">Alias</span><span class="sxs-lookup"><span data-stu-id="9fc76-122">Alias</span></span>       | <span data-ttu-id="9fc76-123">URI</span><span class="sxs-lookup"><span data-stu-id="9fc76-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fc76-124">correlación</span><span class="sxs-lookup"><span data-stu-id="9fc76-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="9fc76-125">Recuperar instancias de una clase de asociación mediante el dialecto AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="9fc76-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="9fc76-126">La utilidad WinRM puede recuperar instancias de clase de asociación WMI de una instancia de origen determinada.</span><span class="sxs-lookup"><span data-stu-id="9fc76-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="9fc76-127">El siguiente comando muestra cómo usar la utilidad WinRM para recuperar instancias de clases de Asociación de [ \_ servicio Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc76-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="9fc76-128">El modificador "-Associations" se debe usar para devolver clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="9fc76-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="9fc76-129">**WinRM Enumerate wmicimv2/ \* -Dialect: Association-Associations-Filter: {Object = \_ servicio Win32? Name = WinRM; resultclassname = Win32 \_ dependentservice; role = dependent}**</span><span class="sxs-lookup"><span data-stu-id="9fc76-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="9fc76-130">El siguiente fragmento de código basado en texto es la salida del comando anterior:</span><span class="sxs-lookup"><span data-stu-id="9fc76-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="9fc76-131">Recuperar instancias de una clase asociada mediante el dialecto AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="9fc76-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="9fc76-132">La utilidad WinRM puede recuperar instancias de clase WMI asociadas a una instancia de origen determinada.</span><span class="sxs-lookup"><span data-stu-id="9fc76-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="9fc76-133">El siguiente comando muestra cómo usar la utilidad WinRM para recuperar instancias de las clases asociadas del [ \_ servicio Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc76-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="9fc76-134">**WinRM Enumerate wmicimv2/ \* -Dialect: Association-Filter: {Object = \_ servicio Win32? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; resultrole = antecedente; role = dependent}**</span><span class="sxs-lookup"><span data-stu-id="9fc76-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="9fc76-135">El siguiente fragmento de código basado en texto es la salida del comando anterior:</span><span class="sxs-lookup"><span data-stu-id="9fc76-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 