---
description: Un servidor con el privilegio SE TCB NAME, como un servicio Windows que se ejecuta en la cuenta LocalSystem, puede llamar a la función LogonUser para autenticar un cliente en el equipo en el que se ejecuta el \_ \_ servidor.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sesiones de inicio de sesión de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783027"
---
# <a name="client-logon-sessions"></a>Sesiones de inicio de sesión de cliente

Un servidor con el privilegio SE TCB NAME, como un servicio Windows que se ejecuta en la cuenta LocalSystem , puede llamar a la función LogonUser para autenticar un cliente en el equipo en el que se ejecuta el \_ \_ servidor. [](/windows/desktop/Services/localsystem-account) [](/windows/desktop/api/winbase/nf-winbase-logonusera) [](/windows/desktop/SecGloss/a-gly) La **función LogonUser** inicia una nueva sesión de [*inicio de sesión*](/windows/desktop/SecGloss/s-gly) y devuelve un token de acceso [*principal*](/windows/desktop/SecGloss/p-gly) que contiene la información de seguridad del cliente. Puede usar este token principal al llamar a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para suplantar al cliente o [](/windows/desktop/SecGloss/s-gly) llamar a la [**función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un proceso que se ejecute en el contexto de seguridad del cliente.

La ventaja de autenticar el cliente de esta manera es que el servidor que suplanta al cliente autenticado, o un proceso creado en el contexto del cliente autenticado, puede conectarse [*a*](/windows/desktop/SecGloss/p-gly) los recursos de red remotos como el cliente. Si no se realiza esta autenticación, el servidor solo puede conectarse a los recursos de red si ha adquirido el nombre de cuenta y la contraseña del cliente para pasar a la función [**WNetAddConnection2.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)

La desventaja de autenticar el cliente de esta manera es que el servidor debe haber adquirido las credenciales del cliente [*(nombre*](/windows/desktop/SecGloss/c-gly) de dominio, nombre de usuario y contraseña). Si un cliente remoto proporciona estas credenciales al servidor, es responsabilidad del cliente y del servidor asegurarse de que las credenciales se transmiten de forma segura.

 

 
