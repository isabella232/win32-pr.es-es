---
description: Instrumental de administración de Windows (WMI) es la implementación de Microsoft de Web-Based Enterprise Management (WBEM), que es una iniciativa industrial para desarrollar una tecnología estándar que permita el acceso a información de administración en un entorno empresarial.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: Acerca de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691b0584c968630a973627166f039bd718125a8a6dd124cbfed2653f3ecaedd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857565"
---
# <a name="about-wmi"></a>Acerca de WMI

Instrumental de administración de Windows (WMI) es la implementación de Microsoft de Web-Based Enterprise Management (WBEM), que es una iniciativa industrial para desarrollar una tecnología estándar que permita el acceso a información de administración en un entorno empresarial. WMI utiliza la norma de la industria CIM (Modelo de información común) para representar sistemas, aplicaciones, redes, dispositivos y otros componentes administrados. CIM es desarrollado y mantenido por el grupo de tareas de administración distribuida[(DMTF).](https://www.dmtf.org/standards/wsman)

> [!Note]  
> La próxima generación de WMI, conocida como Windows Management Infrastructure (MI), está disponible actualmente. MI es totalmente compatible con versiones anteriores de WMI y proporciona una serie de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes que nunca. Por ejemplo, muchos proveedores más recientes se escriben con el marco de trabajo de MI, pero se puede acceder a ellos mediante scripts y aplicaciones WMI. Para obtener más información sobre las diferencias entre las dos tecnologías, consulte [¿Por qué usar MI?](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Administración de sistemas de equipos remotos con WMI

La capacidad de obtener datos de administración de equipos remotos es lo que hace que WMI sea tan útil. Las conexiones de WMI remotas se establecen a través de DCOM. Una alternativa es usar Windows remote management[(WinRM),](/windows/desktop/WinRM/portal)que obtiene datos de administración wmi remota mediante el protocolo basado WS-Management SOAP.

## <a name="programming-with-wmi"></a>Programación con WMI

Las aplicaciones o scripts de administración pueden obtener datos o realizar operaciones a través de WMI en una variedad de lenguajes. Para obtener más información, consulte la sección Audiencia para desarrolladores [en Windows Management Instrumentation](wmi-start-page.md).

Muchas Windows características tienen proveedores WMI asociados, como el proveedor de datos de la configuración de arranque (BCD) [(BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) o Storage [proveedor de volúmenes](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). Los proveedores WMI implementan la funcionalidad descrita por los métodos y propiedades de las clases WMI para administrar las características Windows asociadas. Para obtener más información, vea [Proveedores WMI y](wmi-providers.md) clases [WMI](wmi-classes.md).

Para obtener más información sobre cómo escribir un proveedor para proporcionar datos de nuevas aplicaciones o hardware, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

Para obtener más información sobre cómo implementar esta tecnología, vea [Usar WMI.](using-wmi.md)

En la tabla siguiente se enumeran los temas incluidos en esta sección.



| Sección                                                                                                | Descripción                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de WMI](what-s-new-in-wmi.md)                                                             | Nuevas características de WMI.                                                                                                                                                                                                                              |
| [Disponibilidad del sistema operativo de los componentes WMI](operating-system-availability-of-wmi-components.md) | Algunos componentes ya no están disponibles o están disponibles como una instalación opcional.                                                                                                                                                             |
| [Arquitectura de WMI](wmi-architecture.md)                                                               | Una aplicación de administración se comunica con WMI mediante diversas interfaces, como Visual Basic, C++, ODBC y ActiveX. Todas las interfaces WMI se basan en el modelo de objetos componentes (COM).                                              |
| [Modelo de información común](common-information-model.md)                                               | Modelo de programación independiente del lenguaje que usa técnicas orientadas a objetos para describir una empresa.                                                                                                                                          |
| [Managed Object Format](managed-object-format--mof-.md)                                               | Formato que le permite crear código legible, que el sistema operativo puede traducir en un conjunto de clases CIM. Puede usar las nuevas clases para modelar y controlar nuevas tecnologías para una empresa.                                 |
| [Control de cuentas de usuario y WMI](user-account-control-and-wmi.md)                                       | El control de cuentas de usuario (UAC) afecta a qué datos WMI se devuelven, al acceso remoto y a cómo se deben ejecutar los scripts. Para obtener más información, [vea Tareas iniciales control de cuentas de usuario en Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Acceso a objetos protegibles wmi](access-to-wmi-securable-objects.md)                                 | WMI usa procedimientos Windows y objetos de seguridad estándar para controlar y proteger el acceso a objetos protegibles, como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM.                                                                      |
| [Bibliotecas de rendimiento y WMI](performance-libraries-and-wmi.md)                                     | Los datos de los contadores de rendimiento del sistema están disponibles en las clases WMI.                                                                                                                                                                            |
| [Compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | El proveedor [de rutas IP WMI y](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) las clases de red suministran datos para direcciones IPv4. A partir Windows Vista, WMI también proporciona compatibilidad limitada con las funcionalidades de red IPv6.                                       |
| [Formato de fecha y hora](date-and-time-format.md)                                                       | WMI usa los formatos de fecha y hora definidos por la especificación CIM del grupo de tareas de administración distribuida. Para obtener más información, vea [DMTF](https://www.dmtf.org/).                                                          |
| [Acceso de scripting a WMI](scripting-access-to-wmi.md)                                                 | Escribir scripts WMI para realizar tareas de administración.                                                                                                                                                                                                    |
| [Solución de problemas de WMI](wmi-troubleshooting.md)                                                         | Al acceder a datos locales o remotos de WMI en una aplicación o script, puede recibir errores que van desde clases que faltan hasta acceso denegado. Los proveedores también tienen disponibles opciones de depuración y clases de solución de problemas.                           |
| [Información adicional](further-information.md)                                                         | Sitios web, libros y artículos sobre WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
