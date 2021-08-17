---
description: Proveedores de servicios de transporte Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Proveedores de servicios de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860db59b5a27d19cdc5263069161f105d79e15cfd7353789f8fdcf9944799ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927185"
---
# <a name="transport-service-providers"></a>Proveedores de servicios de transporte

Un proveedor de servicios de transporte determinado admite uno o varios protocolos. Por ejemplo, un proveedor TCP/IP proporcionaría, como mínimo, los protocolos TCP y UDP, mientras que un proveedor IPX/SPX podría proporcionar IPX, SPX y SPX II. Cada protocolo admitido por un proveedor determinado se describe mediante una estructura INFO de [**WSAPROTOCOL, \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) y el conjunto total de estas estructuras se puede pensar en como el catálogo de protocolos instalados. Las aplicaciones pueden recuperar el contenido de este catálogo (para obtener más información, vea [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)y [**WSCEnumProtocols32),**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)y examinando las estructuras info de **\_ WSAPROTOCOL** disponibles, descubra los atributos de comunicación asociados a cada protocolo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolos por capas y cadenas de protocolo en el SPI

Windows Sockets 2 admite el concepto de protocolo por capas. Un protocolo por capas es aquel que implementa solo funciones de comunicaciones de nivel superior, al tiempo que se basa en una pila de transporte subyacente para el intercambio real de datos con un punto de conexión remoto. Un ejemplo de este tipo de protocolo en capas sería una capa de seguridad que agrega el protocolo al proceso de establecimiento de la conexión con el fin de realizar la autenticación y establecer un esquema de cifrado mutuamente acordado. Por lo general, este tipo de protocolo de seguridad requeriría los servicios de un protocolo de transporte confiable subyacente, como TCP o SPX. El término protocolo base hace referencia a un protocolo como TCP o SPX que es totalmente capaz de realizar comunicaciones de datos con un punto de conexión remoto y el término protocolo por capas se usa para describir un protocolo que no puede ser independiente. A continuación, una cadena de protocolos se definiría como uno o varios protocolos en capas juntos y delimitados por un protocolo base.

Este encadenamiento de protocolos en capas y protocolos base en cadenas se puede lograr mediante la organización de los protocolos por capas para admitir el SPI de Winsock en sus bordes superior e inferior. Se crea una estructura info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial que hace referencia a la cadena de protocolos como un todo y que describe el orden explícito en el que se unen los protocolos por capas. Esto se muestra en el gráfico siguiente.

![cadena de protocolos](images/ovrvw2-3.png)

 

 
