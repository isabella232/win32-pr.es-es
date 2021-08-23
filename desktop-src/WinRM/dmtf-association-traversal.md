---
title: Detección de perfiles DMTF mediante el recorrido de asociación
description: Un componente clave de la infraestructura Windows Management Instrumentation (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f49d1433d8263dff2c1d50007f9aa0daf1573c09ebc8d7a513eda658c51997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643155"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Detección de perfiles DMTF mediante el recorrido de asociación

Un componente clave de la infraestructura Windows Management Instrumentation (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema. El modelo se ajusta a un estándar mantenido por el Grupo de tareas de administración de escritorio[(DMTF)](https://www.dmtf.org/standards/wsman)y se conoce como Modelo de información común (CIM). Algunas clases del modelo, como [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) o [Win32 \_ Process,](../cimwin32prov/win32-process.md)se corresponden directamente con entidades administrables. Otras clases del modelo, como [ \_ SystemServices de Win32,](../cimwin32prov/win32-systemservices.md)representan relaciones entre entidades administrables. Estas clases de modelado de relaciones se conocen como clases de asociación.

Con el lenguaje de consulta específico de WMI, WQL, puede recuperar instancias de clases que representan entidades administrables o instancias de clases association. Pero WQL es específico de la implementación. Solo funciona con la implementación Windows del estándar DMTF (WMI). Además, la sintaxis de WQL para recuperar clases de asociación es bastante complicada.

La Windows administración remota remota (WinRM) proporciona una manera excelente de aprovechar la funcionalidad de WMI. Las primeras versiones de WinRM tenían que usar WQL para recuperar instancias de clases association. WinRM 2.0 incluye una nueva característica conocida como detección de perfiles DMTF a través del recorrido de asociación. El recorrido de asociación permite a un usuario de WinRM recuperar instancias de clases association mediante un mecanismo de filtrado estándar, el dialecto AssociationFilter, definido en la especificación de enlace CIM de DMTF. Para obtener más información sobre el recorrido de asociación, vea la especificación WS-Management enlace CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

La utilidad winrm proporciona un mecanismo sencillo para recorrer la asociación adecuada y recuperar un perfil de dispositivo.

## <a name="configuration-implementation-details"></a>Detalles de implementación de configuración

La utilidad winrm ahora admite un dialecto para la solicitud de asociación. El URI o el alias se pueden especificar mediante la utilidad winrm.



| Alias       | Identificador URI                                                               |
|-------------|-------------------------------------------------------------------|
| correlación | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recuperar instancias de una clase de asociación mediante el dialecto AssociationFilter

La utilidad winrm puede recuperar instancias de clase de asociación WMI de una instancia de origen determinada. El siguiente comando muestra cómo usar la utilidad winrm para recuperar instancias de clases de asociación del servicio [Win32. \_ ](../cimwin32prov/win32-service.md) El modificador "-associations" debe usarse para devolver clases de asociación.

**winrm enumerate wmicimv2/ \* -dialect:association -associations -filter:{object=win32 \_ service?name=winrm;resultclassname=win32 \_ dependentservice;role=dependent}**

El siguiente fragmento de código basado en texto es la salida del comando anterior:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Recuperar instancias de una clase asociada mediante el dialecto AssociationFilter

La utilidad winrm puede recuperar instancias de clase WMI asociadas a una instancia de origen determinada. El siguiente comando muestra cómo usar la utilidad winrm para recuperar instancias de clases asociadas al servicio [Win32. \_ ](../cimwin32prov/win32-service.md)

**winrm enumerate wmicimv2/ \* -dialect:association -filter:{object=win32 \_ service?name=winrm;associationclassname=win32 \_ dependentservice;resultclassname=win32 \_ service;resultrole=antecedent;role=dependent}**

El siguiente fragmento de código basado en texto es la salida del comando anterior:

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

 

 