---
description: Una aplicación de servidor puede llamar a la función CreateProcessAsUser para crear un nuevo proceso que se ejecute en un contexto de seguridad de clientes.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Procesos en el contexto de seguridad del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652453"
---
# <a name="processes-in-the-client-security-context"></a>Procesos en el contexto de seguridad del cliente

Una aplicación de servidor puede llamar a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un nuevo proceso que se ejecute en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly)de un cliente. Cuando se llama con el [*token de acceso*](/windows/desktop/SecGloss/a-gly)de un cliente, **CreateProcessAsUser** requiere los privilegios de nombre de ASSIGNPRIMARYTOKEN y de nombre de cuota de aumento de se \_ \_ \_ \_ \_ , que están contenidos en los servicios de Windows que se ejecutan en la [cuenta LocalSystem](/windows/desktop/Services/localsystem-account).

La función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) también requiere un [*token de acceso principal*](/windows/desktop/SecGloss/p-gly). Un servidor puede obtener un token de acceso principal para un cliente, ya sea [iniciando una sesión de inicio](client-logon-sessions.md) de sesión para el cliente o [suplantando el cliente](client-impersonation.md) y duplicando el [*token de suplantación*](/windows/desktop/SecGloss/i-gly).

En los procedimientos siguientes se describen dos maneras de crear un proceso de cliente.

**Para crear un proceso de cliente mediante el inicio de sesión en el cliente**

1.  Inicie la sesión del cliente en el equipo local con las [*credenciales*](/windows/desktop/SecGloss/c-gly) del cliente en una llamada a [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** genera un token primario para la sesión de [*Inicio*](/windows/desktop/SecGloss/l-gly)de sesión del cliente.
2.  Si el servidor necesita usar el contexto de seguridad del cliente, obtenga acceso al archivo ejecutable para el [*proceso*](/windows/desktop/SecGloss/p-gly) de cliente mediante el token principal en una llamada a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
3.  Cree un proceso en el contexto de seguridad del cliente mediante el token principal en una llamada a [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Es posible que un proceso creado mediante la siguiente técnica no pueda tener acceso a los recursos de red a menos que tenga las [*credenciales*](/windows/desktop/SecGloss/c-gly)del cliente.

 

**Para crear un proceso de cliente mediante la suplantación del cliente**

1.  Inicie la suplantación mediante una función de suplantación, como [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient).
2.  Llame a la función [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener un token de suplantación que tenga el contexto de seguridad del cliente.
3.  Llame a la función [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token de suplantación en un token primario.
4.  Utilice el token principal en una llamada a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un proceso en el contexto de seguridad del cliente.

De forma predeterminada, [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) crea el [*proceso*](/windows/desktop/SecGloss/p-gly) de cliente en una estación de ventana y escritorio no interactivos. Para crear un proceso interactivo, el servidor debe establecer primero las [*listas de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de la estación de ventana y el escritorio interactivos para asegurarse de que se permite el acceso al cliente. La mejor manera de hacerlo es registrar el cliente en, [obtener el identificador de seguridad (SID) de la sesión de inicio de sesión del cliente](/previous-versions//aa446670(v=vs.85))y, a continuación, usar ese SID en ACE con acceso permitido en la estación de ventana y el escritorio interactivos. Después, el servidor puede llamar a **CreateProcessAsUser**, especificando la estación de ventana interactiva y el winsta0 de escritorio \\ predeterminados. Para obtener un ejemplo que muestra este procedimiento, vea [iniciar un proceso de cliente interactivo en C++](/previous-versions//aa379608(v=vs.85)).

 

 
