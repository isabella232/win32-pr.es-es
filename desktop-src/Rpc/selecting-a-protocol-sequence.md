---
title: Selección de una secuencia de protocolo
description: Una secuencia de protocolo es el lenguaje que usa un sistema operativo de red para hablar a través de la red con otros equipos.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3470c303737f44e7e2d0aa52393fa893efa4634b4a2a4aa5c1bba47a832ae6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127755"
---
# <a name="selecting-a-protocol-sequence"></a>Selección de una secuencia de protocolo

Una secuencia de protocolo es el lenguaje que usa un sistema operativo de red para hablar a través de la red con otros equipos. En términos más específicos, las aplicaciones RPC deben especificar una cadena que represente una combinación de un protocolo RPC, un protocolo de transporte y un protocolo de red.

Rpc de Microsoft admite tres protocolos RPC:

-   Protocolo orientado a conexiones (NCACN) de arquitectura de informática de red
-   Protocolo de datagramas de arquitectura de informática de red (NCADG)
-   Llamada a procedimiento remoto local de arquitectura de informática de red (NCALRPC)

Las aplicaciones RPC pueden usar el protocolo NCALRPC para invocar los procedimientos que ofrecen los programas de servidor que se ejecutan en el mismo equipo en el que se ejecuta el programa cliente. Este es, con diferencia, el método más eficaz para llamar a la funcionalidad en un proceso diferente en el mismo equipo.

Los protocolos de transporte y de red que usa la aplicación dependen de los protocolos que admita la red. Muchas redes de hoy en día, incluido Internet, admiten TCP/IP. Otros protocolos comunes de transporte y red son IPX/SPX, NetBIOS y DSP de AppleTalk. Rpc de Microsoft admite estos y otros protocolos de transporte y red. Para obtener una lista completa, vea [Constantes de secuencia de protocolo.](protocol-sequence-constants.md)

Cuando la aplicación usa identificadores de enlace automáticos, no es necesario especificar la secuencia de protocolo. Si usa identificadores implícitos o explícitos, debe obtener o especificar la secuencia de protocolo. Cada sistema distribuido debe examinar el entorno en el que se implementará para determinar qué secuencia de protocolo es más adecuada para ese entorno.

No todas las secuencias de protocolo tienen una funcionalidad equivalente. Los desarrolladores deben comprobar que la secuencia de protocolo elegida admite las características necesarias. En general, se recomienda **ncalrpc** para las comunicaciones locales y **ncacn \_ ip \_ tcp** o **ncacn \_ http** para las comunicaciones remotas; funcionan en todos los entornos, tienen un rendimiento óptimo y admiten todas las características de procedimientos recomendados necesarias.

Los clientes también pueden especificar la información de secuencia de protocolo que obtienen de Active Directory, el registro, las variables de entorno creadas e inicializadas por el programa de instalación, los archivos de configuración específicos de la aplicación o las cadenas literales del código fuente del programa.

Una vez que el programa cliente tiene una cadena de secuencia de protocolo válida, puede pasar esa información a las funciones [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) y [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para crear el identificador de enlace.

 

 




