---
title: Introducción al escenario de EAPHost de SSO
description: Contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042783"
---
# <a name="sso-eaphost-scenario-overview"></a>Introducción al escenario de EAPHost de SSO

El tema siguiente contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).

## <a name="about-the-scenarios"></a>Acerca de los escenarios

SSO proporciona funcionalidad para conservar información adicional de credenciales de usuario que tradicionalmente se almacena en el BLOB de usuario de EAP. A diferencia de otros procesos de credenciales, los suplicadores habilitados para SSO pueden resolver situaciones de inicio de sesión como la itinerancia de AP y el cambio de contraseña sin intervención del usuario.

## <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamiento del almacenamiento en caché de PIN EAP-TLS de SSO

Un suplicante puede intentar la autenticación de red mediante un método EAP basado en tarjeta inteligente, como Seguridad de la capa de transporte del Protocolo de autenticación extensible (EAP-TLS). En este y otros escenarios similares, el suplicante obtiene el PIN de tarjeta inteligente del usuario y recupera un certificado de usuario para la autenticación de red seguido de una llamada a WinLogin en el equipo local. Después de la autenticación correcta, el suplicante almacena en caché el BLOB de usuario y no almacena la información del PIN del usuario.

Cuando el usuario se desvía a una sesión de ubicación diferente, se debe reanudar y volver a autenticar. Puesto que el certificado no se puede almacenar antes del inicio de sesión, se producirá un error en la autenticación del usuario y el suplicante vaciará el BLOB del usuario. En este momento, se requiere el PIN de usuario para recuperar el certificado de usuario de la tarjeta inteligente para la autenticación de red. Dado que SSO almacena en caché el PIN, el certificado se puede recuperar sin intervención del usuario. Sin SSO, EAP-TLS tendría que volver a generar una interfaz de usuario de colección de PIN.

Para obtener un enfoque paso a paso, consulte SSO EAP-TLS PIN Caching Behavior (Comportamiento del almacenamiento en caché de [PIN de EAP-TLS de SSO).](sso-eap-tls-pin-caching-behavior-.md)

## <a name="sso-password-change-behavior"></a>Comportamiento de cambio de contraseña de SSO

Un suplicante puede intentar la autenticación de red mediante un método EAP basado en contraseña, como microsoft Challenge Handshake Authentication Protocol versión 2.0 (MS-CHAPv2), configurado para usar credenciales de WinLogin. En este escenario, el suplicante recopila las credenciales de usuario una vez y las proporciona a EAPHost para la autenticación de red. Después de la autenticación de red correcta, el suplicante usa el mismo conjunto de credenciales para WinLogin.

Sin embargo, si las credenciales como la contraseña de usuario se cambiaron durante la autenticación de red sin un suplicante habilitado para SSO, la llamada posterior a WinLogin provocará un error. SSO conserva las nuevas credenciales y permite un WinLogin correcto sin intervención adicional del usuario.

Para obtener un enfoque paso a paso, consulte Comportamiento de cambio de contraseña [de SSO.](sso-password-change-behavior-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




