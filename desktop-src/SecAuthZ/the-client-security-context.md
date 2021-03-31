---
description: Al igual que todos los procesos, un servidor protegido tiene un token de acceso principal que describe su contexto de seguridad.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: Contexto de seguridad del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001277"
---
# <a name="the-client-security-context"></a>Contexto de seguridad del cliente

Al igual que todos los [*procesos*](/windows/desktop/SecGloss/p-gly), un servidor protegido tiene un [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) que describe su [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly). Cuando un cliente se conecta a un servidor protegido, el servidor puede querer realizar acciones con el contexto de seguridad del cliente en lugar del contexto de seguridad del servidor. Por ejemplo, cuando un cliente en una conversación de intercambio dinámico de datos (DDE) solicita información de un servidor DDE, el servidor debe comprobar que el cliente tiene permiso de acceso a la información.

Un servidor puede actuar en el contexto de seguridad del cliente de dos maneras:

-   Un subproceso del proceso de servidor puede suplantar al cliente. En este caso, el subproceso del servidor tiene un token de [*acceso*](/windows/desktop/SecGloss/a-gly) de suplantación que identifica al cliente, los grupos del cliente y los [*privilegios*](/windows/desktop/SecGloss/p-gly)del cliente. Para obtener más información, vea [suplantación de cliente](client-impersonation.md).
-   El servidor puede obtener las [*credenciales*](/windows/desktop/SecGloss/c-gly) del cliente y registrar el cliente en el equipo del servidor. Esto crea una nueva [*sesión*](/windows/desktop/SecGloss/s-gly) de inicio de sesión y genera un token de acceso principal para el cliente. A continuación, el servidor puede usar el token de acceso del cliente para suplantar al cliente o iniciar un nuevo proceso que se ejecute en el contexto de seguridad del cliente. Para obtener más información, vea [sesiones de inicio de sesión de cliente](client-logon-sessions.md).

En la mayoría de los casos, la suplantación del cliente es suficiente. La suplantación permite al servidor comprobar el acceso del cliente a los objetos protegibles, comprobar los privilegios del cliente y generar entradas de traza de auditoría que identifiquen al cliente. Normalmente, un servidor debe iniciar una sesión de inicio de sesión de cliente solo si necesita utilizar el contexto de seguridad del cliente para tener acceso a los recursos de red.

 

 
