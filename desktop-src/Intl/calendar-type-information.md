---
description: En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) utilizada en las funciones EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo y GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Información de tipo de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d59229517143444aa00be9907b7419e0656147ad2fdaacf4aa5cec6e872caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147708"
---
# <a name="calendar-type-information"></a>Información de tipo de calendario

En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) utilizada en las funciones [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) [**EnumCalendarInfoExEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex) [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)y [**GetCalendarInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) La función [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) también usa algunos de estos valores.

Las siguientes constantes CALTYPE se pueden usar en combinación con cualquier otra constante CALTYPE.



| Constante                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAL \_ NOUSEROVERRIDE          | **Windows Me/98, Windows 2000:** Use el valor predeterminado del sistema en lugar de la elección del usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CAL \_ DEVUELVE \_ NOMBRES TIVE \_ | **Windows 7 y versiones posteriores:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) en forma de nombres adicionales de meses, que son los nombres que se usan cuando los nombres de mes se combinan con otros elementos. Por ejemplo, en Insensulte, el equivalente de enero se escribe "" cuando el mes se denomina por sí solo. Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa el formato tivetive del nombre. En el ejemplo Desastroso, el nombre del mes tive se muestra como "5 сtivos 2003". Para obtener más información, [vea LOCALE \_ RETURN \_ \_ TIVETIVE NAMES](locale-return-constants.md). |
| CAL \_ RETURN \_ NUMBER          | **Windows Me/98, Windows 2000:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como un número en lugar de una cadena. Esto solo es válido para los valores que comienzan por CAL \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ USE \_ CP \_ ACP            | **Windows Me/98, Windows 2000:** Use la página de códigos ANSI del sistema (ACP) en lugar de la página de códigos de configuración regional para la traducción de cadenas. Esto solo es relevante para las versiones ANSI de funciones, por ejemplo, **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Las siguientes constantes CALTYPE son mutuamente excluyentes y no se pueden usar en combinación entre sí en una llamada de función.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Valor entero que indica el tipo de calendario del calendario alternativo.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Valor entero que indica el límite superior del intervalo de año de dos dígitos.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Una o varias cadenas terminadas en NULL que especifican los desplazamientos de año para cada uno de los intervalos de era. La última cadena tiene un carácter nulo de terminación adicional. Este valor varía en formato en función del tipo de calendario opcional.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Nombre nativo abreviado del primer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Nombre nativo abreviado del segundo día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Nombre nativo abreviado del tercer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Nombre nativo abreviado del cuarto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Nombre nativo abreviado del quinto día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Nombre nativo abreviado del sexto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Nombre nativo abreviado del séptimo día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 y versiones posteriores:</strong> Nombre nativo abreviado de una era. La era completa se representa mediante la CAL_SERASTRING constante.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Nombre nativo abreviado del primer mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Nombre nativo abreviado del segundo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Nombre nativo abreviado del tercer mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Nombre nativo abreviado del cuarto mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Nombre nativo abreviado del quinto mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Nombre nativo abreviado del sexto mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Nombre nativo abreviado del séptimo mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Nombre nativo abreviado del octavo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Nombre nativo abreviado del noveno mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Nombre nativo abreviado del décimo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Nombre nativo abreviado del undécimo mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Nombre nativo abreviado del duodécimo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Nombre nativo abreviado del decimotercer mes del año, si existe.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Nombre nativo del calendario alternativo.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Nombre nativo del primer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Nombre nativo del segundo día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Nombre nativo del tercer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Nombre nativo del cuarto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Nombre nativo del quinto día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Nombre nativo del sexto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Nombre nativo del séptimo día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Una o varias cadenas terminadas en NULL que especifican cada uno de los puntos de código Unicode que especifican la era asociada a CAL_IYEAROFFSETRANGE. La última cadena tiene un carácter nulo de terminación adicional. Este valor varía en formato en función del tipo de calendario opcional.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Formatos de fecha largos para el tipo de calendario.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 y versiones posteriores:</strong> Formato del mes y día del tipo de calendario. El formato es similar al de los CAL_SLONGDATE. Por ejemplo, si el patrón Mes/Día es el nombre completo del mes seguido del número de día con ceros a la izquierda, por ejemplo, el 3 de septiembre, el formato es &quot; &quot; &quot; MMMM dd &quot; . Se pueden usar comillas simples para insertar caracteres sin formato, por ejemplo, "de" en español.
<blockquote>
[!Note]<br />
Este tipo de calendario solo admite un formato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Nombre nativo del primer mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Nombre nativo del segundo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Nombre nativo del tercer mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Nombre nativo del cuarto mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Nombre nativo del quinto mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Nombre nativo del sexto mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Nombre nativo del séptimo mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Nombre nativo del octavo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Nombre nativo del noveno mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Nombre nativo del décimo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Nombre nativo del undécimo mes del año.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Nombre nativo del duodécimo mes del año.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Nombre nativo del decimotercer mes del año, si existe.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Formatos de fecha cortos para el tipo de calendario.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del primer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del segundo día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del tercer día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del cuarto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del quinto día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del sexto día de la semana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del séptimo día de la semana.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98, Windows 2000:</strong> Formatos de año/mes para los calendarios especificados.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Si el nombre nativo del día de la semana o de un mes es una cadena vacía, ese nombre es idéntico al nombre especificado en la información de configuración regional correspondiente y, por tanto, no se duplica aquí.

 

 

 




