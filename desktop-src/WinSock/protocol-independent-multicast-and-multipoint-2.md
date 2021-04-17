---
description: Windows Sockets 2 proporciona un método genérico para usar las capacidades multipoint y multidifusión de los transportes.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Multidifusión y Multipoint Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696811"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Multidifusión y Multipoint Protocol-Independent

Windows Sockets 2 proporciona un método genérico para usar las capacidades multipoint y multidifusión de los transportes. Este método genérico implementa estas características de la misma forma que permite el acceso a las capacidades básicas de transporte de datos de numerosos protocolos de transporte. El término, Multipoint, se usa en adelante para hacer referencia a las comunicaciones multidifusión y multipoint.

Las implementaciones de Multipoint actuales (por ejemplo, multidifusión IP, ST-II, T. 120 y ATM UNI) varían considerablemente. Cómo se unen los nodos a una sesión de Multipoint, si un nodo determinado se designa como nodo central o raíz, y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y los distintos nodos hoja difieren entre las implementaciones. La estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para Windows Sockets 2 se usa para declarar los distintos atributos multipunto de un protocolo. Mediante el examen de estos atributos, el programador sabe qué convenciones seguir con las funciones de Windows Sockets 2 aplicables para configurar, emplear y anular sesiones multipoint.

A continuación se resumen las características de Winsock que admiten Multipoint:

-   Bits de dos atributos en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Cuatro marcas definidas para el parámetro *dwFlags* de la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Una función, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para agregar nodos hoja en una sesión de Multipoint
-   Dos códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle invertido multipunto y establecer el ámbito para las transmisiones de multidifusión. (Este último se corresponde con el parámetro TTL o período de vida de multidifusión IP).

> [!Note]  
> La inclusión de estas características Multipoint en Windows Sockets 2 no impide que una aplicación use una interfaz dependiente del Protocolo existente, como las opciones de socket Deering para multidifusión IP.

 

Consulte [semántica de multidifusión y multidifusión](multipoint-and-multicast-semantics-2.md) para obtener información detallada sobre cómo se caracterizan los distintos esquemas de multipoint y cómo se usan las características aplicables de Windows Sockets 2.

 

 
