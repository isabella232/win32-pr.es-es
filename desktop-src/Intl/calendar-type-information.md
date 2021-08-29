---
description: En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) usada en las funciones EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo y GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Información de tipo de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719591e3c912b68dca08ab600b9fa479377b9ef0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473731"
---
# <a name="calendar-type-information"></a>Información de tipo de calendario

En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) usada en las funciones [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) [**EnumCalendarInfoExEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex) [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)y [**GetCalendarInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) Algunos de estos valores también los usa la [**función SetCalendarInfo.**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Las siguientes constantes CALTYPE se pueden usar en combinación con cualquier otra constante CALTYPE.



| Constante                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAL \_ NOUSEROVERRIDE          | **Windows Me/98, Windows 2000:** Use el valor predeterminado del sistema en lugar de la elección del usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CAL \_ DEVUELVE \_ NOMBRES TIVE \_ | **Windows 7 y versiones posteriores:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) en forma de nombres teramétricos de meses, que son los nombres que se usan cuando los nombres de mes se combinan con otros elementos. Por ejemplo, en Insulsa, el equivalente de enero se escribe "" cuando el mes se denomina solo. Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa la forma tive del nombre. En el ejemplo Desastroso, el nombre del mes tive se muestra como "5 2003". Para obtener más información, [vea LOCALE \_ RETURN \_ TIVE \_ NAMES](locale-return-constants.md). |
| CAL \_ RETURN \_ NUMBER          | **Windows Me/98, Windows 2000:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como un número en lugar de una cadena. Esto solo es válido para los valores que comienzan por CAL \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ USE \_ CP \_ ACP            | **Windows Me/98, Windows 2000:** Use la página de códigos ANSI (ACP) del sistema en lugar de la página de códigos de configuración regional para la traducción de cadenas. Esto solo es relevante para las versiones ANSI de funciones, por ejemplo, **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Las siguientes constantes CALTYPE son mutuamente excluyentes y no se pueden usar en combinación entre sí en una llamada de función.




