---
description: Windows Sockets 2 no supone que el orden de bytes de red para todos los protocolos es el mismo.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rutinas Byte-Order de conversión de datos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068282"
---
# <a name="extended-byte-order-conversion-routines"></a>Rutinas Byte-Order de conversión de datos extendidos

Windows Sockets 2 no supone que el orden de bytes de red para todos los protocolos es el mismo. Se proporciona un conjunto de rutinas de conversión para convertir cantidades de 16 y 32 bits en y desde el orden de bytes de red. Estas rutinas toman como parámetro de entrada el identificador de socket que tiene asociada una estructura INFO de [**WSAPROTOCOL. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) El **miembro NetworkByteOrder** de la estructura **\_ INFO de WSAPROTOCOL** especifica el orden de bytes de red deseado (actualmente big-endian o little-endian).

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

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANt adheres**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
