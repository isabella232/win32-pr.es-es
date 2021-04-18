---
title: COM y paquetes de seguridad
description: Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación de Kerberos V5 y el paquete de seguridad de Schannel, que proporciona los protocolos PCT 1,0, SSL 2,0, SSL 3,0 y TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714147"
---
# <a name="com-and-security-packages"></a>COM y paquetes de seguridad

Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación de Kerberos V5 y el paquete de seguridad de Schannel, que proporciona los protocolos PCT 1,0, SSL 2,0, SSL 3,0 y TLS 1,0. También se admite Snego, que comprueba los paquetes de seguridad disponibles y selecciona el más apropiado.

En la tabla siguiente se muestran los niveles de autenticación que admiten los distintos paquetes de seguridad.



| Autenticación de servidor/cliente                                                                                           | Compatibilidad con paquetes de seguridad                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Ninguno de ellos puede obtener el nombre del otro.<br/>                                                                      | None<br/>                                                  |
| El cliente puede autenticar el servidor, pero no viceversa.<br/>                                                 | Schannel<br/>                                              |
| El cliente no puede detectar el servidor, pero el servidor puede obtener el identificador de usuario del cliente.<br/>                    | NTLMSSP<br/>                                               |
| Autenticación mutua: el cliente y el servidor pueden conocer el nombre del otro si se concede el permiso.<br/> | NTLMSSP (localmente), protocolo Kerberos V5 y Schannel<br/> |



 

Para obtener más información acerca de estos paquetes de seguridad, vea los temas siguientes en esta sección:

-   [NTLMSSP](ntlmssp.md)
-   [Protocolo Kerberos V5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 





