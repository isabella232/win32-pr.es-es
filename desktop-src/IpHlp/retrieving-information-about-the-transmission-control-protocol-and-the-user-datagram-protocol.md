---
description: El asistente de IP permite acceder a información sobre los protocolos de red que se usan en el equipo local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperar información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f10691c39e1f1a2c9c92af8736549427f01cc2400773e214f3a4d5f536fa46e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102055"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Recuperar información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario

El asistente de IP permite acceder a información sobre los protocolos de red que se usan en el equipo local. Use las funciones descritas en los párrafos siguientes para recuperar información sobre el Protocolo de control de transmisión (TCP) y el Protocolo de datagramas de usuario (UDP) en el equipo local.

La [**función GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera las estadísticas actuales de TCP. Para obtener ejemplos de código **que implican GetTcpStatistics,** vea [Recuperación de información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

La [**función GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera las estadísticas actuales de UDP.

La [**función GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabla de conexión TCP. [**GetUdpTable recupera la**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) tabla de escucha UDP.

La [**función SetTcpEntry permite**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) a un desarrollador establecer el estado de una conexión TCP especificada en MIB TCP STATE DELETE \_ \_ \_ \_ TCB.

 

 



