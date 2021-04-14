---
description: Windows Sockets 2 no supone que el orden de bytes de la red para todos los protocolos es el mismo.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rutinas de conversión extendida Byte-Order
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541603"
---
# <a name="extended-byte-order-conversion-routines"></a>Rutinas de conversión extendida Byte-Order

Windows Sockets 2 no supone que el orden de bytes de la red para todos los protocolos es el mismo. Se proporciona un conjunto de rutinas de conversión para convertir cantidades de 16 y 32 bits a y desde el orden de bytes de la red. Estas rutinas toman como parámetro de entrada el identificador de socket que tiene una estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) asociada. El miembro **NetworkByteOrder** de la estructura de **\_ información de WSAPROTOCOL** especifica el orden de bytes de red deseado (actualmente big-endian o Little-endian).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**información de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
