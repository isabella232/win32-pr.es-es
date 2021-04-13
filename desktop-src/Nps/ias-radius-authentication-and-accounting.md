---
title: Autenticación, autorización y cuentas RADIUS
description: NPS es totalmente compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS). El protocolo RADIUS es el estándar de facto para la autenticación de usuarios remotos y se documenta en RFC 2865 y RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421090"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Autenticación, autorización y cuentas RADIUS

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

NPS es totalmente compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS). El protocolo RADIUS es el estándar de facto para la autenticación de usuarios remotos y se documenta en [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-authentication-and-authorization"></a>Autenticación y autorización RADIUS

En el diagrama siguiente se muestra un cliente de autenticación ("usuario") que se conecta a un servidor de acceso a la red (NAS) a través de una conexión de acceso telefónico mediante el Protocolo punto a punto (PPP). Para autenticar al usuario, el NAS se pone en contacto con un servidor remoto que ejecuta NPS. El NAS y el servidor NPS se comunican mediante el protocolo RADIUS.

![autenticación de usuario remoto](images/ias01.png)

Un NAS funciona como cliente de un servidor o servidores que admiten el protocolo RADIUS. Los servidores que admiten el protocolo RADIUS se conocen normalmente como servidores RADIUS. El cliente RADIUS, es decir, el servidor NAS, pasa información sobre el usuario a los servidores RADIUS designados y, a continuación, actúa en la respuesta que los servidores devuelven. La solicitud enviada por el NAS al servidor RADIUS para autenticar al usuario suele denominarse "solicitud de autenticación".

Si un servidor RADIUS autentica el usuario correctamente, el servidor RADIUS devuelve la información de configuración al NAS para que pueda proporcionar el servicio de red al usuario. Esta información de configuración se compone de "autorizaciones" y contiene, entre otras, el tipo de servicio NAS que puede proporcionar al usuario (por ejemplo, PPP o Telnet).

Mientras el servidor RADIUS está procesando la solicitud de autenticación, puede realizar funciones de autorización como comprobar el número de teléfono del usuario y comprobar si el usuario ya tiene una sesión en curso. El servidor RADIUS puede determinar si el usuario ya tiene una sesión en curso poniéndose en contacto con un servidor de estado.

Para obtener más información sobre la autenticación y autorización RADIUS, consulte [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>Cuentas RADIUS

El servidor RADIUS también recopila una gran variedad de información enviada por el NAS que se puede usar para la contabilidad y para informar sobre la actividad de la red. El cliente RADIUS envía información a los servidores RADIUS designados cuando el usuario inicia sesión y cierra la sesión. El cliente RADIUS puede enviar información de uso adicional periódicamente mientras la sesión está en curso. Las solicitudes enviadas por el cliente al servidor para registrar la información de inicio y cierre de sesión y uso se suelen denominar "solicitudes de contabilidad".

Para obtener más información sobre las cuentas RADIUS, consulte [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Un servidor RADIUS puede actuar como cliente proxy para otros servidores RADIUS. En estos casos, el servidor RADIUS contactado por el NAS pasa la solicitud de autenticación o de cuentas a otro servidor RADIUS que realmente realiza la autenticación o la tarea de contabilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de autenticación de Internet y servidor de directivas de redes](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Paquetes de cuentas RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 