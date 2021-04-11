---
title: Información general sobre el escenario EAPHost de SSO
description: Contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149015"
---
# <a name="sso-eaphost-scenario-overview"></a>Información general sobre el escenario EAPHost de SSO

El siguiente tema contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).

## <a name="about-the-scenarios"></a>Acerca de los escenarios

SSO proporciona funcionalidad para conservar la información adicional de credenciales de usuario que tradicionalmente se almacena en el BLOB de usuario de EAP. A diferencia de otros procesos de credenciales, los suplicantes habilitados para SSO pueden resolver situaciones de inicio de sesión como itinerancia de AP y cambio de contraseña sin intervención del usuario.

## <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamiento de almacenamiento en caché de PIN EAP-TLS

Un suplicante puede intentar la autenticación de red mediante un método EAP basado en tarjeta inteligente, como la seguridad de la capa de transporte del Protocolo de autenticación extensible (EAP-TLS). En este escenario y otros similares, el solicitante obtiene el PIN de la tarjeta inteligente del usuario y recupera un certificado de usuario para la autenticación de red seguido de una llamada a WinLogin en el equipo local. Después de la autenticación correcta, el solicitante almacena en caché el BLOB del usuario y no almacena la información del PIN del usuario.

Cuando el usuario se desplaza a una nueva sesión de ubicación, se debe reanudar y volver a realizar la autenticación. Dado que el certificado no se puede almacenar previamente, se producirá un error en la autenticación del usuario y el solicitante vaciará el BLOB del usuario. En este momento, se necesita el PIN de usuario para recuperar el certificado de usuario de la tarjeta inteligente para la autenticación de red. Dado que SSO almacena en caché el PIN, el certificado se puede recuperar sin intervención del usuario. Sin SSO, EAP-TLS tendría que volver a generar una interfaz de usuario de colección de PIN.

Para obtener un enfoque paso a paso, consulte [comportamiento del almacenamiento en caché del PIN EAP-TLS de SSO](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Comportamiento de cambio de contraseña de SSO

Un suplicante puede intentar la autenticación de red mediante un método EAP basado en contraseña, como el protocolo de autenticación por desafío mutuo de Microsoft versión 2,0 (MS-CHAPv2), configurado para usar las credenciales de WinLogin. En este escenario, el solicitante recopila las credenciales de usuario una vez y las proporciona a EAPHost para la autenticación de red. Después de la autenticación de red correcta, el suplicante usa el mismo conjunto de credenciales para WinLogin.

Sin embargo, si se cambiaron credenciales como la contraseña de usuario durante la autenticación de red sin un suplicante habilitado para SSO, la siguiente llamada a WinLogin producirá un error. SSO conserva las nuevas credenciales y permite un WinLogin correcto sin la intervención del usuario adicional.

Para obtener un enfoque paso a paso, consulte [comportamiento del cambio de contraseña de SSO](sso-password-change-behavior-.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




