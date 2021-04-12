---
description: El protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) es un proveedor de compatibilidad de seguridad que se implementa mediante la interfaz del proveedor de compatibilidad para seguridad (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Proveedor de compatibilidad con seguridad de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275797"
---
# <a name="credential-security-support-provider"></a>Proveedor de compatibilidad con seguridad de credenciales

El protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) es un proveedor de compatibilidad de seguridad que se implementa mediante la interfaz del proveedor de compatibilidad para seguridad ([SSPI](sspi.md)). CredSSP permite a una aplicación delegar las credenciales del usuario desde el cliente al servidor de destino para la autenticación remota. CredSSP proporciona un canal de [Protocolo de seguridad de capa de transporte](transport-layer-security-protocol.md) cifrado. El cliente se autentica a través del canal cifrado mediante el Protocolo simple y protegido Negotiate (SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM](microsoft-ntlm.md).

> [!Caution]  
> Esta no es una delegación restringida. CredSSP pasa las credenciales completas del usuario al servidor sin ninguna restricción.

 

Para obtener información sobre SPNEGO, consulte [Microsoft Negotiate](microsoft-negotiate.md).

Una vez autenticado el cliente y el servidor, el cliente pasa las credenciales del usuario al servidor. Las credenciales se cifran doble bajo las claves de sesión SPNEGO y TLS. CredSSP admite el inicio de sesión basado en contraseña, así como el inicio de sesión de tarjeta inteligente basado en [*X. 509*](/windows/desktop/SecGloss/x-gly) y PKINIT.

> [!IMPORTANT]
> CredSSP no es compatible con los clientes de WOW64.

 

Para obtener más información acerca de CredSSP, vea los temas siguientes.



| Tema                                                                         | Descripción                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Configuración de directiva de grupo CredSSP](credssp-group-policy-settings.md)<br/> | La delegación de credenciales por CredSSP se puede controlar mediante la configuración de directiva de grupo.<br/> |



 

 

