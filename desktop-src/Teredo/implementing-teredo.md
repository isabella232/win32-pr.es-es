---
title: Implementación de Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: Más información acerca de cómo implementar Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279132"
---
# <a name="implementing-teredo"></a>Implementación de Teredo

Aunque no es necesario realizar cambios de programación para [Teredo](about-teredo.md), se recomienda que los desarrolladores realicen cambios menores que dan como resultado el uso más eficaz de la interfaz Teredo:

-   Es posible que las aplicaciones que solo tienen el tráfico IPv6 puedan utilizar Teredo. Sin embargo, se debe tener en cuenta el procesamiento del tráfico IPv4 e IPv6 al desarrollar el protocolo de aplicación. La aplicación necesitará enlazar a \_ las opciones AF inet6 o AF \_ unspec in socket.
-   Las aplicaciones que son capaces de realizar escuchas de tráfico no solicitado desde Internet son necesarias para habilitar la opción de recorrido de traducción de direcciones de red (NAT) dentro de Firewall de Windows. Esto se logra mediante una llamada a la API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con la opción "cruce seguro del perímetro" establecida en Variant \_ true. Windows Vista garantiza que la dirección Teredo esté disponible para su uso cuando una aplicación lo requiera. Como resultado, la dirección Teredo se estabiliza automáticamente cuando se usa la interfaz Teredo. Si una aplicación desea asegurarse de que la dirección Teredo es estable, llamar a la API de [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) desencadena Teredo para que pase a un estado estable.
-   Las aplicaciones también pueden usar la opción de socket Winsock de [ \_ \_ nivel de protección IPv6](/windows/desktop/WinSock/ipv6-protection-level) para establecer el nivel de protección, lo que permite que el tráfico entrante no solicitado pase a través del firewall. Vea [recibir tráfico no solicitado a través de Teredo](receiving-unsolicited-traffic-over-teredo.md) para obtener más información.

La implementación de la aplicación auxiliar de protocolo de Internet (auxiliar IP) de funciones de Teredo específicas sirve como ejemplo de cómo se puede comprobar la dirección Teredo y ponerla a disposición de una aplicación. Para obtener más información, vea [usar Teredo con la aplicación auxiliar de IP](using-teredo-with-ip-helper.md).

 

 
