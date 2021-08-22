---
description: La seguridad de WMI se centra en proteger el acceso a los datos del espacio de nombres. WMI concede primero acceso a grupos de usuarios según lo especificado por la configuración de Control WMI y DCOM y, a continuación, los proveedores determinan si el usuario debe tener acceso a los datos del espacio de nombres.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Mantener la seguridad de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79467b3baffd030cae1022f65bc0b8a97242c5e8bbe2f870753a3d3794b8705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818423"
---
# <a name="maintaining-wmi-security"></a>Mantener la seguridad de WMI

La seguridad de WMI se centra en proteger el acceso a los datos del espacio de nombres. WMI concede primero acceso a grupos de usuarios según lo especificado por la configuración de [*Control WMI*](gloss-w.md) y DCOM y, a continuación, los proveedores determinan si el usuario debe tener acceso a los datos del espacio de nombres.

En este tema se de abordan las siguientes secciones:

-   [Seguridad del espacio de nombres](#namespace-security)
-   [Seguridad del Modelo de objetos componentes distribuidos (DCOM) Configuración.](#distributed-component-object-model-dcom-security-settings)
-   [WMI, hosts de servicio compartido y autenticación](#wmi-shared-service-hosts-and-authentication)
-   [Seguridad para aplicaciones y scripts de cliente WMI](#security-for-wmi-client-scripts-and-applications)
-   [Temas relacionados](#related-topics)

## <a name="namespace-security"></a>Seguridad del espacio de nombres

La seguridad del espacio de nombres depende Windows identificadores de seguridad de usuario [*(SID)*](gloss-s.md) y del [*descriptor de seguridad*](gloss-s.md) para el espacio de nombres WMI.

Puede establecer la seguridad del espacio de nombres realizando las siguientes acciones:

-   Conceder o denegar derechos de acceso a espacios de nombres para los usuarios que usan el control WMI o cuando se crea el espacio de nombres. Para obtener más información, vea [Establecer la seguridad del espacio de](setting-namespace-security-with-the-wmi-control.md) nombres con el control WMI y Establecer la seguridad del espacio de nombres cuando se crea el espacio de [nombres](setting-namespace-security-when-the-namespace-is-created.md).
-   Use el control WMI ficha Seguridad para establecer la auditoría de seguridad. La auditoría de seguridad da como resultado entradas del registro de eventos cuando un usuario produce un error o realiza correctamente una acción auditada, como escribir datos en un objeto WMI o leer el descriptor de seguridad. Para obtener más información, vea [Acceso a espacios de nombres WMI.](access-to-wmi-namespaces.md)
-   Use el archivo MOF que define el espacio de nombres para requerir que un usuario realice una conexión cifrada. Para obtener más información, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Seguridad del Modelo de objetos componentes distribuidos (DCOM) Configuración.

La seguridad de DCOM requiere una configuración de autenticación y una configuración de suplantación. La autenticación significa que un proceso se identifica a sí mismo con otro. La suplantación identifica la autoridad a la que un cliente concede un servidor para llamar a procesos diferentes. Durante una comprobación de seguridad, el servidor suplanta al cliente. Para obtener más información, vea Proteger clientes y proveedores [de C++](securing-c---clients-and-providers.md) o [Proteger clientes de scripting.](securing-scripting-clients.md)

Los scripts y las aplicaciones de C/C++/C# establecen niveles de autenticación y suplantación cuando se conectan a un espacio de nombres WMI o usan la configuración predeterminada. Las conexiones a equipos remotos requieren una configuración diferente a la de los espacios de nombres WMI en el equipo local. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, hosts de servicio compartido y autenticación

WMI reside en un host de servicio compartido con otros servicios que se ejecutan en la cuenta NetworkService. En un proceso svchost, WMI comparte la misma autenticación que los demás procesos del host.

Los archivos DLL de proveedor se cargan en procesos de host de servicio independientes de WMI. La **propiedad HostingModel** de la clase del sistema [**\_ \_ Win32Provider**](--win32provider.md) que representa un proveedor especifica la cuenta del sistema con la que se ejecuta el proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegio especificado. Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Seguridad para aplicaciones y scripts de cliente WMI

Los scripts y las aplicaciones deben establecer la seguridad correcta para conectarse a espacios de nombres WMI en equipos locales y remotos. Para obtener más información, vea Proteger clientes y proveedores de [C++,](securing-c---clients-and-providers.md)Proteger clientes [de scripting](securing-scripting-clients.md)y Proteger [eventos WMI](securing-wmi-events.md).

En la tabla siguiente se enumeran los temas sobre el mantenimiento de la seguridad de WMI.



| Tema                                                                                              | Descripción                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Protección de espacios de nombres WMI](securing-wmi-namespaces.md)                                             | Puede limitar el acceso a los datos del espacio de nombres a los usuarios autorizados mediante el control WMI.                                                                                      |
| [Protección del proveedor](securing-your-provider.md)                                               | Información sobre cómo escribir proveedores seguros.                                                                                                                           |
| [Protección de clientes y proveedores de C++](securing-c---clients-and-providers.md)                       | Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.                                                         |
| [Protección de clientes de scripting](securing-scripting-clients.md)                                       | Los scripts Visual Basic aplicaciones (clientes de automatización) deben establecer la seguridad adecuada para obtener acceso a los datos y eventos wmi.                                        |
| [Protección de eventos WMI](securing-wmi-events.md)                                                     | El proveedor de eventos entrega los eventos WMI a un consumidor temporal o permanente. Los eventos se entregan en forma de una instancia de una clase de eventos.               |
| [Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md) | Con los permisos adecuados, puede llamar a métodos en los objetos WMI que representan objetos protegibles que leen o cambian descriptores de seguridad en objetos protegibles. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

 



