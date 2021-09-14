---
description: Define intervalos de fecha y hora con un formato similar a la sintaxis de fecha y hora al dividir la cadena en los campos de días, horas, minutos, segundos y microsegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070467"
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
| ddddddddd | Ocho dígitos que representan un número de días (de 00000000 a 99999999).                                                                                                                                                                    |
| HH       | Hora de dos dígitos del día que usa el reloj de 24 horas (de 00 a 23).                                                                                                                                                                       |
| MM       | Minuto de dos dígitos en la hora (de 00 a 59).                                                                                                                                                                                                |
| SS       | Número de segundos de dos dígitos en el minuto (de 00 a 59).                                                                                                                                                                                   |
| Mmmmmm   | Número de seis dígitos de microsegundos en el segundo (de 000000 a 999999). La implementación no es necesaria para admitir la evaluación mediante este campo, pero este campo siempre debe estar presente para conservar la naturaleza de longitud fija de la cadena. |



 

Los intervalos siempre tienen un ":000" final como los cuatro últimos caracteres. Además, a diferencia de la fecha y hora, no puede usar asteriscos para indicar campos no usados. Además, todas las propiedades de tipo [CIM \_ DATETIME](cim-datetime.md) que representan intervalos deben marcarse con el calificador [estándar SubType,](standard-wmi-qualifiers.md) con el calificador establecido en "interval".

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

 

 



