---
description: Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se usa para inspeccionar el tráfico de red.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Descarga de netmon y filtros DPWS de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966987"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Descarga de netmon y filtros DPWS de ejemplo

Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se usa para inspeccionar el tráfico de red. Netmon se debe descargar antes de seguir los pasos de solución de problemas indicados en Inspección de seguimientos de red para la detección de [WS](inspecting-network-traces-for-udp-ws-discovery.md) udp e inspección de [seguimientos](inspecting-network-traces-for-http-metadata-exchange.md) de red para la Exchange http. Una vez descargado Netmon, se pueden usar filtros DPWS para ayudar a aislar el tráfico de interés.

## <a name="downloading-netmon"></a>Descarga de Netmon

Para descargar Netmon, vaya [a Monitor de red de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) y siga las instrucciones. Para obtener más información sobre Netmon, vea "Información sobre Monitor de red 3.0" en la página ayuda y soporte técnico Knowledge Base en [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Filtros DPWS de ejemplo

A veces, WS-Discovery solución de problemas de intercambio de metadatos y de metadatos en una red ocupada. Los filtros de ejemplo se pueden usar para ayudar a limitar la salida de Netmon al tráfico de interés. Para obtener más información sobre el uso de filtros de Netmon, vea [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

En el ejemplo siguiente se muestra un filtro que limita la salida a todo el tráfico WS-Discovery difusión.

> [!Note]  
> Este filtro no captura el tráfico de las pilas que no responden a mensajes de WS-Discovery multidifusión que se originan en el puerto 3702. Si se usa este tipo de pila, este filtro de ejemplo debe modificarse antes de su uso.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

En el ejemplo siguiente se muestra un filtro que limita la salida a los mensajes HTTP enviados a las pilas de WSDAPI en el puerto predeterminado.

> [!Note]  
> Los servicios pueden enviar mensajes HTTP pertinentes desde puertos distintos de 5357. Si el tráfico de otros puertos es de interés, este filtro de ejemplo debe modificarse antes de su uso.

 

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

Algunos filtros se pueden combinar para limitar aún más los resultados. En el ejemplo siguiente se muestra un filtro que limita la salida a la multidifusión IPv4 WS-Discovery tráfico.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Cuando se usan estos filtros, se puede excluir el tráfico pertinente de los resultados de Netmon. La exclusión puede producirse cuando los servicios residen en puertos distintos de los puertos predeterminados (5357/5358) y cuando una pila de DPWS no responde a los mensajes mediante el puerto predeterminado. En estos casos, los filtros deben modificarse antes de su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



