---
description: En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato de una cadena de tiempo. Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Imágenes de hora, minuto y segundo formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e201e72e4da621334a46f20c47e1dd5f731d7ea443bb9970ce07bb7f4e5455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130395"
---
# <a name="hour-minute-and-second-format-pictures"></a>Imágenes de hora, minuto y segundo formato

En este tema se describen los tipos de formato de las cadenas que se usan para crear la imagen de formato de una cadena de tiempo. Cada imagen de formato consta de una combinación de una cadena de cada uno de los tipos de formato.

> [!Note]  
> En los tipos de formato, las letras "m", "s" y "t" deben estar en minúsculas, y la letra "h" debe estar en minúsculas para indicar el reloj de 12 horas o mayúscula ("H") para indicar el reloj de 24 horas.

Se pueden usar comillas simples para marcar los caracteres que se deben mostrar exactamente como se ha especificado. Si la aplicación debe mostrar una comilla simple, debe colocar dos comillas simples en una fila. Por ejemplo, 'abc''bar', se muestra como "abc'bar".

En la tabla siguiente se definen los tipos de formato utilizados para representar horas.

| String | Significado                                                             |
|--------|---------------------------------------------------------------------|
| h      | Horas sin ceros iniciales para horas de un solo dígito (reloj de 12 horas). |
| hh     | Horas con ceros a la izquierda para horas de un solo dígito (reloj de 12 horas).    |
| H      | Horas sin ceros iniciales para horas de un solo dígito (reloj de 24 horas). |
| HH     | Horas con ceros iniciales para horas de un solo dígito (reloj de 24 horas).    |

En la tabla siguiente se definen los tipos de formato utilizados para representar minutos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| m      | Minutos sin ceros iniciales para minutos de un solo dígito. |
| MM     | Minutos con ceros a la izquierda para minutos de un solo dígito.    |

En la tabla siguiente se definen los tipos de formato utilizados para representar segundos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| s      | Segundos sin ceros iniciales para segundos de un solo dígito. |
| ss     | Segundos con ceros a la izquierda para segundos de un solo dígito.    |

En la tabla siguiente se definen los tipos de formato utilizados para representar un marcador de tiempo.

| String | Significado|
| ---    | ---    |
| t      | Cadena de marcador de un solo carácter.<br />**Nota:** Este formato no se recomienda para su uso con determinados idiomas, como japonés (Japón). Con este formato, una aplicación siempre toma el primer carácter [](locale-s1159.md) de la cadena de marcador de tiempo, definido por LOCALE_S1159 (AM) [y LOCALE_S2359](locale-s2359.md) (PM). Por este problema, la aplicación puede crear un formato incorrecto con la misma cadena que se usa para AM y PM.|
| tt     | Cadena de marcador de tiempo de varios caracteres. |
