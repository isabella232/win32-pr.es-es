---
description: Calcular la sobrecarga con netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcular la sobrecarga con netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705657"
---
# <a name="calculating-overhead-with-netstat"></a>Calcular la sobrecarga con netstat

El cálculo de la sobrecarga con netstat debe realizarse en una red silenciosa para evitar que el tráfico de red sesgado de los datos, como el tráfico de difusión o multidifusión.

**Para calcular la sobrecarga de red de una aplicación mediante netstat**

1.  Recupere las estadísticas de la interfaz actual mediante netstat.
2.  Ejecute la aplicación.
3.  Obtenga las estadísticas de la interfaz, de nuevo mediante netstat.
4.  Calcule el número de bytes recibidos entre las dos medidas de netstat.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestran estos pasos, con TTCP para enviar 10 bytes de datos, un byte a la vez.

En primer lugar, se calcula una sobrecarga teórica para la aplicación. Para esta prueba, todos los paquetes tienen 60 bytes (el mínimo de Ethernet). Esta transferencia requiere tres paquetes para configurar la conexión, 10 paquetes de datos, 10 paquetes de confirmación (la confirmación diferida se desencadena casi cada vez) y cuatro paquetes para cerrar la conexión correctamente.

Esto equivale a 27 paquetes de 60 bytes cada uno o 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620). Dado que solo se transfieren 10 bytes de datos, la sobrecarga es de 1610 bytes, que es superior al 99% de sobrecarga del protocolo.

### <a name="commands"></a>Comandos:

**netstat-e**

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

**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

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

**Total de bytes:** 1490

**Bytes de usuario:** 10

**Sobrecarga:** 1480/1490 = 99,3%

* * Goodput: * * = 5 bytes/segundo (o 40 bits/s)

> [!Note]  
> Los bytes reales transferidos no coinciden con los valores teóricos debido a que no se tienen en cuenta los bytes de relleno en los valores de netstat.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



