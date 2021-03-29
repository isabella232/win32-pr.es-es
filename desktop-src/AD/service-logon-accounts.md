---
title: Cuentas de inicio de sesión de servicio
description: Un servicio, como cualquier proceso, tiene una identidad de seguridad principal que determina los derechos de acceso concedidos y los privilegios para los recursos locales y de red.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, Inicio de sesión de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903093"
---
# <a name="service-logon-accounts"></a>Cuentas de inicio de sesión de servicio

Un servicio, como cualquier proceso, tiene una identidad de seguridad principal que determina los derechos de acceso concedidos y los privilegios para los recursos locales y de red. Esta identidad de seguridad, o el contexto de seguridad, también determina el potencial que tiene el servicio para daños en los recursos locales y de red.

El contexto de seguridad de un servicio de Microsoft Win32 viene determinado por la cuenta de inicio de sesión que se usa para iniciar el servicio. En esta sección se describen los problemas de programación y los procedimientos recomendados relacionados con la cuenta de inicio de sesión de servicio utilizada por los servicios de Win32, centrándose en los servicios habilitados para el uso de directorios. Esta sección contiene los siguientes temas:

-   [Acerca de las cuentas de inicio de sesión de servicio](about-service-logon-accounts.md): información general sobre las cuentas de inicio de sesión de servicio y los problemas de programación de contexto de seguridad para un servicio Win32
-   [Directrices para seleccionar una cuenta de inicio de sesión de servicio](guidelines-for-selecting-a-service-logon-account.md) para un servicio Win32.
-   [Configuración de la cuenta de usuario de un servicio](setting-up-a-serviceampaposs-user-account.md).
-   [Instalación de un servicio en un equipo host](installing-a-service-on-a-host-computer.md) y especificación de la cuenta de inicio de sesión del servicio.
-   [Conceder el derecho de inicio de sesión como servicio en el equipo host](granting-logon-as-service-right-on-the-host-computer.md): conceda a la cuenta de usuario del servicio el inicio de sesión como servicio en el equipo host.
-   [Probar si se está ejecutando en un controlador de dominio](testing-whether-running-on-a-domain-controller.md): detectando en el momento de la instalación si la instancia de servicio se está instalando en un controlador de dominio.
-   [Conceder derechos de acceso a la cuenta de inicio de sesión del servicio](granting-access-rights-to-the-service-logon-account.md): establecimiento y mantenimiento de las ACE y pertenencias a grupos para asegurarse de que el sistema concederá acceso al servicio en ejecución a los recursos locales y de red necesarios.
-   [Cambiar la contraseña de la cuenta de usuario de un servicio](changing-the-password-on-a-serviceampaposs-user-account.md): cambiar la contraseña en la cuenta de usuario del servicio y, al mismo tiempo, actualizar la contraseña registrada con el administrador de control de servicios en cada servidor host en el que está instalado el servicio.
-   [Autenticación mutua mediante Kerberos](mutual-authentication-using-kerberos.md): mantenimiento del registro del nombre de entidad de seguridad de servicio (SPN) en el objeto de directorio asociado a la cuenta de inicio de sesión de cada instancia de su servicio. Los SPN permiten a los clientes autenticar un servicio mediante la autenticación mutua de Kerberos.
-   [Convertir los formatos de nombre de cuenta de dominio](converting-domain-account-name-formats.md)(por ejemplo, convertir un nombre distintivo en el formato de nombre de ****\\*** usuario de dominio* ) y viceversa.

 

 




