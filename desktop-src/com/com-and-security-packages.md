---
title: Com y paquetes de seguridad
description: Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación Kerberos v5 y el paquete de seguridad Schannel, que proporciona los protocolos PCT 1.0, SSL 2.0, SSL 3.0 y TLS 1.0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ec80a1ea610725716da3640b6e38b2fd0f3282ce6ce778e632c6a5c8e72c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048723"
---
# <a name="com-and-security-packages"></a>Com y paquetes de seguridad

Windows admite NTLMSSP (proveedor de compatibilidad de seguridad de LAN Manager), el protocolo de autenticación Kerberos v5 y el paquete de seguridad Schannel, que proporciona los protocolos PCT 1.0, SSL 2.0, SSL 3.0 y TLS 1.0. También se admite Snego, que comprueba los paquetes de seguridad disponibles y selecciona el más adecuado.

En la tabla siguiente se muestran los niveles de autenticación admitidos por los distintos paquetes de seguridad.



| Autenticación de servidor/cliente                                                                                           | Compatibilidad con paquetes de seguridad                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Ninguno de los dos puede obtener el nombre del otro.<br/>                                                                      | Ninguno<br/>                                                  |
| El cliente puede autenticar el servidor, pero no viceversa.<br/>                                                 | Schannel<br/>                                              |
| El cliente no puede detectar el servidor, pero el servidor puede obtener el identificador de usuario del cliente.<br/>                    | NTLMSSP<br/>                                               |
| Autenticación mutua: tanto el cliente como el servidor pueden conocer el nombre del otro, si se concede el permiso.<br/> | NTLMSSP (localmente), el protocolo Kerberos v5 y Schannel<br/> |



 

Para obtener más información sobre estos paquetes de seguridad, vea los temas siguientes en esta sección:

-   [NTLMSSP](ntlmssp.md)
-   [Protocolo Kerberos v5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 





