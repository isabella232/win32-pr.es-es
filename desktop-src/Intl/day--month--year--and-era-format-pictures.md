---
description: La aplicación usa los elementos descritos en este tema para construir una cadena de imagen de formato terminada en NULL.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Imágenes con formato de día, mes, año y era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ae1adf82a202ebb08f199bb252e59c0f35aab8ad35b60ac57a8ebbe102711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068275"
---
# <a name="day-month-year-and-era-format-pictures"></a>Imágenes con formato de día, mes, año y era

La aplicación usa los elementos descritos en este tema para construir una cadena de imagen de formato terminada en NULL. Si se usan espacios para separar los elementos de la cadena, estos espacios aparecerán en la misma ubicación en la cadena de salida.

> [!Note]  
> Los tipos de formato "d", "g" e "y" deben estar en minúsculas y la letra "M" debe estar en mayúsculas.

 

Por ejemplo, para obtener la cadena de fecha "Wed, Ago 31 94", la aplicación usa la cadena de imagen "ddd", "MMM dd yy".

La aplicación usa comillas simples para marcar caracteres para mostrar exactamente como se especifica. Si la aplicación debe mostrar una comilla simple, debe colocar dos comillas simples en una fila. Por ejemplo, 'abc''bar', se muestra como "abc'bar".

En la tabla siguiente se definen los tipos de formato utilizados para representar los días.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Día del mes como dígitos sin ceros a la izquierda para días de un solo dígito.                                                                                                                                                                                                                                                                                                   |
| dd          | Día del mes como dígitos con ceros iniciales para días de un solo dígito.                                                                                                                                                                                                                                                                                                      |
| ddd         | Día abreviado de la semana según lo especificado por un valor [DE LOCALE \_ SABBREVDAYNAME, \*](locale-sabbrev-constants.md) por ejemplo, "Mon" en inglés (Estados Unidos).**Windows Vista y versiones posteriores:** si se requiere una versión corta del día de la semana, la aplicación debe usar las constantes [ \_ LOCALE SSHORTESTDAYNAME. \*](locale-sshortestdayname-constants.md)<br/> |
| dddd        | Día de la semana según lo especificado por un [valor \_ LOCALE SDAYNAME. \* ](locale-sdayname-constants.md)                                                                                                                                                                                                                                                                              |



 

En la tabla siguiente se definen los tipos de formato utilizados para representar meses.



| Tipo de formato | Significado                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mes como dígitos sin ceros a la izquierda para meses de un solo dígito.                                                                                                                   |
| MM          | Mes como dígitos con ceros a la izquierda para meses de un solo dígito.                                                                                                                      |
| MMM         | Mes abreviado según lo especificado por un valor [DE LOCALE \_ SABBREVMONTHNAME, \* ](locale-sabbrev-constants.md) por ejemplo, "Noviembre" en inglés (Estados Unidos).                             |
| MMMM        | Mes especificado por un valor [ \_ LOCALE SMONTHNAME, \* ](locale-smonthname-constants.md) por ejemplo, "Noviembre" para inglés (Estados Unidos) y "Noviembre" para español (España). |



 

En la tabla siguiente se definen los tipos de formato usados para representar los años.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Año representado solo por el último dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Año representado solo por los dos últimos dígitos. Se agrega un cero a la izquierda para años de un solo dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| aaaa        | Año representado por cuatro o cinco dígitos completos, según el calendario utilizado. Los calendarios tailandés y coreano tienen años de cinco dígitos. El patrón "yyyy" muestra cinco dígitos para estos dos calendarios y cuatro dígitos para todos los demás calendarios admitidos. Los calendarios que tienen años de un solo dígito o de dos dígitos, como para la era del japonés, se representan de forma diferente. Un año de un solo dígito se representa con un cero inicial, por ejemplo, "03". Un año de dos dígitos se representa con dos dígitos, por ejemplo, "13". No se muestran ceros iniciales adicionales. |
| yyyyy       | Se comporta de forma idéntica a "yyyy".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

En la tabla siguiente se definen los tipos de formato utilizados para representar un punto o una era.



| Tipo de formato | Significado                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, gg       | Cadena de período o era con el formato especificado por el valor \_ de CAL SERASTRING. Las imágenes de formato "g" y "gg" de una cadena de fecha se omiten si no hay ninguna cadena de era o punto asociada. |



 

 

 




