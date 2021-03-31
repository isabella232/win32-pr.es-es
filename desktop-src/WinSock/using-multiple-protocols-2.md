---
description: Una aplicación utiliza la función WSAEnumProtocols para determinar qué protocolos de transporte y cadenas de protocolo están presentes, y para obtener información sobre cada uno de los contenidos en la estructura de información de WSAPROTOCOL asociada \_ .
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Usar varios protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154243"
---
# <a name="using-multiple-protocols"></a>Usar varios protocolos

Una aplicación utiliza la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para determinar qué protocolos de transporte y cadenas de protocolo están presentes, y para obtener información sobre cada uno de los contenidos en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) asociada.

En la mayoría de los casos, hay una única estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada cadena de protocolo o protocolo. Sin embargo, algunos protocolos muestran varios comportamientos. Por ejemplo, el protocolo SPX está orientado a mensajes (es decir, la red conserva los límites de los mensajes del remitente), pero el socket receptor puede omitir estos límites de mensajes y tratarlos como un flujo de bytes. Por lo tanto, pueden existir dos entradas diferentes de la estructura de **\_ información de WSAPROTOCOL** para SPX, una para cada comportamiento.

En Windows Sockets 2, aparecen varios valores nuevos de familia de direcciones, tipo de socket y protocolo. Windows Sockets 1,1 admitía una sola familia de direcciones (AF \_ inet) para IPv4 que constaba de un pequeño número de tipos de socket conocidos e identificadores de protocolo. Windows Sockets 2 conserva los identificadores existentes de la familia de direcciones, el tipo de socket y el Protocolo por motivos de compatibilidad, pero también admite nuevos valores de la familia de direcciones para los nuevos protocolos de transporte con nuevos tipos de medios.

Los nuevos identificadores únicos no son necesariamente conocidos, pero esto no debería suponer un problema. Se recomienda que las aplicaciones que necesitan ser independientes del protocolo seleccionen un protocolo en función de su idoneidad en lugar de los valores asignados a sus parámetros de *Protocolo* o *\_ tipo de socket* . La idoneidad del Protocolo se indica mediante los atributos de comunicaciones, como la secuencia de mensajes frente a bytes, y la confianza frente a la no confiable, que se encuentran en la estructura de [**\_ información**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) del protocolo WSAPROTOCOL. La selección de protocolos en función de la idoneidad en lugar de los nombres de protocolo conocidos y los tipos de socket permite a las aplicaciones independientes del protocolo aprovechar los nuevos protocolos de transporte y sus tipos de medios asociados, a medida que estén disponibles.

La mitad del servidor de una aplicación cliente/servidor se beneficia al establecer sockets de escucha en todos los protocolos de transporte adecuados. A continuación, el cliente puede establecer su conexión con cualquier protocolo adecuado. Por ejemplo, esto permite que una aplicación cliente no se modifique si se estaba ejecutando en un sistema de escritorio conectado a través de LAN o en un equipo portátil con una red inalámbrica.

 

 
