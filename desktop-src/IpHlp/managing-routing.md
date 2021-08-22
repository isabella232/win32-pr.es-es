---
description: El asistente de IP proporciona características para administrar el enrutamiento de red. Use las siguientes funciones para administrar la tabla de enrutamiento IP y para obtener otra información de enrutamiento.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Administrar el enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3b351882e08be3d09615acd033e0fb86192aee8675e8f52c4812a1eba398ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146648"
---
# <a name="managing-routing"></a>Administrar el enrutamiento

El asistente de IP proporciona características para administrar el enrutamiento de red. Use las siguientes funciones para administrar la tabla de enrutamiento IP y para obtener otra información de enrutamiento.

Recupere el contenido de la tabla de enrutamiento IP mediante una llamada a la [**función GetIpForwardTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) Manipule entradas específicas de la tabla de enrutamiento IP mediante las funciones [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)y [**SetIpForwardEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) Use la **función CreateIpForwardEntry para** agregar una nueva entrada de tabla de enrutamiento. Use la **función DeleteIpForwardEntry** para quitar una entrada existente. La **función SetIpForwardEntry** modifica una entrada existente.

Las funcionalidades de administración de enrutadores del asistente de IP se pueden usar para recuperar información sobre cómo se enrutar los datagramas a través de la red. La [**función GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la mejor ruta a una dirección de destino especificada. La [**función GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera el índice de la interfaz utilizada por la mejor ruta a una dirección de destino especificada. Por último, la función [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera el tiempo de ida y vuelta (RTT) y el número de saltos a una dirección de destino especificada.

 

 



