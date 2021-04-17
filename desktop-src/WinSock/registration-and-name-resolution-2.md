---
description: Windows Sockets 2 es un conjunto de funciones que estandariza el modo en que las aplicaciones tienen acceso a los diversos servicios de nombres de red y los usan.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registro y resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706109"
---
# <a name="registration-and-name-resolution"></a>Registro y resolución de nombres

Windows Sockets 2 es un conjunto de funciones que estandariza el modo en que las aplicaciones tienen acceso a los diversos servicios de nombres de red y los usan. Cuando se usan estas funciones, las aplicaciones no necesitan distinguir los protocolos que difieren ampliamente de los asociados a los servicios de nombres como DNS, NIS, X. 500, SAP, etc. Para mantener la compatibilidad completa con versiones anteriores de Windows Sockets 1,1, las funciones de búsqueda de base de datos **getXbyY** y asincrónica **WSAAsyncGetXbyY** se siguen admitiendo, pero se implementan en la interfaz del proveedor de servicios de Windows Sockets en cuanto a las nuevas capacidades de resolución de nombres. Para obtener más información, vea las funciones [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) y [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) . Además, consulte [resolución de nombres compatible para TCP/IP en Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

En esta sección se describen las capacidades de registro y resolución de nombres disponibles para los desarrolladores de Winsock. En la lista siguiente se describen los temas de esta sección:

-   [Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
-   [Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Winsock](about-winsock.md)
</dt> <dt>

[Usar WinSock](using-winsock.md)
</dt> </dl>

 

 



