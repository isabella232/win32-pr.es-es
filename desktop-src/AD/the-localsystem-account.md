---
title: Usar la cuenta LocalSystem como cuenta de inicio de sesión de servicio
description: Una ventaja de la ejecución en la cuenta LocalSystem es que el servicio tiene acceso completo sin restricciones a los recursos locales.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- cuenta localsystem
- Localsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ac31cb7b3e0ad335f9a2781187aadcb03a1529055eb0771856aa01543add0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024583"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Usar la cuenta LocalSystem como cuenta de inicio de sesión de servicio

Una ventaja de la ejecución en la cuenta LocalSystem es que el servicio tiene acceso completo sin restricciones a los recursos locales. Esto también es la desventaja de LocalSystem porque un servicio LocalSystem puede hacer cosas que harían que todo el sistema se desfasase. En concreto, un servicio que se ejecuta como LocalSystem en un controlador de dominio (DC) tiene acceso sin restricciones a Active Directory Domain Services. Esto significa que los errores del servicio, o los ataques de seguridad en el servicio, pueden dañar el sistema o, si el servicio está en un controlador de dominio, dañar toda la red empresarial.

Por estos motivos, los administradores de dominio en instalaciones confidenciales tendrán cuidado al permitir que los servicios se ejecuten como LocalSystem. De hecho, pueden tener directivas en él, especialmente en los equipos de dominio. Si el servicio debe ejecutarse como LocalSystem, la documentación del servicio debe justificar a los administradores de dominio los motivos para conceder al servicio el derecho a ejecutarse con privilegios elevados. Los servicios nunca deben ejecutarse como LocalSystem en un controlador de dominio. Para obtener más información y un ejemplo de código que muestra cómo un instalador de servicio o servicio puede determinar si se ejecuta en un controlador de dominio, vea Probar si se ejecuta en [un controlador de dominio.](testing-whether-running-on-a-domain-controller.md)

Cuando un servicio se ejecuta con la cuenta LocalSystem en un equipo que es miembro de dominio, el servicio tiene cualquier acceso de red que se conceda a la cuenta de equipo o a cualquier grupo del que sea miembro la cuenta de equipo. Tenga en cuenta que, Windows 2000, una cuenta de equipo de dominio es una entidad de servicio, similar a una cuenta de usuario. Esto significa que una cuenta de equipo puede estar en un grupo de seguridad y una ACE en un descriptor de seguridad puede conceder acceso a una cuenta de equipo. Tenga en cuenta que no se recomienda agregar cuentas de equipo a grupos por dos motivos:

-   Las cuentas de equipo están sujetas a eliminación y nueva creación si el equipo abandona y, a continuación, vuelve a unirse al dominio.
-   Si agrega una cuenta de equipo a un grupo, todos los servicios que se ejecutan como LocalSystem en ese equipo tienen permitidos los derechos de acceso del grupo. Esto se debe a que todos los servicios LocalSystem comparten la cuenta de equipo de su servidor host. Por este motivo, es especialmente importante que las cuentas de equipo no sean miembros de ningún grupo de administradores de dominio.

Las cuentas de equipo suelen tener pocos privilegios y no pertenecen a grupos. La protección de ACL predeterminada en Active Directory Domain Services permite un acceso mínimo para las cuentas de equipo. Por lo tanto, los servicios que se ejecutan como LocalSystem, en equipos que no son DCs, solo tienen acceso mínimo a Active Directory Domain Services.

Si el servicio se ejecuta en LocalSystem, debe probar el servicio en un servidor miembro para asegurarse de que el servicio tiene derechos suficientes para leer y escribir en Dominio de Active Directory Controllers. Un controlador de dominio no debe ser el único Windows en el que pruebe el servicio. Tenga en cuenta que un servicio que se ejecuta en LocalSystem en un controlador de dominio de Windows tiene acceso completo a Active Directory Domain Services y que un servidor miembro se ejecuta en el contexto de la cuenta de equipo que tiene considerablemente menos derechos.

 

 




