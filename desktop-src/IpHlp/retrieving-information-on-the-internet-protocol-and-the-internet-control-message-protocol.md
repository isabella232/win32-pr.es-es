---
description: La aplicación auxiliar de IP proporciona funciones de recuperación de información que son útiles para la administración de red del equipo local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recuperación de información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000895"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Recuperación de información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet

La aplicación auxiliar de IP proporciona funciones de recuperación de información que son útiles para la administración de red del equipo local. Las siguientes funciones recuperan estadísticas del Protocolo de Internet (IP) y del Protocolo de mensajes de control de Internet (ICMP). También puede usar estas funciones para establecer determinados parámetros de configuración de IP.

La función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera las estadísticas de IP actuales para el equipo local. Para obtener ejemplos de código que impliquen a **GetIpStatistics** , vea [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md).

La función [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera las estadísticas de ICMP actuales.

Use la función [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) para habilitar o deshabilitar el reenvío IP. Esta función también permite establecer el período de vida (TTL) predeterminado para los datagramas IP. Como alternativa, puede establecer el TTL mediante la función [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .

 

 



