---
title: Acerca de Servicios de Escritorio remoto
description: Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) proporciona una funcionalidad similar a un entorno basado en terminal, host centralizado o sistema central, en el que varios terminales se conectan a un equipo host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073382"
---
# <a name="about-remote-desktop-services"></a>Acerca de Servicios de Escritorio remoto

Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) proporciona una funcionalidad similar a un entorno basado en terminal, host centralizado o sistema central, en el que varios terminales se conectan a un equipo host. Cada terminal proporciona un conduit para la entrada y salida entre un usuario y el equipo host. Un usuario puede iniciar sesión en un terminal y, a continuación, ejecutar aplicaciones en el equipo host, acceder a archivos, bases de datos, recursos de red, entre otros. Cada sesión de terminal es independiente, y el sistema operativo host administra los conflictos entre varios usuarios que contendían por recursos compartidos.

La principal diferencia entre Servicios de Escritorio remoto y el entorno del sistema central tradicional es que los terminales descuentas de un entorno de sistema central solo proporcionan entrada y salida basadas en caracteres. Un emulador o cliente de Conexión a Escritorio remoto (RDC) proporciona una interfaz gráfica de usuario completa que incluye un escritorio de sistema operativo Windows y compatibilidad con una variedad de dispositivos de entrada, como un teclado y un mouse.

En el Servicios de Escritorio remoto remoto, una aplicación se ejecuta completamente en el servidor Escritorio remoto Session Host (host de sesión de Escritorio remoto) (anteriormente conocido como terminal server). El cliente RDC no realiza ningún procesamiento local del software de la aplicación. El servidor transmite la interfaz gráfica de usuario al cliente. El cliente transmite la entrada del usuario al servidor.

Para obtener más información, vea los temas siguientes:

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Modificar el valor predeterminado de redirección de dispositivos](modify-device-redirection-default-.md)
</dt> <dd>

Dado que Escritorio remoto Gateway intenta aplicar directivas de redireccionamiento de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión de Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.

</dd> <dt>

[Protocolo de escritorio remoto](remote-desktop-protocol.md)
</dt> <dd>

El Escritorio remoto de Microsoft remoto (RDP) proporciona funcionalidades de visualización y entrada remotas a través de conexiones de red para aplicaciones basadas Windows que se ejecutan en un servidor.

</dd> <dt>

[Servicios de Escritorio remoto API](terminal-services-api.md)
</dt> <dd>

La API Servicios de Escritorio remoto es principalmente útil para aplicaciones cliente/servidor y aplicaciones para Servicios de Escritorio remoto administración.

</dd> <dt>

[Servicios de Escritorio remoto de administración de aplicaciones](terminal-services-management-applications.md)
</dt> <dd>

Describe las aplicaciones de administración que Servicios de Escritorio remoto admite.

</dd> <dt>

[Servicios de Escritorio remoto de programación](terminal-services-programming-guidelines.md)
</dt> <dd>

Temas que proporcionan instrucciones para desarrollar aplicaciones en un entorno Servicios de Escritorio remoto trabajo.

</dd> <dt>

[Escritorio remoto sesiones](terminal-services-sessions.md)
</dt> <dd>

Dado que cada inicio de sesión en un cliente de Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de oficina y un equipo principal.

</dd> <dt>

[Conexión web a Escritorio remoto](remote-desktop-web-connection.md)
</dt> <dd>

Describe cómo instalar un Conexión web a Escritorio remoto.

</dd> <dt>

[Recursos en un servidor host Escritorio remoto sesión local](resources-on-a-terminal-server.md)
</dt> <dd>

Varios usuarios pueden iniciar sesión simultáneamente en un único servidor host de sesión de Escritorio remoto, compartiendo los recursos de hardware y software del servidor.

</dd> <dt>

[Novedades de Servicios de Escritorio remoto](what-s-new-in-terminal-services.md)
</dt> <dd>

Temas que describen los cambios en cada versión de Servicios de Escritorio remoto API.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conectarse a otro equipo mediante la Conexión a Escritorio remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




