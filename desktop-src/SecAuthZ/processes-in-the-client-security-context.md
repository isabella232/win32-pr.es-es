---
description: Una aplicación de servidor puede llamar a la función CreateProcessAsUser para crear un nuevo proceso que se ejecute en un contexto de seguridad de clientes.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Procesos en el contexto de seguridad de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3537f2f9dfa9129a84d0811d2e8c45ff91f5a987af0131d1f65ceedda6103d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907585"
---
# <a name="processes-in-the-client-security-context"></a>Procesos en el contexto de seguridad de cliente

Una aplicación de servidor puede llamar a [**la función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un nuevo proceso que se ejecute en el contexto de seguridad [*de un cliente.*](/windows/desktop/SecGloss/s-gly) Cuando se llama con [*el token*](/windows/desktop/SecGloss/a-gly)de acceso de un cliente, **CreateProcessAsUser** requiere los privilegios SE ASSIGNPRIMARYTOKEN NAME y SE INCREASE QUOTA NAME, que mantienen los servicios de Windows que se ejecutan en la cuenta \_ \_ \_ \_ \_ [LocalSystem](/windows/desktop/Services/localsystem-account).

La [**función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) también requiere un [*token de acceso principal.*](/windows/desktop/SecGloss/p-gly) Un servidor puede obtener un token de [](client-logon-sessions.md) acceso principal para un [](client-impersonation.md) cliente iniciando una sesión de inicio de sesión para el cliente o suplantando el cliente y duplicando el [*token de suplantación*](/windows/desktop/SecGloss/i-gly).

Los procedimientos siguientes describen dos maneras de crear un proceso de cliente.

**Para crear un proceso de cliente iniciando sesión en el cliente**

1.  Inicie sesión en el cliente en el equipo local con las credenciales del cliente [*en*](/windows/desktop/SecGloss/c-gly) una llamada a [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** genera un token principal para la sesión de inicio de [*sesión del cliente.*](/windows/desktop/SecGloss/l-gly)
2.  Si el servidor necesita usar el contexto de seguridad del cliente, [](/windows/desktop/SecGloss/p-gly) obtenga acceso al archivo ejecutable para el proceso de cliente mediante el token principal en una llamada a la [**función ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
3.  Cree un proceso en el contexto de seguridad del cliente mediante el token principal en una llamada a [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Es posible que un proceso creado mediante la técnica siguiente no pueda acceder a los recursos de red a menos que tenga las credenciales del [*cliente*](/windows/desktop/SecGloss/c-gly).

 

**Para crear un proceso de cliente suplantando al cliente**

1.  Inicie la suplantación mediante una función de suplantación, como [**ImpersonateNamedPipeClient.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)
2.  Llame a [**la función OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obtener un token de suplantación que tenga el contexto de seguridad del cliente.
3.  Llame a [**la función DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token de suplantación en un token principal.
4.  Use el token principal en una llamada a la [**función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para crear un proceso en el contexto de seguridad del cliente.

De forma predeterminada, [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) crea el proceso [*de cliente*](/windows/desktop/SecGloss/p-gly) en una estación de ventana y un escritorio no inactivos. Para crear un proceso interactivo, el servidor debe establecer primero las listas de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) de la estación de ventana interactiva y el escritorio para asegurarse de que el cliente tiene permiso de acceso a ellas. La manera preferida de hacerlo es iniciar sesión en el cliente, obtener el identificador de seguridad [(SID)](/previous-versions//aa446670(v=vs.85))de la sesión de inicio de sesión del cliente y, a continuación, usar ese SID en las ACE con acceso permitido tanto en la estación de ventana interactiva como en el escritorio. A continuación, el servidor puede llamar **a CreateProcessAsUser**, especificando la estación de ventana interactiva y el escritorio winsta0 \\ predeterminado. Para obtener un ejemplo que muestra este procedimiento, vea [Iniciar un proceso de cliente interactivo en C++.](/previous-versions//aa379608(v=vs.85))

 

 
