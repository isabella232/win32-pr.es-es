---
title: Instalación y configuración de aplicaciones RPC
description: Cuando microsoft Windows sistema operativo está instalado en un servidor o cliente, el programa de instalación instala automáticamente los archivos en tiempo de ejecución de RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Llamada a procedimiento remoto RPC, tareas, instalación y configuración de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5cf5d408e2b23042074031ce0307b3a13cf3461df31cc39899b0315f99e8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020445"
---
# <a name="installing-and-configuring-rpc-applications"></a>Instalación y configuración de aplicaciones RPC

Cuando microsoft Windows sistema operativo está instalado en un servidor o cliente, el programa de instalación instala automáticamente los archivos en tiempo de ejecución de RPC. No se requiere ninguna otra instalación de RPC. Sin embargo, debe asegurarse de que la versión de Windows que instala admita todas las características que se usan en la aplicación distribuida.

Cuando se usa una aplicación RPC en un sistema operativo Windows 3.x o Microsoft MS-DOS, debe copiar los archivos ejecutables en tiempo de ejecución de RPC en los equipos Windows 3.x o MS-DOS que van a usar la aplicación. El directorio \\ mstools rpc rt16 en el CD del Kit de desarrollo de software de plataforma (SDK) contiene una imagen de disco de estos archivos junto con un programa de instalación para \\ \_ instalar los archivos. Use esta imagen de disco para crear un disco de instalación para su distribución con la aplicación RPC. También puede usar aplicaciones cliente de 16 bits destinadas a MS-DOS o Windows en un sistema operativo de 32 bits/64 Windows bits. Sin embargo, el programa de instalación de la aplicación debe instalar los archivos ejecutables contenidos en esta imagen de disco.

Al compilar una aplicación RPC para un cliente Macintosh, debe vincular los archivos necesarios a la aplicación en tiempo de compilación. No se necesita ninguna instalación rpc adicional.

Para obtener más información sobre los archivos redistribuibles y los contratos de licencia, \\ consulte LICENSERedist.txt y LICENSELicense.txt en el CD de Platform \\ \\ \\ SDK.

Esta sección contiene información sobre cómo configurar aplicaciones RPC en una variedad de plataformas de hardware y software. Presenta la explicación en las secciones siguientes:

-   [Configuración del proveedor de servicios de nombres](configuring-the-name-service-provider.md)
-   [Información del Registro](registry-information.md)
-   [Uso de RPC con Winsock Proxy](using-rpc-with-winsock-proxy.md)
-   [Instalación de SPX/IPX](spx-ipx-installation.md)
-   [Configuración del servidor de seguridad](configuring-the-security-server.md)

 

 




