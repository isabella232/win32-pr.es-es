---
description: Una aplicación usa la función WSAEnumProtocols para determinar qué protocolos de transporte y cadenas de protocolo están presentes, y para obtener información sobre cada uno de ellos, tal como se incluye en la estructura info de WSAPROTOCOL \_ asociada.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Uso de varios protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9e1641c8e1ed308561b9e85425005933fceac17b156d1161895f13ad06d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739965"
---
# <a name="using-multiple-protocols"></a>Uso de varios protocolos

Una aplicación usa la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para determinar qué protocolos de transporte y cadenas de protocolo están presentes, y para obtener información sobre cada uno de ellos, tal como se encuentra en la estructura info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) asociada.

En la mayoría de los casos, hay una única [**estructura INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada protocolo o cadena de protocolo. Sin embargo, algunos protocolos presentan varios comportamientos. Por ejemplo, el protocolo SPX está orientado a mensajes (es decir, la red conserva los límites del mensaje del remitente), pero el socket receptor puede omitir estos límites de mensaje y tratarlos como una secuencia de bytes. Por lo tanto, podrían existir dos entradas de estructura INFO de **WSAPROTOCOL \_** diferentes para SPX, una para cada comportamiento.

En Windows Sockets 2, aparecen varios valores nuevos de familia de direcciones, tipo de socket y protocolo. Windows Sockets 1.1 admite una familia de direcciones únicas (AF INET) para IPv4 que constaba de un pequeño número de tipos de socket conocidos e identificadores \_ de protocolo. Windows Sockets 2 conserva la familia de direcciones, el tipo de socket y los identificadores de protocolo existentes por motivos de compatibilidad, pero también admite nuevos valores de familia de direcciones para nuevos protocolos de transporte con nuevos tipos de medios.

Los identificadores nuevos y únicos no son necesariamente conocidos, pero esto no debería suponer un problema. Se recomienda que las aplicaciones que necesitan ser independientes del protocolo seleccionen un protocolo en función de su idoneidad, en lugar de los valores asignados a su tipo de *socket \_* o parámetros *de* protocolo. La idoneidad del protocolo se indica mediante los atributos de comunicaciones, como el flujo de mensajes frente a bytes, y de confianza frente a no confiable, que se encuentran en la estructura info de [**WSAPROTOCOL \_ del protocolo.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) La selección de protocolos en función de la idoneidad en lugar de nombres de protocolo y tipos de socket conocidos permite que las aplicaciones independientes del protocolo aprovechen los nuevos protocolos de transporte y sus tipos de medios asociados, a medida que estén disponibles.

La mitad del servidor de una aplicación cliente/servidor se beneficia al establecer sockets de escucha en todos los protocolos de transporte adecuados. A continuación, el cliente puede establecer su conexión mediante cualquier protocolo adecuado. Por ejemplo, esto permitiría que una aplicación cliente no se modificara si se ejecutaba en un sistema de escritorio conectado a través de LAN o en un portátil mediante una red inalámbrica.

 

 
