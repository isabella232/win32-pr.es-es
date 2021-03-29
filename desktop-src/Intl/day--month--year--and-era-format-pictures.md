---
description: La aplicación utiliza los elementos que se describen en este tema para construir una cadena de imagen con formato terminada en NULL.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Imágenes con formato de día, mes, año y era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912553"
---
# <a name="day-month-year-and-era-format-pictures"></a>Imágenes con formato de día, mes, año y era

La aplicación utiliza los elementos que se describen en este tema para construir una cadena de imagen con formato terminada en NULL. Si se usan espacios para separar los elementos de la cadena, estos espacios aparecerán en la misma ubicación en la cadena de salida.

> [!Note]  
> Los tipos de formato "d", "g" y "y" deben estar en minúsculas y la letra "M" debe estar en mayúsculas.

 

Por ejemplo, para obtener la cadena de fecha "Mié, agosto 31 94", la aplicación usa la cadena de imagen "DDD", "MMM DD AA".

La aplicación utiliza comillas simples para marcar los caracteres de modo que se muestren exactamente como se especifica. Si la aplicación debe mostrar una comilla simple, debe colocar dos comillas simples en una fila. Por ejemplo, "ABC", "bar", se muestra como "abc'bar".

En la tabla siguiente se definen los tipos de formato que se usan para representar días.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Día del mes como dígitos sin ceros a la izquierda para los días de un solo dígito.                                                                                                                                                                                                                                                                                                   |
| dd          | Día del mes como dígitos con ceros a la izquierda para los días de un solo dígito.                                                                                                                                                                                                                                                                                                      |
| ddd         | Día de la semana abreviado según lo especificado por un valor de [ \_ SABBREVDAYNAME \* de configuración regional](locale-sabbrev-constants.md) , por ejemplo, "LUN" en inglés (Estados Unidos).**Windows Vista y versiones posteriores:** si se requiere una versión abreviada del día de la semana, la aplicación debe usar las constantes de [ \_ SSHORTESTDAYNAME \* de configuración regional](locale-sshortestdayname-constants.md) .<br/> |
| dddd        | Día de la semana según lo especificado por un valor de [ \_ SDAYNAME \* de configuración regional](locale-sdayname-constants.md) .                                                                                                                                                                                                                                                                              |



 

En la tabla siguiente se definen los tipos de formato que se usan para representar los meses.



| Tipo de formato | Significado                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mes como dígitos sin ceros a la izquierda para los meses de un solo dígito.                                                                                                                   |
| MM          | Mes como dígitos con ceros a la izquierda para los meses de un solo dígito.                                                                                                                      |
| MMM         | El mes abreviado se especifica mediante un valor de [ \_ SABBREVMONTHNAME \* de configuración regional](locale-sabbrev-constants.md) , por ejemplo, "Nov" en inglés (Estados Unidos).                             |
| MMMM        | Mes según lo especificado por un valor de [ \_ SMONTHNAME \* de configuración regional](locale-smonthname-constants.md) , por ejemplo, "noviembre" para inglés (Estados Unidos) y "noviembre" para español (España). |



 

En la tabla siguiente se definen los tipos de formato que se usan para representar los años.



| Tipo de formato | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Año representado solo por el último dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Año representado solo por los dos últimos dígitos. Se agrega un cero a la izquierda para los años de un solo dígito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| aaaa        | Año representado por un total de cuatro o cinco dígitos, según el calendario utilizado. Los calendarios budista tailandés y Coreano tienen años de cinco dígitos. El patrón "yyyy" muestra cinco dígitos para estos dos calendarios y cuatro dígitos para todos los demás calendarios admitidos. Los calendarios que tienen años de un solo dígito o de dos dígitos, como para la era del Emperador japonés, se representan de forma diferente. Un año con un solo dígito se representa con un cero a la izquierda, por ejemplo, "03". Un año de dos dígitos se representa con dos dígitos, por ejemplo, "13". No se muestran ceros iniciales adicionales. |
| yyyyy       | Se comporta de forma idéntica a "yyyy".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

En la tabla siguiente se definen los tipos de formato que se usan para representar un punto o una era.



| Tipo de formato | Significado                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, GG       | Cadena de período/era con el formato especificado por el valor de SERASTRING de CAL \_ . Las imágenes con formato "g" y "GG" en una cadena de fecha se omiten si no hay ninguna era o cadena de período asociada. |



 

 

 




