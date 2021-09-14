---
description: Calcular la sobrecarga con Netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcular la sobrecarga con Netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070470"
---
# <a name="calculating-overhead-with-netstat"></a>Calcular la sobrecarga con Netstat

El cálculo de la sobrecarga con Netstat debe realizarse en una red silenciosa para evitar que otro tráfico de red sesga los datos, como el tráfico de difusión o multidifusión.

**Para calcular la sobrecarga de red de una aplicación mediante Netstat**

1.  Recupere las estadísticas de interfaz actuales mediante Netstat.
2.  Ejecute la aplicación.
3.  Obtenga las estadísticas de la interfaz, de nuevo mediante Netstat.
4.  Calcule el número de bytes recibidos entre las dos medidas de Netstat.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestran estos pasos, mediante TTCP para enviar 10 bytes de datos, un byte a la vez.

En primer lugar, se calcula una sobrecarga teórica para la aplicación. Para esta prueba, todos los paquetes tienen 60 bytes (el mínimo ethernet). Esta transferencia requiere tres paquetes para configurar la conexión, 10 paquetes de datos, 10 paquetes de confirmación (la confirmación retrasada se desencadena casi cada vez) y cuatro paquetes para cerrar la conexión correctamente.

Esto equivale a 27 paquetes de 60 bytes cada uno, o 1620 bytes (3+4+10+10) \* 60=1620). Puesto que solo se transfieren 10 bytes de datos, la sobrecarga es de 1610 bytes, lo que supera el 99 % de la sobrecarga del protocolo.

### <a name="commands"></a>Comandos:

**netstat -e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat -e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>Cálculos

**Enviado:** 816 bytes

**Recibido:** 674 bytes

**Bytes totales:** 1490

**Bytes de usuario:** 10

**Sobrecarga:** 1480/1490 = 99,3 %

**Goodput: **= 5 bytes/segundo (o 40 bits/s)

> [!Note]  
> Los bytes reales transferidos no coinciden con los valores teóricos debido a que los bytes de relleno no se tienen en cuenta en los valores de Netstat.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



