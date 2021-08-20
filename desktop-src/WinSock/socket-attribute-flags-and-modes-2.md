---
description: Hay varios atributos de socket que se pueden indicar a través del parámetro flags en WSPSocket.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Marcas y modos de atributo de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2943116c58c77d53cefa4e8d238f9c5542ea71840b31f979ffbe6eb7f1c2550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927337"
---
# <a name="socket-attribute-flags-and-modes"></a>Marcas y modos de atributo de socket

Hay varios atributos de socket que se pueden indicar a través del *parámetro flags* en [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) La marca OVERLAPPED de WSA FLAG indica que se usará un socket para \_ \_ las operaciones de E/S superpuestas. La compatibilidad con este atributo es obligatoria para todos los proveedores de servicios. Consulte [E/S superpuesta para](overlapped-i-o-2.md) obtener más información. Tenga en cuenta que la creación de un socket con el atributo superpuesto no tiene ningún impacto en si un socket está actualmente en modo de bloqueo o de no bloqueo. Los sockets creados con el atributo superpuesto se pueden usar para realizar operaciones de E/S superpuestas y, al hacerlo, no cambia el modo de bloqueo de un socket. Puesto que las operaciones de E/S superpuestas no se bloquean, el modo de bloqueo de un socket es irrelevante para estas operaciones.

Se usan cuatro marcas de atributo adicionales al crear sockets que se van a usar para operaciones multipunto o multidifusión, y la compatibilidad con estos atributos es opcional. Los proveedores que admiten atributos multipunto lo indican a través del bit XP1 SUPPPORT MULTIPOINT en sus respectivas estructuras \_ info de \_ [**WSAPROTOCOL. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Consulte Multipoint y [**multipunto WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) y [Protocol-Independent en](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) la API para ver la definición y el uso de cada una de estas marcas. Solo se pueden usar sockets creados con atributos relacionados con varios puntos en la función [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para crear sesiones de varios puntos.

Un socket está en uno de estos dos modos, bloqueo y no bloqueo, en cualquier momento. Los sockets se crean en el modo de bloqueo de forma predeterminada y se pueden cambiar al modo de no bloqueo llamando a [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)). Un socket se puede volver a cambiar al modo de bloqueo mediante **WSPIoctl** si no hay **ningún WSPAsyncSelect** o **WSPEventSelect** activo. El modo de un socket solo afecta a las funciones que pueden bloquearse y no afecta a las operaciones de E/S superpuestas. Consulte [Operaciones de bloqueo](blocking-operations-2.md) para obtener más información.

 

 
