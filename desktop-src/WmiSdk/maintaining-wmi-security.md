---
description: La seguridad de WMI se centra en proteger el acceso a los datos del espacio de nombres. En primer lugar, WMI concede acceso a grupos de usuarios según lo especificado por el control WMI y la configuración de DCOM y, a continuación, los proveedores determinan si el usuario debe tener acceso a los datos del espacio de nombres.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Mantenimiento de la seguridad de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697418"
---
# <a name="maintaining-wmi-security"></a>Mantenimiento de la seguridad de WMI

La seguridad de WMI se centra en proteger el acceso a los datos del espacio de nombres. En primer lugar, WMI concede acceso a grupos de usuarios según lo especificado por el [*control WMI*](gloss-w.md) y la configuración de DCOM y, a continuación, los proveedores determinan si el usuario debe tener acceso a los datos del espacio de nombres.

En este tema se describen las siguientes secciones:

-   [Seguridad del espacio de nombres](#namespace-security)
-   [Configuración de seguridad del modelo de objetos componentes distribuido (DCOM).](#distributed-component-object-model-dcom-security-settings)
-   [WMI, hosts de servicio compartido y autenticación](#wmi-shared-service-hosts-and-authentication)
-   [Seguridad de las aplicaciones y scripts de cliente WMI](#security-for-wmi-client-scripts-and-applications)
-   [Temas relacionados](#related-topics)

## <a name="namespace-security"></a>Seguridad del espacio de nombres

La seguridad del espacio de nombres depende de los [*identificadores de seguridad de usuario (SID)*](gloss-s.md) de Windows estándar y el [*descriptor de seguridad*](gloss-s.md) para el espacio de nombres WMI.

Para establecer la seguridad de los espacios de nombres, realice las siguientes acciones:

-   Conceda o deniegue derechos de acceso a los espacios de nombres de los usuarios mediante el control WMI o cuando se cree el espacio de nombres. Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md) y [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).
-   Use la pestaña seguridad del control WMI para establecer la auditoría de seguridad. La auditoría de seguridad produce entradas en el registro de eventos cuando un usuario produce un error o se ejecuta correctamente en una acción auditada, como la escritura de datos en un objeto WMI o la lectura del descriptor de seguridad. Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).
-   Use el archivo MOF que define el espacio de nombres para requerir que un usuario realice una conexión cifrada. Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Configuración de seguridad del modelo de objetos componentes distribuido (DCOM).

La seguridad de DCOM requiere una configuración de autenticación y una configuración de suplantación. La autenticación significa que un proceso se identifica a sí mismo en otro. La suplantación identifica la autoridad que un cliente concede a un servidor para que llame a distintos procesos. Durante una comprobación de seguridad, el servidor suplanta al cliente. Para obtener más información, vea [proteger clientes y proveedores de C++](securing-c---clients-and-providers.md) o [proteger los clientes de scripting](securing-scripting-clients.md).

Los scripts y las aplicaciones de C/C++/C # establecen un nivel de autenticación y suplantación cuando se conectan a un espacio de nombres WMI o utilizan la configuración predeterminada. Las conexiones a equipos remotos requieren una configuración diferente de la de los espacios de nombres de WMI en el equipo local. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, hosts de servicio compartido y autenticación

WMI reside en un host de servicio compartido con otros servicios que se ejecutan con la cuenta NetworkService. En un proceso svchost, WMI comparte la misma autenticación que los demás procesos del host.

Los archivos dll de proveedor se cargan en procesos de host de servicio independientes desde WMI. La propiedad **HostingModel** de la clase del sistema [**\_ \_ Win32Provider**](--win32provider.md) que representa un proveedor especifica la cuenta del sistema en la que se ejecuta el proveedor. Al establecer esta propiedad, el proveedor se carga en un proceso de host compartido que tiene un nivel de privilegios especificado. Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Seguridad de las aplicaciones y scripts de cliente WMI

Los scripts y las aplicaciones deben establecer la seguridad correcta para conectarse a los espacios de nombres WMI en equipos locales y remotos. Para obtener más información, consulte [protección de clientes y proveedores de C++](securing-c---clients-and-providers.md), protección de [los clientes de scripting](securing-scripting-clients.md)y [protección de eventos de WMI](securing-wmi-events.md).

En la tabla siguiente se enumeran los temas sobre el mantenimiento de la seguridad de WMI.



| Tema                                                                                              | Descripción                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)                                             | Puede limitar el acceso a los datos del espacio de nombres a los usuarios autorizados a través del control WMI.                                                                                      |
| [Protección del proveedor](securing-your-provider.md)                                               | Información sobre cómo escribir proveedores seguros.                                                                                                                           |
| [Protección de clientes y proveedores de C++](securing-c---clients-and-providers.md)                       | Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.                                                         |
| [Protección de los clientes de scripting](securing-scripting-clients.md)                                       | Los scripts y las aplicaciones de Visual Basic (clientes de automatización) deben establecer la seguridad adecuada para obtener acceso a los eventos y datos de WMI.                                        |
| [Proteger eventos WMI](securing-wmi-events.md)                                                     | El proveedor de eventos entrega los eventos WMI a un consumidor temporal o permanente. Los eventos se entregan en forma de una instancia de una clase de eventos.               |
| [Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md) | Con los permisos adecuados, puede llamar a métodos en los objetos WMI que representan objetos protegibles que leen o modifican los descriptores de seguridad de los objetos protegibles. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

 



