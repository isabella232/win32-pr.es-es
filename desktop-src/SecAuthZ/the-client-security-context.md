---
description: Al igual que todos los procesos, un servidor protegido tiene un token de acceso principal que describe su contexto de seguridad.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Contexto de seguridad de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af57c11c7b0452003498b88b0be24c880e2875fec459fb80e3cd87ef01bdd493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907125"
---
# <a name="the-client-security-context"></a>Contexto de seguridad de cliente

Al igual [*que todos los*](/windows/desktop/SecGloss/p-gly)procesos, un servidor protegido tiene un token de acceso [*principal*](/windows/desktop/SecGloss/p-gly) que describe su contexto [*de seguridad.*](/windows/desktop/SecGloss/s-gly) Cuando un cliente se conecta a un servidor protegido, es posible que desee realizar acciones mediante el contexto de seguridad del cliente en lugar del contexto de seguridad del servidor. Por ejemplo, cuando un cliente de una conversación de intercambio dinámico de datos (DDE) solicita información de un servidor DDE, el servidor debe comprobar que el cliente tiene permiso de acceso a la información.

Hay dos maneras de que un servidor pueda actuar en el contexto de seguridad del cliente:

-   Un subproceso del proceso de servidor puede suplantar al cliente. En este caso, el subproceso del servidor tiene un token de acceso de [*suplantación*](/windows/desktop/SecGloss/a-gly) que identifica el cliente, los grupos del cliente y los [*privilegios del cliente.*](/windows/desktop/SecGloss/p-gly) Para obtener más información, vea [Suplantación de cliente.](client-impersonation.md)
-   El servidor puede obtener las credenciales del [*cliente*](/windows/desktop/SecGloss/c-gly) e iniciar sesión en el cliente en el equipo del servidor. Esto crea una nueva sesión de [*inicio de sesión*](/windows/desktop/SecGloss/s-gly) y genera un token de acceso principal para el cliente. A continuación, el servidor puede usar el token de acceso del cliente para suplantar al cliente o para iniciar un nuevo proceso que se ejecuta en el contexto de seguridad del cliente. Para obtener más información, vea [Sesiones de inicio de sesión de cliente.](client-logon-sessions.md)

En la mayoría de los casos, suplantar al cliente es suficiente. La suplantación permite al servidor comprobar el acceso del cliente a objetos protegibles, comprobar los privilegios del cliente y generar entradas de registro de auditoría que identifiquen al cliente. Normalmente, un servidor debe iniciar una sesión de inicio de sesión de cliente solo si necesita usar el contexto de seguridad del cliente para acceder a los recursos de red.

 

 
