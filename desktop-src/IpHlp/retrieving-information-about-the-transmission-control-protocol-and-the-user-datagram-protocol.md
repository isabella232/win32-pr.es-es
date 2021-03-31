---
description: La aplicación auxiliar IP permite obtener acceso a información acerca de los protocolos de red que se usan en el equipo local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperación de información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819483"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recuperación de información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario

La aplicación auxiliar IP permite obtener acceso a información acerca de los protocolos de red que se usan en el equipo local. Use las funciones descritas en los párrafos siguientes para recuperar información sobre el protocolo de control de transmisión (TCP) y el protocolo de datagramas de usuario (UDP) en el equipo local.

La función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera las estadísticas actuales para TCP. Para obtener ejemplos de código que impliquen a **GetTcpStatistics** , vea [recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

La función [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera las estadísticas actuales para UDP.

La función [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabla de conexiones TCP. [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera la tabla de escucha de UDP.

La función [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permite a un desarrollador establecer el estado de una conexión TCP especificada en MIB \_ TCP \_ \_ Delete \_ TCB.

 

 



