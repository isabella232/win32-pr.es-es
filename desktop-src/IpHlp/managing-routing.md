---
description: La aplicación auxiliar de IP proporciona características para administrar el enrutamiento de red. Utilice las siguientes funciones para administrar la tabla de enrutamiento IP y obtener otra información de enrutamiento.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Administrar el enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907884"
---
# <a name="managing-routing"></a>Administrar el enrutamiento

La aplicación auxiliar de IP proporciona características para administrar el enrutamiento de red. Utilice las siguientes funciones para administrar la tabla de enrutamiento IP y obtener otra información de enrutamiento.

Recupere el contenido de la tabla de enrutamiento IP realizando una llamada a la función [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) . Manipular entradas específicas en la tabla de enrutamiento IP mediante las funciones [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)y [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) . Utilice la función **CreateIpForwardEntry** para agregar una nueva entrada de la tabla de enrutamiento. Use la función **DeleteIpForwardEntry** para quitar una entrada existente. La función **SetIpForwardEntry** modifica una entrada existente.

Las capacidades de administración del enrutador de la aplicación auxiliar IP se pueden usar para recuperar información acerca de cómo se enrutan los datagramas a través de la red. La función [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la mejor ruta a una dirección de destino especificada. La función [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera el índice de la interfaz utilizada por la mejor ruta a una dirección de destino especificada. Por último, la función [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera el tiempo de ida y vuelta (RTT) y el número de saltos a una dirección de destino especificada.

 

 



