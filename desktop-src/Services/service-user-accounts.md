---
description: Cada servicio se ejecuta en el contexto de seguridad de una cuenta de usuario.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Cuentas de usuario de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6053a4f870b2a49923d802f7cb5f2a45b786d63314d1010773c3e8f58627bec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888552"
---
# <a name="service-user-accounts"></a>Cuentas de usuario de servicio

Cada servicio se ejecuta en el contexto de seguridad de una cuenta de usuario. La función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) especifica el nombre de usuario y la contraseña de una cuenta en el momento en que se instala el servicio. El nombre de usuario y la contraseña se pueden cambiar mediante la [**función ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Puede usar la función [**QueryServiceConfig para**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) obtener el nombre de usuario (pero no la contraseña) asociado a un objeto de servicio. El administrador de control de servicios (SCM) carga automáticamente el perfil de usuario.

Al iniciar un servicio, el SCM inicia sesión en la cuenta asociada al servicio. Si el inicio de sesión se realiza correctamente, el sistema genera un token de acceso y lo asocia al nuevo proceso de servicio. Este token identifica el proceso de servicio en todas las interacciones posteriores con objetos protegibles (objetos que tienen un descriptor de seguridad asociado a ellos). Por ejemplo, si el servicio intenta abrir un identificador en una canalización, el sistema compara el token de acceso del servicio con el descriptor de seguridad de la canalización antes de conceder acceso.

El SCM no mantiene las contraseñas de las cuentas de usuario de servicio. Si una contraseña ha expirado, se produce un error en el inicio de sesión y el servicio no se inicia. El administrador del sistema que asigna cuentas a servicios puede crear cuentas con contraseñas que nunca expiren. El administrador también puede administrar cuentas con contraseñas que expiren mediante un programa [de configuración de servicio](service-configuration-programs.md) para cambiar periódicamente las contraseñas.

Si un servicio necesita reconocer otro servicio antes de compartir su información, el segundo servicio puede usar la misma cuenta que el primer servicio o puede ejecutarse en una cuenta que pertenezca a un alias reconocido por el primer servicio. Los servicios que deben ejecutarse de forma distribuida a través de la red deben ejecutarse en cuentas de todo el dominio.

Puede especificar una de las siguientes cuentas especiales en lugar de especificar una cuenta de usuario para el servicio:

-   [LocalService (Servicio local)](localservice-account.md)
-   [NetworkService (Servicio de red)](networkservice-account.md)
-   [LocalSystem (Sistema local)](localsystem-account.md)

 

 



