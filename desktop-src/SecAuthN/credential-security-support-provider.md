---
description: El protocolo del proveedor de compatibilidad de seguridad de credenciales (CredSSP) es un proveedor de soporte técnico de seguridad que se implementa mediante la interfaz del proveedor de soporte técnico de seguridad (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Proveedor de soporte técnico de seguridad de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4059da0dcc1e6c963ab011ad03415175849191374732f3d1df395914aebe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008743"
---
# <a name="credential-security-support-provider"></a>Proveedor de soporte técnico de seguridad de credenciales

El protocolo del proveedor de compatibilidad de seguridad de credenciales (CredSSP) es un proveedor de soporte técnico de seguridad que se implementa mediante la interfaz del proveedor de soporte técnico de seguridad[(SSPI).](sspi.md) CredSSP permite que una aplicación delegue las credenciales del usuario del cliente al servidor de destino para la autenticación remota. CredSSP proporciona un canal cifrado de protocolo de [seguridad de la capa de](transport-layer-security-protocol.md) transporte. El cliente se autentica a través del canal cifrado mediante el protocolo Simple and Protected Negotiate (SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM.](microsoft-ntlm.md)

> [!Caution]  
> No se trata de una delegación restringida. CredSSP pasa las credenciales completa del usuario al servidor sin ninguna restricción.

 

Para obtener información sobre SPNEGO, vea [Microsoft Negotiate](microsoft-negotiate.md).

Una vez autenticado el cliente y el servidor, el cliente pasa las credenciales del usuario al servidor. Las credenciales se cifran doblemente en las claves de sesión SPNEGO y TLS. CredSSP admite el inicio de sesión basado en contraseña, así como el inicio de sesión con tarjeta inteligente basado en [*X.509*](/windows/desktop/SecGloss/x-gly) y PKINIT.

> [!IMPORTANT]
> CredSSP no admite clientes Wow64.

 

Para obtener más información sobre CredSSP, vea los temas siguientes.



| Tema                                                                         | Descripción                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [CredSSP directiva de grupo Configuración](credssp-group-policy-settings.md)<br/> | La delegación de credenciales por CredSSP se puede controlar mediante la configuración de directiva de grupo.<br/> |



 

 

