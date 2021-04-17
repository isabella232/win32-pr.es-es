---
description: Hay varios atributos de socket que se pueden indicar mediante el parámetro flags en WSPSocket.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Marcas y modos de atributo de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da1a5f621a7d9f489f4e91782462c215659772b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716634"
---
# <a name="socket-attribute-flags-and-modes"></a>Marcas y modos de atributo de socket

Hay varios atributos de socket que se pueden indicar mediante el parámetro *Flags* en [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). La marca de superposición de \_ marca WSA \_ indica que se usará un socket para las operaciones de e/s superpuestas. La compatibilidad de este atributo es obligatoria para todos los proveedores de servicios. Para obtener más información [, vea e/s superpuesta](overlapped-i-o-2.md) . Tenga en cuenta que la creación de un socket con el atributo OVERLAPPED no tiene ningún efecto sobre si un socket está actualmente en modo de bloqueo o de no bloqueo. Los sockets creados con el atributo OVERLAPPED se pueden usar para realizar operaciones de e/s superpuestas y, al hacerlo, no se cambia el modo de bloqueo de un socket. Dado que las operaciones de e/s superpuestas no se bloquean, el modo de bloqueo de un socket es irrelevante para estas operaciones.

Al crear sockets que se van a usar para las operaciones de Multipoint o multidifusión, se usan cuatro marcas de atributo adicionales, y la compatibilidad con estos atributos es opcional. Los proveedores que admiten atributos Multipoint indican esto a través del \_ \_ bit de Multipoint de XP1 soporte técnico en sus estructuras de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) respectivas. Consulte [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) y [multidifusión independiente del protocolo y Multipoint en la API](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) para obtener la definición y el uso de cada una de estas marcas. Solo los sockets creados con atributos relacionados con Multipoint se pueden usar en la función [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para crear sesiones multipoint.

Un socket está en uno de los dos modos: bloqueo y no bloqueo, en cualquier momento. De forma predeterminada, los sockets se crean en el modo de bloqueo y se pueden cambiar al modo de no bloqueo mediante una llamada a [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)). Un socket se puede volver al modo de bloqueo mediante **WSPIoctl** si no hay ningún **WSPAsyncSelect** o **WSPEventSelect** activo. El modo de un socket solo afecta a las funciones que se pueden bloquear y no afecta a las operaciones de e/s superpuestas. Consulte [operaciones de bloqueo](blocking-operations-2.md) para obtener más información.

 

 
