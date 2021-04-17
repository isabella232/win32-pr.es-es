---
description: Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se utiliza para inspeccionar el tráfico de red.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Descarga de los filtros Netmon y DPWS de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696912"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Descarga de los filtros Netmon y DPWS de ejemplo

Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se utiliza para inspeccionar el tráfico de red. Se debe descargar Netmon antes de seguir los pasos de solución de problemas que se indican en [inspeccionar seguimientos de red para UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e [inspeccionar los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md) . Una vez descargado Netmon, se pueden usar filtros de DPWS para ayudar a aislar el tráfico de interés.

## <a name="downloading-netmon"></a>Descarga de Netmon

Para descargar Netmon, vaya a [monitor de red de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) y siga las instrucciones. Para obtener más información acerca de Netmon, vea "información acerca de Monitor de red 3,0" en la Knowledge base de ayuda y soporte técnico en [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Filtros de DPWS de ejemplo

En ocasiones, la solución de problemas de WS-Discovery y de intercambio de metadatos debe realizarse en una red ocupada. Los filtros de ejemplo se pueden usar para limitar el resultado de Netmon al tráfico de interés. Para obtener más información acerca del uso de filtros de Netmon, vea [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

En el ejemplo siguiente se muestra un filtro que limita la salida a todo el tráfico de WS-Discovery de difusión.

> [!Note]  
> Este filtro no captura el tráfico de pilas que no responden a los mensajes de multidifusión WS-Discovery que se originan en el puerto 3702. Si se utiliza una pila de este tipo, se debe modificar este filtro de ejemplo antes de utilizarlo.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

En el ejemplo siguiente se muestra un filtro que limita la salida a los mensajes HTTP enviados a las pilas de WSDAPI en el puerto predeterminado.

> [!Note]  
> Los servicios pueden enviar mensajes HTTP relevantes de puertos distintos de 5357. Si el tráfico procedente de otros puertos es de interés, este filtro de ejemplo debe modificarse antes de usarse.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de multidifusión IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de multidifusión IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Algunos filtros se pueden combinar para limitar aún más los resultados. En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de WS-Discovery de multidifusión IPv4.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Cuando se usan estos filtros, se puede excluir el tráfico relevante de los resultados de Netmon. La exclusión puede producirse cuando los servicios residen en puertos distintos de los puertos predeterminados (5357/5358) y cuando una pila DPWS no responde a los mensajes mediante el puerto predeterminado. En estos casos, los filtros deben modificarse antes de usarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



