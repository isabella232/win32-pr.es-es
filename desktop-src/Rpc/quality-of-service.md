---
title: Calidad de servicio (RPC)
description: Los programas cliente pueden usar la función RpcBindingSetAuthInfoEx en lugar de la función RpcBindingSetAuthInfo para crear un enlace autenticado.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d7c68386a5d7db4f59b620bc998d628faa2969671ef99b5c5fc2c65aadeb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927153"
---
# <a name="quality-of-service-rpc"></a>Calidad de servicio (RPC)

Los programas cliente pueden usar [**la función RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) en lugar de [**la función RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para crear un enlace autenticado. Si lo hacen, pasan un puntero a una estructura [**\_ \_ QOS DE SEGURIDAD RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) como parámetro final de **RpcBindingSetAuthInfoEx**. Esta estructura contiene información sobre la calidad del servicio. Los programas cliente también pueden especificar el seguimiento de identidades y seleccionar el tipo de suplantación.

Use el **miembro Capabilities** de la estructura [**\_ \_ QOS de seguridad rpc**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) para establecer qué partes de la aplicación cliente/servidor se autentican. Si se selecciona RPC C QOS CAPABILITIES DEFAULT ,la biblioteca rpc en tiempo de ejecución autentica el cliente o servidor de acuerdo con el valor predeterminado \_ \_ para el \_ \_ SSP. De forma predeterminada, el protocolo Kerberos SSP autentica el cliente y el servidor. El valor predeterminado para todos los demás SSP que proporciona Microsoft es autenticar el cliente en el servidor, pero no autenticar el servidor en el cliente.

Si el cliente y el servidor deben autenticarse siempre entre sí, establezca el miembro **Capabilities** de la estructura [**\_ \_ QOS**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) de seguridad rpc en RPC \_ C \_ QOS \_ CAPABILITIES MUTUAL \_ \_ AUTH. Es posible que algunos proveedores de seguridad no admitan la autenticación mutua. Si se \_ especifica RPC C QOS CAPABILITIES MUTUAL AUTH para estos proveedores de seguridad, se devuelve un error cuando se realiza una llamada \_ a procedimiento \_ \_ \_ remoto. Cuando se usa SCHANNEL SSP, también es posible establecer el miembro **Capabilities** en RPC \_ C \_ QOS CAPABILITIES ANY \_ \_ \_ AUTHORITY. Esta constante especifica que el SSP validará la llamada a procedimiento remoto incluso si la entidad de certificación que emitió el certificado de autenticación del cliente no está en el almacén de certificados raíz del SSP. El valor predeterminado es rechazar el certificado si el SSP no reconoce la entidad de certificación. La entidad de certificación es una empresa u organización independiente, como VeriSign, que emite certificados de autenticación.

Las aplicaciones también pueden establecer el seguimiento de identidades que usa la biblioteca en tiempo de ejecución rpc. Por lo general, los programas [*usan el seguimiento de identidades estáticas.*](s-glos.md) Con el seguimiento estático, las credenciales del cliente se establecen cuando llama a la [**función RpcBindingSetAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) A continuación, la biblioteca en tiempo de ejecución rpc usa esas credenciales para todas las llamadas RPC en el enlace, independientemente de los cambios en la identidad del subproceso de llamada o el proceso de llamada. Las aplicaciones también pueden seleccionar [*el seguimiento dinámico de identidades.*](d-glos.md) El seguimiento dinámico de identidades indica a la biblioteca en tiempo de ejecución rpc que use las credenciales del subproceso que realiza la llamada en el momento de cada llamada, en lugar del identificador de enlace. El seguimiento de identidades predeterminado es estático.

Si la identidad del cliente no va a cambiar, el seguimiento de identidades estáticas puede tener mejores características de rendimiento y puede ahorrar el tiempo de ejecución de RPC de comprobar cada vez si la identidad en el subproceso que realiza la llamada es la misma que la identidad dada al sistema de seguridad. Si la identidad del subproceso que realiza la llamada puede cambiar entre llamadas y el servidor necesita reconocer esos cambios, es mejor especificar el seguimiento dinámico de identidades: el tiempo de ejecución de RPC realiza un seguimiento de la identidad de forma silenciosa y eficaz, y si cambia la identidad, administra ese cambio en su nombre.

> [!Note]  
> En el caso de las llamadas **ncalrpc,** el seguimiento de identidades estáticas y dinámicas tiene características de rendimiento diferentes y, en función de las circunstancias, puede ser más rápido.

 

Como parte de la especificación qos, el programa cliente también puede establecer el tipo de suplantación que un programa de servidor puede realizar en su nombre. Para obtener más información, vea [Suplantación de cliente.](client-impersonation.md)

El campo número de versión de la [**estructura \_ \_ QOS de seguridad RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) siempre debe establecerse en RPC C SECURITY \_ \_ \_ QOS \_ VERSION.

 

 




