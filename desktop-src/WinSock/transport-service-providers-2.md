---
description: Proveedores de servicios de transporte y Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Proveedores de servicios de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696370"
---
# <a name="transport-service-providers"></a>Proveedores de servicios de transporte

Un proveedor de servicios de transporte determinado admite uno o más protocolos. Por ejemplo, un proveedor TCP/IP proporcionaría, como mínimo, los protocolos TCP y UDP, mientras que un proveedor IPX/SPX podría proporcionar IPX, SPX y SPX II. Cada protocolo admitido por un proveedor determinado se describe mediante una estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) y el conjunto total de estas estructuras puede considerarse como el catálogo de protocolos instalados. Las aplicaciones pueden recuperar el contenido de este catálogo (para obtener más información, vea [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)) y examinar las estructuras de **\_ información WSAPROTOCOL** disponibles, detectar los atributos de comunicaciones asociados a cada protocolo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolos en capas y cadenas de protocolo en el SPI

Windows Sockets 2 incluye el concepto de protocolo superpuesto. Un protocolo en capas es aquél que implementa solo funciones de comunicaciones de nivel superior, mientras que se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto. Un ejemplo de este tipo de protocolo en capas sería un nivel de seguridad que agrega el protocolo al proceso de establecimiento de la conexión para realizar la autenticación y establecer un esquema de cifrado acordado mutuamente. Por lo general, este protocolo de seguridad requeriría los servicios de un protocolo de transporte confiable subyacente, como TCP o SPX. El término protocolo base hace referencia a un protocolo como TCP o SPX que es totalmente capaz de realizar comunicaciones de datos con un punto de conexión remoto, y el término protocolo en capas se usa para describir un protocolo que no puede ser independiente. A continuación, una cadena de protocolos se definiría como uno o varios protocolos superpuestos agrupados juntos y delimitados por un protocolo base.

Esta cadena de protocolos en capas y protocolos base en cadenas puede realizarse mediante la organización de los protocolos en capas para admitir el SPI de Winsock en los bordes superior e inferior. Se crea una estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial que hace referencia a la cadena de protocolos en conjunto y que describe el orden explícito en el que se unen los protocolos en capas. Esto se muestra en el gráfico siguiente.

![cadena de protocolos](images/ovrvw2-3.png)

 

 
