---
title: Niveles de suplantación (COM)
description: Si la suplantación se realiza correctamente, significa que el cliente ha aceptado dejar que el servidor sea el cliente hasta cierto punto.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369544"
---
# <a name="impersonation-levels"></a>Niveles de suplantación

Si la suplantación se realiza correctamente, significa que el cliente ha aceptado dejar que el servidor sea el cliente hasta cierto punto. Los distintos grados de suplantación se denominan niveles de suplantación y indican cuánta autoridad se da al servidor cuando suplanta al cliente. 

Actualmente, hay cuatro niveles de suplantación: *anónimo,* *identificar*, *suplantar* y *delegar*. En la lista siguiente se describe brevemente cada nivel de suplantación:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC \_ C \_ IMP LEVEL \_ \_ ANONYMOUS)
</dt> <dd>

El cliente es anónimo para el servidor. El proceso de servidor puede suplantar al cliente, pero el token de suplantación no contiene información sobre el cliente. Este nivel solo se admite en el transporte de comunicación entre procesos local. Todos los demás transportes promueven silenciosamente este nivel para identificarlo.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY)
</dt> <dd>

Nivel predeterminado del sistema. El servidor puede obtener la identidad del cliente y suplantarlo para realizar comprobaciones ACL.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>suplantar (RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE)
</dt> <dd>

El servidor puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre. El servidor puede obtener acceso a los recursos locales como el cliente. Si el servidor es local, puede acceder a los recursos de red como el cliente. Si el servidor es remoto, solo puede acceder a los recursos que están en el mismo equipo que el servidor.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC \_ C \_ IMP LEVEL \_ \_ DELEGATE)
</dt> <dd>

Nivel de suplantación más completo. Cuando se selecciona este nivel, el servidor (ya sea local o remoto) puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre. Durante la suplantación, las credenciales del cliente (tanto locales como de red) se pueden pasar a cualquier número de equipos.

Para que la suplantación funcione en el nivel de delegado, se deben cumplir los siguientes requisitos:

-   El cliente debe establecer el nivel de suplantación en RPC \_ C \_ IMP LEVEL \_ \_ DELEGATE.
-   La cuenta de cliente no debe marcarse como "La cuenta es confidencial y no se puede delegar" en el servicio Active Directory cliente.
-   La cuenta de servidor debe marcarse con el atributo "Trusted for delegation" (Confianza para delegación) en Active Directory Service.
-   Los equipos que hospedan el cliente, el servidor y los servidores "de bajada" deben ejecutarse en un dominio.

</dd> </dl>

Al elegir el nivel de suplantación, el cliente indica al servidor hasta dónde puede llegar la suplantación del cliente. El cliente establece el nivel de suplantación en el proxy que usa para comunicarse con el servidor.

## <a name="setting-the-impersonation-level"></a>Establecer el nivel de suplantación

Hay dos maneras de establecer el nivel de suplantación:

-   El cliente puede establecerlo en todo el proceso, mediante una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Un cliente puede establecer la seguridad de nivel de proxy en una interfaz de un objeto remoto mediante una llamada a [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o a la función auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Para establecer el nivel de suplantación, pase un valor de RPC C IMP LEVEL xxx adecuado a \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del *parámetro dwImpLevel.*

Los distintos servicios de autenticación admiten la suplantación de nivel de delegado en distintas extensiones. Por ejemplo, NTLMSSP admite la suplantación de nivel de delegado entre subprocesos y procesos, pero no entre equipos. Por otro lado, el protocolo Kerberos admite la suplantación de nivel de delegado a través de los límites del equipo, mientras que Schannel no admite ninguna suplantación en el nivel de delegado. Si tiene un proxy en el nivel de suplantación y desea establecer el nivel de suplantación en delegado, debe llamar a [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) mediante las constantes predeterminadas para cada parámetro, excepto el nivel de suplantación. COM elegirá NTLM localmente y el protocolo Kerberos de forma remota (cuando el protocolo Kerberos funcione).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> </dl>

 

 