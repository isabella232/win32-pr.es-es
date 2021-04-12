---
description: Instrumental de administración de Windows (WMI) es la implementación de Microsoft de Web-Based Enterprise Management (WBEM), que es una iniciativa industrial para desarrollar una tecnología estándar que permita el acceso a información de administración en un entorno empresarial.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: Acerca de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361282"
---
# <a name="about-wmi"></a>Acerca de WMI

Instrumental de administración de Windows (WMI) es la implementación de Microsoft de Web-Based Enterprise Management (WBEM), que es una iniciativa industrial para desarrollar una tecnología estándar que permita el acceso a información de administración en un entorno empresarial. WMI utiliza la norma de la industria CIM (Modelo de información común) para representar sistemas, aplicaciones, redes, dispositivos y otros componentes administrados. El equipo de administración distribuida ([DMTF](https://www.dmtf.org/standards/wsman)) desarrolla y mantiene CIM.

> [!Note]  
> La próxima generación de WMI, conocida como Windows Management Infrastructure (MI), está disponible actualmente. MI es totalmente compatible con las versiones anteriores de WMI y proporciona un host de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes. Por ejemplo, muchos proveedores más recientes se escriben con el marco de trabajo de MI, pero se puede tener acceso a ellos mediante scripts y aplicaciones WMI. Para obtener más información acerca de las diferencias entre las dos tecnologías, consulte [¿por qué usar mi?](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Administración de sistemas de equipos remotos con WMI

La capacidad de obtener datos de administración de equipos remotos es lo que hace que WMI sea tan útil. Las conexiones de WMI remotas se establecen a través de DCOM. Una alternativa es usar Administración remota de Windows ([WinRM](/windows/desktop/WinRM/portal)), que obtiene datos de administración de WMI remotos mediante el protocolo basado en SOAP WS-Management.

## <a name="programming-with-wmi"></a>Programar con WMI

Las aplicaciones o los scripts de administración pueden obtener datos o realizar operaciones a través de WMI en diversos lenguajes. Para obtener más información, consulte la sección audiencia para desarrolladores en [instrumental de administración de Windows](wmi-start-page.md).

Muchas características de Windows tienen proveedores WMI asociados, como el [proveedor de datos de la configuración de arranque (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) o el [proveedor de volumen de almacenamiento](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). Los proveedores de WMI implementan la funcionalidad descrita por métodos y propiedades de clases de WMI para administrar las características de Windows asociadas. Para obtener más información, vea [proveedores WMI](wmi-providers.md) y [clases WMI](wmi-classes.md).

Para obtener más información acerca de cómo escribir un proveedor para proporcionar datos de nuevas aplicaciones o hardware, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).

Para obtener más información sobre cómo implementar esta tecnología, consulte [usar WMI](using-wmi.md).

En la tabla siguiente se enumeran los temas incluidos en esta sección.



| Sección                                                                                                | Descripción                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de WMI](what-s-new-in-wmi.md)                                                             | Nuevas características de WMI.                                                                                                                                                                                                                              |
| [Disponibilidad del sistema operativo de los componentes WMI](operating-system-availability-of-wmi-components.md) | Algunos componentes ya no están disponibles o están disponibles como una instalación opcional.                                                                                                                                                             |
| [Arquitectura de WMI](wmi-architecture.md)                                                               | Una aplicación de administración se comunica con WMI mediante el uso de una variedad de interfaces, como Visual Basic, C++, ODBC y ActiveX. Todas las interfaces WMI se basan en el modelo de objetos componentes (COM).                                              |
| [Modelo de información común](common-information-model.md)                                               | Modelo de programación independiente del lenguaje que utiliza técnicas orientadas a objetos para describir una empresa.                                                                                                                                          |
| [Managed Object Format](managed-object-format--mof-.md)                                               | Formato que permite crear código legible, que el sistema operativo puede traducir en un conjunto de clases CIM. Puede utilizar las nuevas clases para modelar y controlar nuevas tecnologías para una empresa.                                 |
| [Control de cuentas de usuario y WMI](user-account-control-and-wmi.md)                                       | Control de cuentas de usuario (UAC) afecta a los datos de WMI que se devuelven, el acceso remoto y el modo en que se deben ejecutar los scripts. Para obtener más información, vea [Introducción con control de cuentas de usuario en Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md)                                 | WMI utiliza objetos y procedimientos de seguridad de Windows estándar para controlar y proteger el acceso a objetos protegibles como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM.                                                                      |
| [Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)                                     | Los datos de los contadores de rendimiento del sistema están disponibles en las clases de WMI.                                                                                                                                                                            |
| [Compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | Las clases de red y del [proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) de WMI proporcionan datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.                                       |
| [Formato de fecha y hora](date-and-time-format.md)                                                       | WMI usa los formatos de fecha y hora definidos por la especificación CIM del forzado de la tarea de administración distribuida. Para obtener más información, consulte [DMTF](https://www.dmtf.org/).                                                          |
| [Acceso de script a WMI](scripting-access-to-wmi.md)                                                 | Escribir scripts de WMI para realizar tareas de administración.                                                                                                                                                                                                    |
| [Solución de problemas de WMI](wmi-troubleshooting.md)                                                         | Al tener acceso a los datos locales o remotos de WMI en una aplicación o un script, es posible que reciba errores que van desde clases que faltan a acceso denegado. Los proveedores también tienen opciones de depuración y clases de solución de problemas disponibles.                           |
| [Información adicional](further-information.md)                                                         | Sitios web, libros y artículos sobre WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
