---
title: Implementación de Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Más información sobre: Implementación de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b24f4524d6c513dc0a5cd11e7f6420eb7e546fa3bce75c830759fc38faaef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681655"
---
# <a name="implementing-teredo"></a>Implementación de Teredo

Aunque no es necesario realizar cambios de programación para [Teredo,](about-teredo.md)se recomienda que los desarrolladores realicen cambios menores que resulte en el uso más eficaz de la interfaz teredo:

-   Es posible que las aplicaciones que solo son capaces de tráfico IPv6 utilicen Teredo. Sin embargo, se debe tener en cuenta el procesamiento del tráfico IPv4 e IPv6 al desarrollar el protocolo de aplicación. La aplicación tendrá que enlazarse a AF \_ INET6 o AF \_ UNSPEC en las opciones de socket.
-   Las aplicaciones que son capaces de escuchar el tráfico no solicitado desde Internet son necesarias para habilitar la opción de recorrido de traducción de direcciones de red (NAT) dentro de Windows Firewall. Para ello, llame a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "Edge Traversal" establecida en VARIANT \_ TRUE. Windows Vista garantiza que la dirección teredo esté disponible para su uso cuando una aplicación la requiera. Como resultado, la dirección Teredo se estabiliza automáticamente cuando se usa la interfaz Teredo. Si una aplicación quiere asegurarse de que la dirección de Teredo es estable, al llamar a la API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) se desencadena teredo para que se haga la transición a un estado estable.
-   Las aplicaciones también pueden usar la opción de socket [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) Winsock para establecer el nivel de protección, lo que permite que el tráfico entrante no solicitado pase a través del firewall. Consulte [Recepción de tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md) para obtener más información.

La implementación del asistente de protocolos de Internet (asistente de IP) de funciones específicas de Teredo sirve como ejemplo de cómo se puede comprobar y hacer que la dirección teredo esté disponible para una aplicación. Para obtener más información, [vea Uso de Teredo con el asistente de IP.](using-teredo-with-ip-helper.md)

 

 