| Constante | Descripción | 
|----------|-------------|
| CAL_ICALINTVALUE | Valor entero que indica el tipo de calendario del calendario alternativo. | 
| CAL_ITWODIGITYEARMAX | <strong>Windows Me/98, Windows 2000:</strong> Valor entero que indica el límite superior del intervalo de año de dos dígitos. | 
| CAL_IYEAROFFSETRANGE | Una o varias cadenas terminadas en NULL que especifican los desplazamientos de año para cada uno de los intervalos de era. La última cadena tiene un carácter nulo de terminación adicional. Este valor varía en formato en función del tipo de calendario opcional. | 
| CAL_SABBREVDAYNAME1 | Nombre nativo abreviado del primer día de la semana. | 
| CAL_SABBREVDAYNAME2 | Nombre nativo abreviado del segundo día de la semana. | 
| CAL_SABBREVDAYNAME3 | Nombre nativo abreviado del tercer día de la semana. | 
| CAL_SABBREVDAYNAME4 | Nombre nativo abreviado del cuarto día de la semana. | 
| CAL_SABBREVDAYNAME5 | Nombre nativo abreviado del quinto día de la semana. | 
| CAL_SABBREVDAYNAME6 | Nombre nativo abreviado del sexto día de la semana. | 
| CAL_SABBREVDAYNAME7 | Nombre nativo abreviado del séptimo día de la semana. | 
| CAL_SABBREVERASTRING | <strong>Windows 7 y versiones posteriores:</strong> Nombre nativo abreviado de una era. La era completa se representa mediante la constante CAL_SERASTRING datos. | 
| CAL_SABBREVMONTHNAME1 | Nombre nativo abreviado del primer mes del año. | 
| CAL_SABBREVMONTHNAME2 | Nombre nativo abreviado del segundo mes del año. | 
| CAL_SABBREVMONTHNAME3 | Nombre nativo abreviado del tercer mes del año. | 
| CAL_SABBREVMONTHNAME4 | Nombre nativo abreviado del cuarto mes del año. | 
| CAL_SABBREVMONTHNAME5 | Nombre nativo abreviado del quinto mes del año. | 
| CAL_SABBREVMONTHNAME6 | Nombre nativo abreviado del sexto mes del año. | 
| CAL_SABBREVMONTHNAME7 | Nombre nativo abreviado del séptimo mes del año. | 
| CAL_SABBREVMONTHNAME8 | Nombre nativo abreviado del octavo mes del año. | 
| CAL_SABBREVMONTHNAME9 | Nombre nativo abreviado del noveno mes del año. | 
| CAL_SABBREVMONTHNAME10 | Nombre nativo abreviado del décimo mes del año. | 
| CAL_SABBREVMONTHNAME11 | Nombre nativo abreviado del undécimo mes del año. | 
| CAL_SABBREVMONTHNAME12 | Nombre nativo abreviado del duodécimo mes del año. | 
| CAL_SABBREVMONTHNAME13 | Nombre nativo abreviado del decimotercer mes del año, si existe. | 
| CAL_SCALNAME | Nombre nativo del calendario alternativo. | 
| CAL_SDAYNAME1 | Nombre nativo del primer día de la semana. | 
| CAL_SDAYNAME2 | Nombre nativo del segundo día de la semana. | 
| CAL_SDAYNAME3 | Nombre nativo del tercer día de la semana. | 
| CAL_SDAYNAME4 | Nombre nativo del cuarto día de la semana. | 
| CAL_SDAYNAME5 | Nombre nativo del quinto día de la semana. | 
| CAL_SDAYNAME6 | Nombre nativo del sexto día de la semana. | 
| CAL_SDAYNAME7 | Nombre nativo del séptimo día de la semana. | 
| CAL_SERASTRING | Una o varias cadenas terminadas en NULL que especifican cada uno de los puntos de código Unicode que especifican la era asociada a CAL_IYEAROFFSETRANGE. La última cadena tiene un carácter nulo de terminación adicional. Este valor varía en formato en función del tipo de calendario opcional. | 
| CAL_SLONGDATE | Formatos de fecha largos para el tipo de calendario. | 
| CAL_SMONTHDAY | <strong>Windows 7 y versiones posteriores:</strong> Formato del mes y día para el tipo de calendario. El formato es similar al de CAL_SLONGDATE. Por ejemplo, si el patrón Month/Day es el nombre completo del mes seguido del número de día con ceros a la izquierda, por ejemplo, "Septiembre 03", el formato es "MMMM dd". Se pueden usar comillas simples para insertar caracteres sin formato, por ejemplo, "de" en español.<blockquote>[!Note]<br />Este tipo de calendario solo admite un formato.</blockquote><br /> | 
| CAL_SMONTHNAME1 | Nombre nativo del primer mes del año. | 
| CAL_SMONTHNAME2 | Nombre nativo del segundo mes del año. | 
| CAL_SMONTHNAME3 | Nombre nativo del tercer mes del año. | 
| CAL_SMONTHNAME4 | Nombre nativo del cuarto mes del año. | 
| CAL_SMONTHNAME5 | Nombre nativo del quinto mes del año. | 
| CAL_SMONTHNAME6 | Nombre nativo del sexto mes del año. | 
| CAL_SMONTHNAME7 | Nombre nativo del séptimo mes del año. | 
| CAL_SMONTHNAME8 | Nombre nativo del octavo mes del año. | 
| CAL_SMONTHNAME9 | Nombre nativo del noveno mes del año. | 
| CAL_SMONTHNAME10 | Nombre nativo del décimo mes del año. | 
| CAL_SMONTHNAME11 | Nombre nativo del undécimo mes del año. | 
| CAL_SMONTHNAME12 | Nombre nativo del duodécimo mes del año. | 
| CAL_SMONTHNAME13 | Nombre nativo del decimotercer mes del año, si existe. | 
| CAL_SSHORTDATE | Formatos de fecha corta para el tipo de calendario. | 
| CAL_SSHORTESTDAYNAME1 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del primer día de la semana. | 
| CAL_SSHORTESTDAYNAME2 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del segundo día de la semana. | 
| CAL_SSHORTESTDAYNAME3 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del tercer día de la semana. | 
| CAL_SSHORTESTDAYNAME4 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del cuarto día de la semana. | 
| CAL_SSHORTESTDAYNAME5 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del quinto día de la semana. | 
| CAL_SSHORTESTDAYNAME6 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del sexto día de la semana. | 
| CAL_SSHORTESTDAYNAME7 | <strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del séptimo día de la semana. | 
| CAL_SYEARMONTH | <strong>Windows Me/98, Windows 2000:</strong> Formatos de año/mes para los calendarios especificados. | 




 

> [!Note]  
> Si el nombre nativo del día de la semana o de un mes es una cadena vacía, ese nombre es idéntico al nombre especificado en la información de configuración regional correspondiente y, por tanto, no se duplica aquí.

 

 

 




