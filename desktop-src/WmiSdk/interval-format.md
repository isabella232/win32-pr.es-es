---
description: Define intervalos de fecha y hora con un formato similar a la sintaxis de fecha y hora al dividir la cadena en los campos de días, horas, minutos, segundos y microsegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30db455b6b39349b3da2f8328b22597d8b9c16c47387ba7f6b15d81e62ceb134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318541"
---
# <a name="interval-format"></a>Formato de intervalo

WMI define intervalos de fecha y hora con un formato similar a la sintaxis de fecha y hora al dividir la cadena en los campos de días, horas, minutos, segundos y microsegundos.

En el ejemplo siguiente se muestra el formato de un intervalo de fecha y hora.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

En la tabla siguiente se enumeran los campos del intervalo de fecha y hora.



| Campo    | Descripción                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | Ocho dígitos que representan un número de días (de 00000000 a 99999999).                                                                                                                                                                    |
| HH       | Hora de dos dígitos del día que usa el reloj de 24 horas (de 00 a 23).                                                                                                                                                                       |
| MM       | Minuto de dos dígitos en la hora (de 00 a 59).                                                                                                                                                                                                |
| SS       | Número de segundos de dos dígitos en el minuto (de 00 a 59).                                                                                                                                                                                   |
| Mmmmmm   | Número de microsegundos de seis dígitos en el segundo (de 000000 a 999999). La implementación no es necesaria para admitir la evaluación mediante este campo, pero este campo siempre debe estar presente para conservar la naturaleza de longitud fija de la cadena. |



 

Los intervalos siempre tienen un ":000" final como los últimos cuatro caracteres. Además, a diferencia de la fecha y hora, no puede usar asteriscos para indicar campos no utilizados. Además, todas las propiedades de tipo [ \_ CIM DATETIME](cim-datetime.md) que representan intervalos deben marcarse con el calificador [estándar SubType,](standard-wmi-qualifiers.md) con el calificador establecido en "interval".

La cadena siguiente representa un intervalo de 1 día, 12 horas, 0 minutos y 32 segundos.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de fecha y hora](date-and-time-format.md)
</dt> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[CIM \_ DATETIME](cim-datetime.md)
</dt> </dl>

 

 



