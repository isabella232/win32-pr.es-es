---
description: El asistente de IP proporciona funcionalidades de recuperación de información que son útiles para la administración de red del equipo local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recuperar información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160065"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Recuperar información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet

El asistente de IP proporciona funcionalidades de recuperación de información que son útiles para la administración de red del equipo local. Las siguientes funciones recuperan estadísticas para el Protocolo de Internet (IP) y el Protocolo de mensajes de control de Internet (ICMP). También puede usar estas funciones para establecer determinados parámetros de configuración para IP.

La [**función GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera las estadísticas ip actuales del equipo local. Para obtener ejemplos de código **relacionados con GetIpStatistics,** vea [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).

La [**función GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera las estadísticas ICMP actuales.

Use la [**función SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) para habilitar o deshabilitar el reenvío IP. Esta función también permite establecer el período de vida predeterminado (TTL) para datagramas IP. Como alternativa, puede establecer el TTL mediante la [**función SetIpTTL.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl)

 

 



