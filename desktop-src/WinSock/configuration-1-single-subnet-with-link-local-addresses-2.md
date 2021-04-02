---
description: La primera configuración no requiere ninguna configuración adicional más allá de la instalación del protocolo Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuración 1: subred única con direcciones locales de vínculo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082124"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Configuración 1: subred única con direcciones locales de vínculo

La primera configuración no requiere ninguna configuración adicional más allá de la instalación del protocolo Microsoft IPv6 Technology Preview. Esta configuración consta de al menos dos nodos en la misma subred. En la terminología de IPv6, los dos nodos están en el mismo vínculo sin enrutadores intermedios.

En la ilustración siguiente se muestra la configuración de dos nodos en una sola subred mediante direcciones locales de vínculo.

![dos nodos que usan direcciones locales de vínculo.](images/v6mig-1.png)

De forma predeterminada, IPv6 configura las direcciones IP locales de vínculo para cada interfaz correspondiente a los adaptadores de red Ethernet instalados. Las direcciones locales de vínculo tienen el prefijo fe80::/64. Los últimos 64 bits de la dirección IPv6 se conocen como el identificador de interfaz y se derivan de la dirección MAC de 48 bits del adaptador de red.

Para crear el identificador de interfaz IPv6 a partir de la dirección MAC Ethernet de 48 bits (6 bytes):

-   Los dígitos hexadecimales 0xFF-fe se insertan entre el tercer y el cuarto byte de la dirección MAC.
-   Se complementa el bit universal/local, el segundo bit de orden inferior del primer byte de la dirección MAC. Si es 1, se convierte en 0 y si es un 0, se convierte en 1.

Por ejemplo, para la dirección MAC 00-60-08-52-F9-D8:

-   Los dígitos hexadecimales 0xFF-fe se insertan entre 0x08 (el tercer byte) y 0x52 (el cuarto byte) de la dirección MAC, formando la dirección de 64 bits 00-60-08-FF-fe-52-F9-D8.
-   El bit universal/local, el segundo bit de orden inferior de 0x00 (el primer byte) de la dirección MAC se complementa. El segundo bit de orden inferior de 0x00 es 0, que, cuando se complementa, se convierte en 1. El resultado es que para el primer byte, 0x00 se convierte en 0x02.

Por lo tanto, el identificador de la interfaz IPv6 correspondiente a la dirección MAC Ethernet de 00-60-08-52-F9-D8 es 02-60-08-FF-fe-52-F9-D8.

La dirección local del vínculo de un nodo es la combinación del prefijo fe80::/64 y el identificador de la interfaz de 64 bits expresado en la notación hexadecimal con dos puntos de IPv6. Por lo tanto, la dirección local del vínculo de este nodo de ejemplo con el prefijo fe80::/64 y el identificador de interfaz 02-60-08-FF-fe-52-F9-D8 es fe80:: 260:8ff: Fe52: F9D8.

Puede ver la dirección local del vínculo mediante IPv6 si, tal y como se muestra en el ejemplo siguiente:

**IPv6 si**

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

La interfaz 4 es una interfaz que corresponde a un adaptador Ethernet instalado con una dirección local de vínculo de fe80:: 210:5AfF: feaa: 20a2.

Para obtener más información sobre el direccionamiento IPv6 y una introducción a los conceptos de IPv6, consulte las notas del producto Introducción a IPv6.

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Probar la conectividad entre dos hosts locales de vínculo

Puede realizar un ping sencillo (un intercambio de mensajes de solicitud de eco ICMPv6 y de respuesta de eco) mediante IPv6 entre dos hosts locales de vínculo.

**Para hacer ping mediante IPv6 entre dos hosts locales de vínculo**

1.  Instale Microsoft IPv6 Technology Preview para Windows en dos hosts de Windows (el host A y el host B) que se encuentran en el mismo vínculo (subred).
2.  Use IPv6 si en el host a para obtener la dirección local del vínculo para la interfaz Ethernet.

    Ejemplo: la dirección local del vínculo del host A es fe80:: 210:5AfF: feaa: 20a2.

3.  Use IPv6 si en el host B para obtener la dirección local del vínculo para la interfaz Ethernet.

    Ejemplo: la dirección local del vínculo del host B es fe80:: 260:97ff: fe02:6ea5.

4.  Desde el host A, haga ping al host B mediante Ping6.exe.

    Ejemplo: ping6 fe80:: 260:97ff: fe02:6ea5

Para especificar la dirección de origen desde la que se envían los mensajes de solicitud de eco, también puede usar la opción Ping6.exe-s. Por ejemplo, para enviar solicitudes de eco al host B desde la dirección IPv6 de fe80:: 210:5AfF: feaa: 20a2, use el siguiente comando:

**ping6-s fe80:: 210:5AfF: feaa: 20a2% 4 fe80:: 260:97ff: fe02:6ea5**

Al hacer ping a una dirección local de vínculo o local de sitio, se recomienda especificar el identificador de ámbito para que la dirección de destino no sea ambigua. La notación para especificar el identificador de ámbito es dirección% de identificador de ámbito. En el caso de las direcciones locales de vínculo, el identificador de ámbito es igual al número de interfaz, tal y como se muestra en el comando IPv6 if. En el caso de las direcciones locales del sitio, el identificador de ámbito es igual al número de sitio que se muestra en el comando IPv6 if. Por ejemplo, para enviar mensajes de solicitud de eco al host B mediante el identificador de ámbito 4, use el siguiente comando:

**ping6 fe80:: 260:97ff: fe02:6ea5% 4**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones recomendadas para IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



