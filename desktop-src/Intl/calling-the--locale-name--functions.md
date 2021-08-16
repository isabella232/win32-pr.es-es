---
description: Windows Vista presenta un gran número de funciones que usan nombres de configuración regional en lugar de identificadores de configuración regional.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Llamar a las funciones "Nombre de configuración regional"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc97490f21c54a187f2db31c6ee5c7eaa6c45e64069f9be9594c99e2376ef04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754895"
---
# <a name="calling-the-locale-name-functions"></a>Llamar a las funciones "Nombre de configuración regional"

Windows Vista presenta un gran número de funciones que usan nombres de [configuración regional en](locale-names.md) lugar de [identificadores de configuración regional.](locale-identifiers.md) Estas nuevas funciones proporcionan una buena compatibilidad con configuraciones [regionales](custom-locales.md)complementarias y varias de ellas proporcionan funcionalidad adicional que no está disponible en las funciones nls anteriores. Algunas de ellas, como las nuevas funciones de enumeración, también representan mejoras de diseño.

> [!Note]  
> Las aplicaciones diseñadas para ejecutarse solo en Windows Vista y versiones posteriores deben usar las funciones de "nombre de configuración regional" en lugar de las funciones NLS que usan identificadores de configuración regional.

 

En la tabla siguiente se enumeran las funciones de nombre de configuración regional junto con las funciones anteriores que pueden reemplazar.



| Funciones que usan nombres de configuración regional                                     | Funciones que usan identificadores de configuración regional                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [ **EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) |
| [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | [**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [ **EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)     |
| [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [**EnumSystemLocales**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [**EnumTimeFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [**EnumTimeFormats**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [**GetCurrencyFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [**GetCurrencyFormat**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [**GetNumberFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [**GetNumberFormat**](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [**IsValidLocale**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a>Ejemplo

Puede encontrar un ejemplo que muestra el uso de varias funciones basadas en nombres de configuración regional en [NLS: Ejemplo](nls--name-based-apis-sample.md)de API basadas en nombres .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> </dl>

 

 
