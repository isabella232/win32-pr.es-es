---
title: Instalación y configuración de aplicaciones RPC
description: Cuando el sistema operativo Microsoft Windows se instala en un servidor o un cliente, el programa de instalación instala automáticamente los archivos de tiempo de ejecución de RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Llamada a procedimiento remoto RPC, tareas, instalación y configuración de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487042"
---
# <a name="installing-and-configuring-rpc-applications"></a>Instalación y configuración de aplicaciones RPC

Cuando el sistema operativo Microsoft Windows se instala en un servidor o un cliente, el programa de instalación instala automáticamente los archivos de tiempo de ejecución de RPC. No es necesaria ninguna otra instalación de RPC. Sin embargo, debe asegurarse de que la versión de Windows que instale admita todas las características usadas en la aplicación distribuida.

Cuando use una aplicación RPC en un sistema operativo Windows 3. x o Microsoft MS-DOS, debe copiar los archivos ejecutables en tiempo de ejecución de RPC en los equipos con Windows 3. x o MS-DOS que vayan a usar la aplicación. El directorio \\ mstools \\ RPC \_ RT16 del CD del kit de desarrollo de software (SDK) de la plataforma contiene una imagen de disco de estos archivos junto con un programa de instalación para instalar los archivos. Use esta imagen de disco para crear un disco de instalación para la distribución con la aplicación RPC. También puede usar aplicaciones cliente de 16 bits destinadas a MS-DOS o Windows en un sistema operativo Windows de 32 bits o 64 bits. Sin embargo, el programa de instalación de la aplicación debe instalar los archivos ejecutables contenidos en esta imagen de disco.

Al compilar una aplicación RPC para un cliente Macintosh, debe vincular los archivos necesarios a la aplicación en tiempo de compilación. No es necesaria ninguna otra instalación de RPC.

Para obtener más información acerca de los archivos redistribuibles y los contratos de licencia, consulteRedist.txt de licencias \\ \\ y \\ \\License.txt de licencias en el CD de Platform SDK.

Esta sección contiene información sobre cómo configurar las aplicaciones RPC en una variedad de plataformas de hardware y software. Presenta la explicación en las secciones siguientes:

-   [Configurar el proveedor de servicios de nombres](configuring-the-name-service-provider.md)
-   [Información del registro](registry-information.md)
-   [Usar RPC con el proxy Winsock](using-rpc-with-winsock-proxy.md)
-   [Instalación de SPX/IPX](spx-ipx-installation.md)
-   [Configuración del servidor de seguridad](configuring-the-security-server.md)

 

 




