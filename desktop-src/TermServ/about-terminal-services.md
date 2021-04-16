---
title: Acerca de Servicios de Escritorio remoto
description: Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685612"
---
# <a name="about-remote-desktop-services"></a>Acerca de Servicios de Escritorio remoto

Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host. Cada terminal proporciona un conducto para la entrada y la salida entre un usuario y el equipo host. Un usuario puede iniciar sesión en un terminal y, a continuación, ejecutar aplicaciones en el equipo host, tener acceso a archivos, bases de datos, recursos de red, etc. Cada sesión de terminal es independiente, con el sistema operativo host que administra los conflictos entre varios usuarios que compiten por recursos compartidos.

La principal diferencia entre Servicios de Escritorio remoto y el entorno de mainframe tradicional es que los terminales no de un entorno de gran sistema solo proporcionan entradas y salidas basadas en caracteres. Un emulador o cliente Conexión a Escritorio remoto (RDC) proporciona una interfaz gráfica de usuario completa que incluye un escritorio del sistema operativo Windows y compatibilidad con una variedad de dispositivos de entrada, como un teclado y un mouse.

En el entorno de Servicios de Escritorio remoto, una aplicación se ejecuta completamente en el servidor de host de sesión Escritorio remoto (host de sesión de escritorio remoto) (anteriormente conocido como servidor de Terminal Server). El cliente RDC no realiza ningún procesamiento local del software de la aplicación. El servidor transmite la interfaz gráfica de usuario al cliente. El cliente vuelve a transmitir la entrada del usuario al servidor.

Para obtener más información, vea los siguientes temas.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Modificar el valor predeterminado de redirección del dispositivo](modify-device-redirection-default-.md)
</dt> <dd>

Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.

</dd> <dt>

[Protocolo de escritorio remoto](remote-desktop-protocol.md)
</dt> <dd>

El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor.

</dd> <dt>

[API de Servicios de Escritorio remoto](terminal-services-api.md)
</dt> <dd>

La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.

</dd> <dt>

[Aplicaciones de administración de Servicios de Escritorio remoto](terminal-services-management-applications.md)
</dt> <dd>

Describe las aplicaciones de administración que Servicios de Escritorio remoto admite.

</dd> <dt>

[Instrucciones de programación de Servicios de Escritorio remoto](terminal-services-programming-guidelines.md)
</dt> <dd>

Temas que proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.

</dd> <dt>

[Sesiones de Escritorio remoto](terminal-services-sessions.md)
</dt> <dd>

Dado que cada inicio de sesión en un cliente de Conexión a Escritorio remoto (RDC) recibe un identificador de sesión independiente, la experiencia del usuario es similar a iniciar sesión en varios equipos al mismo tiempo. por ejemplo, un equipo de Office y un equipo doméstico.

</dd> <dt>

[Conexión web a Escritorio remoto](remote-desktop-web-connection.md)
</dt> <dd>

Describe cómo instalar un Conexión web a Escritorio remoto.

</dd> <dt>

[Recursos en un servidor host de sesión Escritorio remoto](resources-on-a-terminal-server.md)
</dt> <dd>

Varios usuarios pueden iniciar sesión simultáneamente en un solo servidor host de sesión de escritorio remoto, compartiendo los recursos de hardware y software del servidor.

</dd> <dt>

[Novedades de Servicios de Escritorio remoto](what-s-new-in-terminal-services.md)
</dt> <dd>

Temas que describen los cambios en cada versión de la API de Servicios de Escritorio remoto.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conectarse a otro equipo mediante la Conexión a Escritorio remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




