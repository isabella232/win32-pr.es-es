---
title: Niveles de suplantación (COM)
description: Si la suplantación se realiza correctamente, significa que el cliente ha acordado dejar que el servidor sea el cliente hasta cierto punto.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904833"
---
# <a name="impersonation-levels"></a>Niveles de suplantación

Si la suplantación se realiza correctamente, significa que el cliente ha acordado dejar que el servidor sea el cliente hasta cierto punto. Los distintos grados de suplantación se denominan *niveles de suplantación* e indican la cantidad de autoridad que se asigna al servidor cuando suplanta al cliente.

Actualmente, hay cuatro niveles de suplantación: *anónimo*, *identificación*, *Suplantar* y *delegado*. En la lista siguiente se describe brevemente cada nivel de suplantación:

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anónimo ( \_ nivel Imp de RPC C \_ \_ \_ anónimo)
</dt> <dd>

El cliente es anónimo para el servidor. El proceso de servidor puede suplantar al cliente, pero el token de suplantación no contiene información sobre el cliente. Este nivel solo se admite en el transporte de comunicación local entre procesos. Todos los demás transportes promueven de forma silenciosa este nivel para identificar.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>Identify ( \_ \_ \_ identificación del nivel Imp de RPC C \_ )
</dt> <dd>

Nivel predeterminado del sistema. El servidor puede obtener la identidad del cliente y suplantarlo para realizar comprobaciones ACL.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate ( \_ la \_ \_ suplantación de nivel Imp de RPC C \_ )
</dt> <dd>

El servidor puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre. El servidor puede obtener acceso a los recursos locales como el cliente. Si el servidor es local, puede tener acceso a los recursos de red como el cliente. Si el servidor es remoto, solo podrá tener acceso a los recursos que se encuentren en el mismo equipo que el servidor.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegado (delegado de nivel de Imp de RPC \_ C \_ \_ \_ )
</dt> <dd>

Nivel de suplantación más completo. Cuando se selecciona este nivel, el servidor (ya sea local o remoto) puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre. Durante la suplantación, las credenciales del cliente (locales y de red) se pueden pasar a cualquier número de equipos.

Para que la suplantación funcione en el nivel de delegado, deben cumplirse los siguientes requisitos:

-   El cliente debe establecer el nivel de suplantación en \_ el \_ delegado de nivel Imp de RPC C \_ \_ .
-   La cuenta de cliente no debe estar marcada como "la cuenta es importante y no se puede delegar" en el servicio de Active Directory.
-   La cuenta del servidor se debe marcar con el atributo "Trusted for delegation" en el servicio de Active Directory.
-   Los equipos que hospedan el cliente, el servidor y los servidores de "nivel inferior" deben ejecutarse en un dominio.

</dd> </dl>

Al elegir el nivel de suplantación, el cliente indica al servidor hasta qué punto puede llegar a suplantar al cliente. El cliente establece el nivel de suplantación en el proxy que usa para comunicarse con el servidor.

## <a name="setting-the-impersonation-level"></a>Establecimiento del nivel de suplantación

Hay dos maneras de establecer el nivel de suplantación:

-   El cliente puede establecerlo en processwide, a través de una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Un cliente puede establecer la seguridad de nivel de proxy en una interfaz de un objeto remoto a través de una llamada a [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o la función auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Establezca el nivel de suplantación pasando un \_ valor XXX de nivel de Imp de RPC C adecuado \_ \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del parámetro *dwImpLevel* .

Distintos servicios de autenticación admiten la suplantación de nivel de delegado en diferentes extensiones. Por ejemplo, NTLMSSP admite la suplantación multiproceso y de nivel de delegado entre procesos, pero no entre equipos. Por otro lado, el protocolo Kerberos admite la suplantación de nivel de delegado a través de los límites del equipo, mientras que Schannel no admite la suplantación en el nivel de delegado. Si tiene un proxy en el nivel de suplantación y desea establecer el nivel de suplantación en Delegate, debe llamar a [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con las constantes predeterminadas para cada parámetro, excepto el nivel de suplantación. COM elegirá NTLM localmente y el protocolo Kerberos de forma remota (cuando el protocolo Kerberos funcione).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> </dl>

 

 