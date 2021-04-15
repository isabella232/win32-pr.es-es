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
# <a name="wmi-architecture"></a>Arquitectura de WMI

WMI proporciona una interfaz uniforme para todas las aplicaciones o scripts locales o remotos que obtienen datos de administración de un sistema informático, una red o una empresa. La interfaz uniforme está diseñada para que las aplicaciones de cliente WMI y los scripts no tengan que llamar a una amplia variedad de interfaces de programación de aplicaciones (API) del sistema operativo. No se puede llamar a muchas API mediante clientes de automatización como scripts o aplicaciones Visual Basic. Otras API no realizan llamadas a equipos remotos.

Para obtener datos de WMI, escriba un script o una aplicación de cliente que tenga acceso a [las clases WMI](wmi-classes.md) o proporcione datos a WMI escribiendo un [*proveedor WMI*](gloss-p.md). Para obtener más información, vea [usar WMI](using-wmi.md).

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objetos, consumidores y infraestructura de WMI

En el diagrama siguiente se muestra la relación entre la infraestructura WMI y los proveedores WMI y los objetos administrados, y también se muestra la relación entre la infraestructura WMI y los consumidores WMI.

![relación entre la infraestructura de WMI, los proveedores de WMI y los objetos administrados](images/wmi-architecture.png)

## <a name="wmi-components"></a>Componentes WMI

En la lista siguiente se describen los componentes clave de WMI:

-   Objetos administrados y proveedores de WMI

    Un proveedor WMI es un objeto COM que supervisa uno o más [*objetos administrados*](gloss-m.md) para WMI. Un objeto administrado es un componente de empresa físico o lógico, como una unidad de disco duro, un adaptador de red, un sistema de base de datos, un sistema operativo, un proceso o un servicio.

    De forma similar a un controlador, un proveedor proporciona a WMI datos de un objeto administrado y controla los mensajes de WMI en el objeto administrado. Los proveedores WMI constan de un archivo DLL y un archivo [*Managed Object Format (MOF)*](gloss-m.md) que define las clases para las que el proveedor devuelve datos y realiza operaciones. Los proveedores, como las aplicaciones de C++ de WMI, utilizan la [API de com para WMI](com-api-for-wmi.md). Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).

    Un ejemplo de un proveedor es el [proveedor del registro](/previous-versions/windows/desktop/regprov/system-registry-provider)preinstalado, que tiene acceso a los datos del registro del sistema. El proveedor del registro tiene una [*clase WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), con muchos métodos pero sin propiedades. Otros proveedores preinstalados, como el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider), suelen tener clases con muchas propiedades, pero con pocos métodos, como el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) o el [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). El archivo DLL del proveedor del registro, Stdprov.dll, contiene el código que devuelve datos dinámicamente cuando los solicitan las aplicaciones o scripts de cliente.

    Los archivos MOF y DLL de WMI se encuentran en% WINDIR% \\ system32 \\ WBEM, junto con las [herramientas de Command-Line de wmi](wmi-command-line-tools.md), como [**Winmgmt.exe**](winmgmt.md) y [**Mofcomp.exe**](mofcomp.md). Las clases de proveedor, como [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), se definen en archivos MOF y, a continuación, se compilan en el repositorio WMI al iniciarse el sistema.

-   [Infraestructura WMI](wmi-infrastructure.md)

    La infraestructura WMI es un componente del sistema operativo Microsoft Windows conocido como servicio WMI (WinMgmt). La infraestructura WMI tiene dos componentes: el núcleo WMI y el [*repositorio WMI*](gloss-w.md).

    El repositorio WMI está organizado por [*espacios de nombres*](gloss-n.md)WMI. El servicio WMI crea algunos espacios de nombres como \\ la raíz predeterminada, la raíz \\ cimv2 y \\ la suscripción raíz al iniciar el sistema y preinstala un conjunto predeterminado de definiciones de clase, incluidas las [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider), las [clases del sistema WMI](wmi-system-classes.md)y otras. El resto de los espacios de nombres que se encuentran en el sistema se crean mediante proveedores para otras partes del sistema operativo o de los productos. Para obtener más información y una lista de los proveedores de WMI que se encuentran en la mayoría de las versiones del sistema operativo, consulte [proveedores de WMI](wmi-providers.md).

    El servicio WMI actúa como intermediario entre los proveedores, las aplicaciones de administración y el repositorio WMI. Solo los datos estáticos sobre objetos se almacenan en el repositorio, como las clases definidas por los proveedores. WMI obtiene la mayoría de los datos dinámicamente del proveedor cuando un cliente lo solicita. También puede configurar suscripciones para recibir notificaciones de eventos de un proveedor. Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).

-   Consumidores de WMI

    Un consumidor WMI es una aplicación de administración o un script que interactúa con la infraestructura WMI. Una aplicación de administración puede consultar, enumerar datos, ejecutar métodos de proveedor o suscribirse a eventos mediante una llamada a la [API com para WMI](com-api-for-wmi.md) o la [API de scripting para WMI](scripting-api-for-wmi.md). Los únicos datos o acciones disponibles para un objeto administrado, como una unidad de disco o un servicio, son los que proporciona un proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> <dt>

[Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Clases WMI](wmi-classes.md)
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
