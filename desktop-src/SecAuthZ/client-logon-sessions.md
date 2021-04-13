---
description: Un servidor con el \_ privilegio de nombre TCB de se, como \_ un servicio de Windows que se ejecuta en la cuenta LocalSystem, puede llamar a la función LogonUser para autenticar un cliente en el equipo en el que se está ejecutando el servidor.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sesiones de inicio de sesión de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1439b27637b0e46df3b468b42cb9c45ac8f759f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543547"
---
# <a name="client-logon-sessions"></a>Sesiones de inicio de sesión de cliente

Un servidor con el \_ privilegio de nombre TCB de se, como \_ un servicio de Windows que se ejecuta en la [cuenta LocalSystem](/windows/desktop/Services/localsystem-account), puede llamar a la función [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) para [*autenticar*](/windows/desktop/SecGloss/a-gly) un cliente en el equipo en el que se está ejecutando el servidor. La función **LogonUser** inicia una nueva [*sesión*](/windows/desktop/SecGloss/s-gly) de inicio de sesión y devuelve un [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) que contiene la información de seguridad del cliente. Puede usar este token primario para llamar a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para suplantar al cliente o al llamar a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un proceso que se ejecute en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) del cliente.

La ventaja de autenticar al cliente de esta manera es que el servidor que suplanta al cliente autenticado, o un [*proceso*](/windows/desktop/SecGloss/p-gly) creado en el contexto del cliente autenticado, puede conectarse a los recursos de la red remota como el cliente. Si no se realiza esta autenticación, el servidor puede conectarse a los recursos de red solo si ha adquirido el nombre de cuenta y la contraseña del cliente para pasarlos a la función [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .

El inconveniente de la autenticación del cliente de esta manera es que el servidor debe haber adquirido las [*credenciales*](/windows/desktop/SecGloss/c-gly) del cliente (nombre de dominio, nombre de usuario y contraseña). Si un cliente remoto proporciona estas credenciales al servidor, es responsabilidad del cliente y del servidor asegurarse de que las credenciales se transmiten de forma segura.

 

 
