---
description: Windows Sockets 2 proporciona un método genérico para usar las funcionalidades multipunto y multidifusión de transportes.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multipunto y multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238949f017c2ecb910b533d12a809aa1c04af02e64d08aa0ef4e8d4f3d39b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857914"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent multipunto y multipunto

Windows Sockets 2 proporciona un método genérico para usar las funcionalidades multipunto y multidifusión de transportes. Este método genérico implementa estas características del mismo modo que permite acceder a las funcionalidades básicas de transporte de datos de numerosos protocolos de transporte. El término multipunto se usa a partir de ahora para hacer referencia a las comunicaciones de multipunto y multipunto.

Las implementaciones actuales de varios puntos (por ejemplo, multidifusión IP, ST-II, T.120 y ATM UNI) varían considerablemente. La forma en que los nodos unen una sesión de varios puntos, si un nodo determinado se designa como nodo central o raíz, y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y los distintos nodos hoja difieren entre las implementaciones. La estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para Windows Sockets 2 se usa para declarar los distintos atributos multipunto de un protocolo. Al examinar estos atributos, el programador sabe qué convenciones se deben seguir con las funciones de sockets de Windows 2 aplicables para configurar, usar y desusar sesiones de varios puntos.

A continuación se resumen las características de Winsock que admiten multipunto:

-   Bits de dos atributos en la [**estructura INFO de WSAPROTOCOL. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Cuatro marcas definidas para el *parámetro dwFlags* de la [**función WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
-   Una función, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)para agregar nodos hoja a una sesión de varios puntos
-   Dos [**códigos de comando WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle de retorno de varios puntos y establecer el ámbito de las transmisiones de multidifusión. (Este último corresponde al parámetro TTL o período de vida de multidifusión IP).

> [!Note]  
> La inclusión de estas características multipunto en Windows Sockets 2 no impide que una aplicación use una interfaz dependiente del protocolo existente, como las opciones de socket de deering para la multidifusión IP.

 

Consulte [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) (Semántica de multipunto y multidifusión) para obtener información detallada sobre cómo se caracterizan los distintos esquemas de multipunto y cómo se usan las características aplicables de Windows Sockets 2.

 

 
