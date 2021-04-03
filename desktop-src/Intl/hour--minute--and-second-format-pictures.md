---
description: En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato para una cadena de hora. Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Imágenes con formato de hora, minuto y segundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083478"
---
# <a name="hour-minute-and-second-format-pictures"></a>Imágenes con formato de hora, minuto y segundo

En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato para una cadena de hora. Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.

> [!Note]  
> En los tipos de formato, las letras "m", "s" y "t" deben estar en minúsculas, y la letra "h" debe estar en minúsculas para indicar el reloj de 12 horas o mayúsculas ("H") para indicar el reloj de 24 horas.

Las comillas simples se pueden usar para marcar los caracteres que se deben mostrar exactamente como se especifican. Si la aplicación debe mostrar una comilla simple, debe colocar dos comillas simples en una fila. Por ejemplo, "ABC", "bar", se muestra como "abc'bar".

En la tabla siguiente se definen los tipos de formato que se usan para representar las horas.

| String | Significado                                                             |
|--------|---------------------------------------------------------------------|
| h      | Horas sin ceros a la izquierda para las horas de un solo dígito (reloj de 12 horas). |
| hh     | Horas con ceros a la izquierda para las horas de un solo dígito (reloj de 12 horas).    |
| H      | Horas sin ceros a la izquierda para las horas de un solo dígito (reloj de 24 horas). |
| HH     | Horas con ceros a la izquierda para las horas de un solo dígito (reloj de 24 horas).    |

En la tabla siguiente se definen los tipos de formato que se usan para representar los minutos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| m      | Minutos sin ceros a la izquierda para los minutos con un solo dígito. |
| MM     | Minutos con ceros a la izquierda para los minutos con un solo dígito.    |

En la tabla siguiente se definen los tipos de formato que se usan para representar los segundos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| s      | Segundos sin ceros a la izquierda para los segundos de un solo dígito. |
| ss     | Segundos con ceros a la izquierda para los segundos de un solo dígito.    |

En la tabla siguiente se definen los tipos de formato que se usan para representar un marcador de tiempo.

| String | Significado|
| ---    | ---    |
| t      | Cadena de marcador de tiempo de un carácter.<br />**Nota:** No se recomienda usar este formato con determinados idiomas, como japonés (Japón). Con este formato, una aplicación siempre toma el primer carácter de la cadena de marcador de hora, definida por [LOCALE_S1159](locale-s1159.md) (AM) y [LOCALE_S2359](locale-s2359.md) (PM). Por esta razón, la aplicación puede crear un formato incorrecto con la misma cadena que se usa para AM y PM.|
| tt     | Cadena de marcador de tiempo de varios caracteres. |
