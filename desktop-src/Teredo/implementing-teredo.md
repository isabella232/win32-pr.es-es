---
title: Implementación de Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Más información sobre: Implementación de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073395"
---
# <a name="implementing-teredo"></a>Implementación de Teredo

Aunque no es necesario realizar cambios de programación para [Teredo,](about-teredo.md)se recomienda que los desarrolladores realicen cambios menores que den como resultado el uso más eficaz de la interfaz de Teredo:

-   Es posible que las aplicaciones que solo son capaces de tráfico IPv6 utilicen Teredo. Sin embargo, se debe tener en cuenta el procesamiento del tráfico IPv4 e IPv6 al desarrollar el protocolo de aplicación. La aplicación tendrá que enlazarse a AF \_ INET6 o AF \_ UNSPEC en las opciones de socket.
-   Las aplicaciones que son capaces de escuchar el tráfico no solicitado desde Internet son necesarias para habilitar la opción De recorrido de traducción de direcciones de red (NAT) dentro de Windows Firewall. Esto se logra mediante una llamada a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "Edge Traversal" establecida en VARIANT \_ TRUE. Windows Vista garantiza que la dirección teredo esté disponible para su uso cuando una aplicación lo requiera. Como resultado, la dirección teredo se estabiliza automáticamente cuando se usa la interfaz de Teredo. Si una aplicación desea asegurarse de que la dirección de Teredo es estable, al llamar a la API [**NotifyStableUnicastIpAddressTable,**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) Teredo se desencadena para realizar la transición a un estado estable.
-   Las aplicaciones también pueden usar la opción de socket Winsock [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) para establecer el nivel de protección, lo que permite que el tráfico entrante no solicitado pase a través del firewall. Consulte [Recepción de tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md) para obtener más información.

La implementación del asistente de protocolos de Internet (asistente de IP) de funciones específicas de Teredo sirve como ejemplo de cómo se puede comprobar y hacer que la dirección de Teredo esté disponible para una aplicación. Para obtener más información, [vea Uso de Teredo con el asistente de IP.](using-teredo-with-ip-helper.md)

 

 
