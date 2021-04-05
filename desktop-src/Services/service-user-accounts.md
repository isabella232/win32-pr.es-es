---
description: Cada servicio se ejecuta en el contexto de seguridad de una cuenta de usuario.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Cuentas de usuario de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912797"
---
# <a name="service-user-accounts"></a>Cuentas de usuario de servicio

Cada servicio se ejecuta en el contexto de seguridad de una cuenta de usuario. El nombre de usuario y la contraseña de una cuenta se especifican mediante la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) en el momento en que se instala el servicio. El nombre de usuario y la contraseña se pueden cambiar mediante la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Puede usar la función [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) para obtener el nombre de usuario (pero no la contraseña) asociado a un objeto de servicio. El administrador de control de servicios (SCM) carga automáticamente el perfil de usuario.

Al iniciar un servicio, el SCM inicia sesión en la cuenta asociada con el servicio. Si el inicio de sesión se realiza correctamente, el sistema genera un token de acceso y lo adjunta al nuevo proceso de servicio. Este token identifica el proceso de servicio en todas las interacciones posteriores con objetos protegibles (objetos que tienen un descriptor de seguridad asociado a ellos). Por ejemplo, si el servicio intenta abrir un identificador a una canalización, el sistema compara el token de acceso del servicio con el descriptor de seguridad de la canalización antes de conceder el acceso.

El SCM no mantiene las contraseñas de las cuentas de usuario de servicio. Si una contraseña ha expirado, se produce un error en el inicio de sesión y el servicio no se inicia. El administrador del sistema que asigna cuentas a los servicios puede crear cuentas con contraseñas que nunca expiran. Además, el administrador puede administrar las cuentas con contraseñas que caducan mediante el uso de un [programa de configuración de servicio](service-configuration-programs.md) para cambiar las contraseñas periódicamente.

Si un servicio necesita reconocer otro servicio antes de compartir su información, el segundo servicio puede utilizar la misma cuenta que el primer servicio, o bien puede ejecutarse en una cuenta que pertenezca a un alias reconocido por el primer servicio. Los servicios que deben ejecutarse de forma distribuida a través de la red deben ejecutarse en cuentas de todo el dominio.

Puede especificar una de las siguientes cuentas especiales en lugar de especificar una cuenta de usuario para el servicio:

-   [LocalService (Servicio local)](localservice-account.md)
-   [NetworkService (Servicio de red)](networkservice-account.md)
-   [LocalSystem (Sistema local)](localsystem-account.md)

 

 



