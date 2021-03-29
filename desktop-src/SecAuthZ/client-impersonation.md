---
description: La suplantación es la capacidad de un subproceso de ejecutarse utilizando información de seguridad diferente que el proceso que posee el subproceso.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Suplantación de cliente (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e72abb17c9f5f6271f55fbfc77da4f6b93ca2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001384"
---
# <a name="client-impersonation-authorization"></a>Suplantación de cliente (autorización)

La [*suplantación*](/windows/desktop/SecGloss/i-gly) es la capacidad de un subproceso de ejecutarse utilizando información de seguridad diferente que el proceso que posee el subproceso. Normalmente, un subproceso de una aplicación de servidor suplanta a un cliente. Esto permite que el subproceso de servidor actúe en nombre de ese cliente para obtener acceso a los objetos del servidor o validar el acceso a los objetos propios del cliente.

La API de Microsoft Windows proporciona las siguientes funciones para iniciar una suplantación:

-   Una aplicación de servidor DDE puede llamar a la función [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) para suplantar a un cliente.
-   Un servidor de canalización con nombre puede llamar a la función [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) .
-   Puede llamar a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para suplantar el contexto de seguridad del [*token de acceso*](/windows/desktop/SecGloss/a-gly)de un usuario que ha iniciado sesión.
-   La función [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) permite que un subproceso genere una copia de su propio token de acceso. Esto resulta útil cuando una aplicación necesita cambiar el contexto de seguridad de un único subproceso. Por ejemplo, a veces solo un subproceso de un proceso necesita habilitar un [*privilegio*](/windows/desktop/SecGloss/p-gly).
-   Puede llamar a la función [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) para que el subproceso de destino se ejecute en el contexto de seguridad de un [*token de suplantación*](/windows/desktop/SecGloss/i-gly)especificado.
-   Una aplicación de servidor de llamada a procedimiento remoto (RPC) de Microsoft puede llamar a la función [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para suplantar a un cliente.
-   Un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) o un servidor de aplicaciones puede llamar a la función [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar a un cliente.

Para la mayoría de estas suplantaciones, el subproceso de suplantación puede revertir a su propio contexto de seguridad mediante una llamada a la función [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) . La excepción es la suplantación de RPC, en la que la aplicación de servidor RPC llama a [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) para revertir a su propio contexto de seguridad.

 

 
