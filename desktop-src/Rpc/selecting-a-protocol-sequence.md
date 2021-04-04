---
title: Seleccionar una secuencia de protocolo
description: Una secuencia de protocolo es el idioma que utiliza un sistema operativo de red para comunicarse a través de la red con otros equipos.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076174"
---
# <a name="selecting-a-protocol-sequence"></a>Seleccionar una secuencia de protocolo

Una secuencia de protocolo es el idioma que utiliza un sistema operativo de red para comunicarse a través de la red con otros equipos. En términos más específicos, las aplicaciones RPC deben especificar una cadena que represente una combinación de un protocolo RPC, un protocolo de transporte y un protocolo de red.

Microsoft RPC admite tres protocolos RPC:

-   Protocolo orientado a la conexión de arquitectura de informática de red (NCACN)
-   Protocolo de datagramas de arquitectura de informática de red (NCADG)
-   Llamada a procedimiento remoto local de arquitectura de informática de red (NCALRPC)

Las aplicaciones RPC pueden usar el protocolo NCALRPC para invocar los procedimientos que ofrecen los programas de servidor que se ejecutan en el mismo equipo en el que se ejecuta el programa cliente. En este momento, es el método más eficaz para llamar a la funcionalidad en un proceso diferente en el mismo equipo.

Los protocolos de red y transporte que utiliza la aplicación dependen de los protocolos que admite la red. Muchas redes hoy en día, incluido Internet, admiten TCP/IP. Otros protocolos de red y transporte comunes son IPX/SPX, NetBIOS y AppleTalk DSP. Microsoft RPC es compatible con estos y otros protocolos de red y transporte. Para obtener una lista completa, vea [constantes de secuencia de protocolos](protocol-sequence-constants.md).

Cuando la aplicación utiliza identificadores de enlace automáticos, no es necesario especificar la secuencia de protocolos. Si usa identificadores implícitos o explícitos, debe obtener o especificar la secuencia de protocolo. Cada sistema distribuido debe examinar el entorno en el que se implementará para determinar qué secuencia de protocolo es más adecuada para ese entorno.

No todas las secuencias de protocolo tienen una funcionalidad equivalente. Los desarrolladores deben comprobar que la secuencia de protocolos elegida admite las características necesarias. En general, se recomienda **ncalrpc** para las comunicaciones locales y **ncacn \_ IP \_ TCP** o **ncacn \_ http** para las comunicaciones remotas; funcionan en todos los entornos, tienen un rendimiento óptimo y admiten todas las características necesarias y prácticas recomendadas.

Los clientes también pueden especificar la información de la secuencia de protocolos que obtienen de Active Directory, el registro, las variables de entorno creadas y inicializadas por el programa de instalación, los archivos de configuración específicos de la aplicación o las cadenas literales del código fuente del programa.

Una vez que el programa cliente tiene una cadena de secuencia de protocolo válida, puede pasar esa información a las funciones [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) y [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para crear el identificador de enlace.

 

 




