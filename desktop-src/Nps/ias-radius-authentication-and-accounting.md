---
title: Autenticación, autorización y contabilidad RADIUS
description: NPS admite totalmente el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS). El protocolo RADIUS es el estándar de facto para la autenticación de usuario remoto y se documenta en RFC 2865 y RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063512"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Autenticación, autorización y contabilidad RADIUS

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

NPS admite totalmente el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS). El protocolo RADIUS es el estándar de facto para la autenticación de usuario remoto y se documenta en [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-authentication-and-authorization"></a>Autenticación y autorización RADIUS

En el diagrama siguiente se muestra un cliente de autenticación ("Usuario") que se conecta a un servidor de acceso a redes (NAS) a través de una conexión de acceso telefónico, mediante Protocolo punto a punto (PPP). Para autenticar al usuario, el NAS se pone en contacto con un servidor remoto que ejecuta NPS. El nas y el servidor NPS se comunican mediante el protocolo RADIUS.

![autenticación de usuario remoto](images/ias01.png)

Un NAS funciona como un cliente de un servidor o servidores que admiten el protocolo RADIUS. Los servidores que admiten el protocolo RADIUS se conocen generalmente como servidores RADIUS. El cliente RADIUS, es decir, el NAS, pasa información sobre el usuario a los servidores RADIUS designados y, a continuación, actúa sobre la respuesta que devuelven los servidores. La solicitud enviada por el NAS al servidor RADIUS para autenticar al usuario suele denominarse "solicitud de autenticación".

Si un servidor RADIUS autentica correctamente al usuario, el servidor RADIUS devuelve información de configuración al NAS para que pueda proporcionar servicio de red al usuario. Esta información de configuración se compone de "autorizaciones" y contiene, entre otras, el tipo de servicio que NAS puede proporcionar al usuario (por ejemplo, PPP o telnet).

Mientras el servidor RADIUS procesa la solicitud de autenticación, puede realizar funciones de autorización como comprobar el número de teléfono del usuario y comprobar si el usuario ya tiene una sesión en curso. El servidor RADIUS puede determinar si el usuario ya tiene una sesión en curso ponerse en contacto con un servidor de estado.

Para obtener más información sobre la autenticación y autorización RADIUS, [vea RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>Contabilidad RADIUS

El servidor RADIUS también recopila una variedad de información enviada por el NAS que se puede usar para la contabilidad y para informar sobre la actividad de red. El cliente RADIUS envía información a los servidores RADIUS designados cuando el usuario inicia sesión y cierra sesión. El cliente RADIUS puede enviar información de uso adicional periódicamente mientras la sesión está en curso. Las solicitudes enviadas por el cliente al servidor para registrar la información de inicio y cierre de sesión y uso se denominan generalmente "solicitudes de contabilidad".

Para obtener más información sobre la contabilidad RADIUS, [vea RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Un servidor RADIUS puede actuar como un cliente proxy para otros servidores RADIUS. En estos casos, el servidor RADIUS contactado por el NAS pasa la solicitud de autenticación o contabilidad a otro servidor RADIUS que realmente realiza la autenticación o la tarea de contabilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de autenticación de Internet y servidor de directivas de red](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Paquetes de contabilidad RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 