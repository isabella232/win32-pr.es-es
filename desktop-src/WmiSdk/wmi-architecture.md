---
description: WMI proporciona una interfaz uniforme para las aplicaciones o scripts locales o remotos que obtienen datos de administración de un sistema informático, una red o una empresa.
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
ms.openlocfilehash: e261459785fa4e0ccdce7337df788de007c6f335799bbe4778e80f551f5e519e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995535"
---
# <a name="wmi-architecture"></a>Arquitectura de WMI

WMI proporciona una interfaz uniforme para las aplicaciones o scripts locales o remotos que obtienen datos de administración de un sistema informático, una red o una empresa. La interfaz uniforme está diseñada de forma que los scripts y las aplicaciones cliente WMI no tengan que llamar a una amplia variedad de interfaces de programación de aplicaciones (API) del sistema operativo. Muchos clientes de automatización no pueden llamar a muchas API, como scripts o Visual Basic aplicaciones. Otras API no hacen llamadas a equipos remotos.

Para obtener datos de WMI, escriba un script de cliente o una aplicación que acceda a clases [WMI](wmi-classes.md) o proporcione datos a WMI escribiendo un [*proveedor WMI*](gloss-p.md). Para obtener más información, vea [Usar WMI.](using-wmi.md)

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objetos, consumidores e infraestructura de WMI

En el diagrama siguiente se muestra la relación entre la infraestructura WMI y los proveedores wmi y los objetos administrados, y también se muestra la relación entre la infraestructura WMI y los consumidores wmi.

![relación entre la infraestructura wmi, los proveedores wmi y los objetos administrados](images/wmi-architecture.png)

## <a name="wmi-components"></a>Componentes wmi

En la lista siguiente se describen los componentes clave de WMI:

-   Objetos administrados y proveedores WMI

    Un proveedor WMI es un objeto COM que supervisa uno o varios [*objetos administrados*](gloss-m.md) para WMI. Un objeto administrado es un componente empresarial lógico o físico, como una unidad de disco duro, un adaptador de red, un sistema de base de datos, un sistema operativo, un proceso o un servicio.

    De forma similar a un controlador, un proveedor proporciona WMI con datos de un objeto administrado y controla los mensajes de WMI al objeto administrado. Los proveedores WMI constan de un archivo DLL y un archivo [*Managed Object Format (MOF)*](gloss-m.md) que define las clases para las que el proveedor devuelve datos y realiza operaciones. Los proveedores, como las aplicaciones wmi de C++, usan la [API COM para WMI.](com-api-for-wmi.md) Para obtener más información, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

    Un ejemplo de un proveedor es el proveedor del [Registro preinstalado](/previous-versions/windows/desktop/regprov/system-registry-provider), que tiene acceso a los datos del registro del sistema. El proveedor del Registro tiene una [*clase WMI,*](gloss-w.md) [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov)con muchos métodos pero sin propiedades. Otros proveedores preinstalados, como el proveedor [Win32,](/windows/desktop/CIMWin32Prov/win32-provider)suelen tener clases con muchas propiedades, pero pocos métodos, como [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) o [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). El archivo DLL del proveedor del Registro, Stdprov.dll, contiene el código que devuelve dinámicamente los datos cuando lo solicitan las aplicaciones o scripts de cliente.

    Los archivos MOF y DLL de WMI se encuentran en %WINDIR% \\ System32 \\ Wbem, [](winmgmt.md) [****](mofcomp.md)junto con wmi [Command-Line Tools](wmi-command-line-tools.md), comoWinmgmt.exeyMofcomp.exe. Las clases de proveedor, como [**\_ Win32 LogicalDisk,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)se definen en archivos MOF y, a continuación, se compilan en el repositorio WMI al iniciar el sistema.

-   [Infraestructura wmi](wmi-infrastructure.md)

    La infraestructura WMI es un componente Windows sistema operativo de Microsoft conocido como servicio WMI(winmgmt). La infraestructura wmi tiene dos componentes: el núcleo de WMI y el [*repositorio wmi*](gloss-w.md).

    El repositorio WMI está organizado por espacios [*de nombres WMI.*](gloss-n.md) El servicio WMI crea algunos espacios de nombres, como root default, root cimv2 y root subscription al iniciar el sistema, y preinstala un conjunto predeterminado de definiciones de clase, incluidas las clases Win32 , las clases del sistema WMI y \\ \\ \\ otras. [](/windows/desktop/CIMWin32Prov/win32-provider) [](wmi-system-classes.md) Los restantes espacios de nombres que se encuentran en el sistema los crean proveedores para otras partes del sistema operativo o productos. Para obtener más información y una lista de los proveedores WMI que se encuentran en la mayoría de las versiones del sistema operativo, vea [Proveedores WMI](wmi-providers.md).

    El servicio WMI actúa como intermediario entre los proveedores, las aplicaciones de administración y el repositorio WMI. Solo los datos estáticos sobre objetos se almacenan en el repositorio, como las clases definidas por los proveedores. WMI obtiene la mayoría de los datos dinámicamente del proveedor cuando un cliente lo solicita. También puede configurar suscripciones para recibir notificaciones de eventos de un proveedor. Para obtener más información, vea [Monitoring Events](monitoring-events.md).

-   Consumidores WMI

    Un consumidor WMI es una aplicación de administración o un script que interactúa con la infraestructura WMI. Una aplicación de administración puede consultar, enumerar datos, ejecutar métodos de proveedor o suscribirse a eventos llamando a la [API COM](com-api-for-wmi.md) para WMI o a scripting API [para WMI.](scripting-api-for-wmi.md) Los únicos datos o acciones disponibles para un objeto administrado, como una unidad de disco o un servicio, son los que proporciona un proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> <dt>

[Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Tareas wmi para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Clases WMI](wmi-classes.md)
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
