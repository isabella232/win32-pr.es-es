---
title: Uso de la cuenta LocalSystem como cuenta de inicio de sesión de servicio
description: Una ventaja de ejecutar con la cuenta LocalSystem es que el servicio tiene un acceso sin restricciones completo a los recursos locales.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- cuenta LocalSystem
- LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993887"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Uso de la cuenta LocalSystem como cuenta de inicio de sesión de servicio

Una ventaja de ejecutar con la cuenta LocalSystem es que el servicio tiene un acceso sin restricciones completo a los recursos locales. Esta también es la desventaja de LocalSystem porque un servicio LocalSystem puede hacer cosas que desactivarían todo el sistema. En concreto, un servicio que se ejecuta como LocalSystem en un controlador de dominio (DC) tiene acceso sin restricciones a Active Directory Domain Services. Esto significa que los errores en el servicio o los ataques de seguridad en el servicio pueden dañar el sistema o, si el servicio está en un controlador de dominio, dañar toda la red de la empresa.

Por estos motivos, los administradores de dominio en instalaciones confidenciales serán cautos para permitir que los servicios se ejecuten como LocalSystem. De hecho, pueden tener directivas en él, especialmente en los controladores de sesión. Si el servicio debe ejecutarse como LocalSystem, la documentación del servicio debe justificar a los administradores de dominio los motivos por los que se concede el derecho de ejecución al servicio con privilegios elevados. Los servicios nunca deben ejecutarse como LocalSystem en un controlador de dominio. Para obtener más información y un ejemplo de código que muestre cómo un servicio o instalador de servicio puede determinar si se está ejecutando en un controlador de dominio, consulte [comprobar si se está ejecutando en un controlador de dominio](testing-whether-running-on-a-domain-controller.md).

Cuando un servicio se ejecuta con la cuenta LocalSystem en un equipo que es miembro del dominio, el servicio tiene el acceso a la red que se concede a la cuenta de equipo o a los grupos de los que es miembro la cuenta de equipo. Tenga en cuenta que en Windows 2000, una cuenta de equipo de dominio es una entidad de servicio, similar a una cuenta de usuario. Esto significa que una cuenta de equipo puede estar en un grupo de seguridad y una ACE en un descriptor de seguridad puede conceder acceso a una cuenta de equipo. Tenga en cuenta que no se recomienda agregar cuentas de equipo a grupos por dos motivos:

-   Las cuentas de equipo están sujetas a eliminación y recreación si el equipo sale del dominio y, a continuación, se vuelve a unir.
-   Si agrega una cuenta de equipo a un grupo, todos los servicios que se ejecutan como LocalSystem en ese equipo tienen permitidos los derechos de acceso del grupo. Esto se debe a que todos los servicios LocalSystem comparten la cuenta de equipo de su servidor host. Por esta razón, es especialmente importante que las cuentas de equipo no sean miembros de ningún grupo de administradores de dominio.

Normalmente, las cuentas de equipo tienen pocos privilegios y no pertenecen a los grupos. La protección de ACL predeterminada en Active Directory Domain Services permite un acceso mínimo para las cuentas de equipo. Por lo tanto, los servicios que se ejecutan como LocalSystem, en equipos que no sean controladores de sesión, solo tienen acceso mínimo a Active Directory Domain Services.

Si el servicio se ejecuta bajo LocalSystem, debe probar el servicio en un servidor miembro para asegurarse de que el servicio tiene derechos suficientes para leer y escribir en los controladores de Dominio de Active Directory. Un controlador de dominio no debe ser el único equipo de Windows en el que se prueba el servicio. Tenga en cuenta que un servicio que se ejecuta bajo LocalSystem en un controlador de dominio de Windows tiene acceso completo a Active Directory Domain Services y que un servidor miembro se ejecuta en el contexto de la cuenta de equipo que tiene muchos menos derechos.

 

 




