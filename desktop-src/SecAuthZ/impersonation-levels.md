---
description: La \_ enumeración nivel de SUplantación de seguridad \_ define cuatro niveles de suplantación que determinan las operaciones que puede realizar un servidor en el contexto de los clientes.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Niveles de suplantación (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91654f42a86e5c47069197bed084df56f5445dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668401"
---
# <a name="impersonation-levels-authorization"></a>Niveles de suplantación (autorización)

La enumeración [**\_ \_ nivel de suplantación de seguridad**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) define cuatro niveles de suplantación que determinan las operaciones que un servidor puede realizar en el contexto del cliente.



| Nivel de suplantación    | Descripción                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | El servidor no puede suplantar o identificar al cliente.                                            |
| SecurityIdentification | El servidor puede obtener la identidad y los privilegios del cliente, pero no puede suplantar al cliente. |
| SecurityImpersonation  | El servidor puede suplantar el contexto de seguridad del cliente en el sistema local.                    |
| SecurityDelegation     | El servidor puede suplantar el contexto de seguridad del cliente en sistemas remotos.                      |



 

El cliente de una canalización con nombre, RPC o conexión DDE puede controlar el nivel de suplantación. Por ejemplo, un cliente de canalización con nombre puede llamar a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador a una canalización con nombre y especificar el nivel de suplantación del servidor.

Cuando la canalización con nombre, RPC o conexión DDE es remota, se omiten las marcas pasadas a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para establecer el nivel de suplantación. En este caso, el nivel de suplantación del cliente viene determinado por los niveles de suplantación habilitados por el servidor, que se establece mediante una marca en la cuenta del servidor en el servicio de directorio. Por ejemplo, si el servidor está habilitado para la delegación, el nivel de suplantación del cliente también se establecerá en delegación aunque las marcas pasadas a **CreateFile** especifiquen el nivel de suplantación de identificación.

Los clientes DDE usan la función [**DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) con la estructura [**\_ \_ de calidad de \_ servicio de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) para especificar el nivel de suplantación. El nivel SecurityImpersonation es el valor predeterminado para los servidores de canalización con nombre, RPC y DDE. Las funciones [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)y [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) permiten al llamador especificar un nivel de suplantación. Use la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) para recuperar el nivel de suplantación de un [*token de acceso*](/windows/desktop/SecGloss/a-gly).

En el nivel SecurityImpersonation, la mayoría de las acciones del subproceso se producen en el contexto de seguridad del [*token de suplantación*](/windows/desktop/SecGloss/i-gly) del subproceso, en lugar de en el [*token principal*](/windows/desktop/SecGloss/p-gly) del [*proceso*](/windows/desktop/SecGloss/p-gly) que posee el subproceso. Por ejemplo, si un subproceso de suplantación abre un [objeto protegible](securable-objects.md), el sistema utiliza el token de suplantación para comprobar el acceso del subproceso. Del mismo modo, si un subproceso de suplantación crea un nuevo objeto, por ejemplo llamando a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , el propietario del nuevo objeto es el propietario predeterminado del [*token de acceso*](/windows/desktop/SecGloss/a-gly)del cliente.

Sin embargo, el sistema utiliza el token principal del proceso en lugar del token de suplantación del subproceso que realiza la llamada en las siguientes situaciones:

-   Si un subproceso de suplantación llama a la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , el nuevo proceso hereda siempre el token principal del proceso.
-   En el caso de las funciones que requieren el \_ privilegio de nombre TCB de se \_ , como la función [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) , el sistema siempre comprueba el privilegio en el token principal del proceso.
-   En el caso de las funciones que requieren el privilegio de nombre de auditoría de SE \_ \_ , como la función [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) , el sistema siempre comprueba el privilegio en el token principal del proceso.
-   En una llamada a la función [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , un subproceso puede especificar si la función utiliza el token de suplantación o el token primario para determinar si se debe conceder el acceso solicitado.

 

 
