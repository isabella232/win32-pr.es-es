---
description: En este tema se incluyen instrucciones para usar las funciones NLS en las aplicaciones para recuperar información de fecha y hora, así como datos de duración. Si la aplicación debe conservar los datos, consulte uso de datos de configuración regional persistentes.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Recuperar información de fecha y hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2c2fa1d15de2c1ba5587a981373ff14b1c1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688117"
---
# <a name="retrieving-time-and-date-information"></a>Recuperar información de fecha y hora

En este tema se incluyen instrucciones para usar las funciones NLS en las aplicaciones para recuperar información de [fecha y hora](time-and-date.md) , así como datos de duración. Si la aplicación debe conservar los datos, consulte [uso de datos de configuración regional persistentes](using-persistent-locale-data.md).

**Windows Vista y versiones posteriores:** Las funciones descritas en este tema pueden recuperar datos de [configuraciones regionales personalizadas](custom-locales.md). En concreto, se pueden usar para personalizar los formatos de fecha y hora. Por ejemplo, es posible tener un formato de hora como "hhHmm'ss" ", lo que da lugar a cadenas de hora como" 12H34 "12" ".

## <a name="retrieve-time-information"></a>Recuperar información de hora

La aplicación puede obtener cadenas para cualquier momento en un formato adecuado para la configuración regional actual mediante las funciones [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) y [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) . Cualquiera de las funciones comprueba cada uno de los valores de hora en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida para determinar que se encuentra dentro del intervalo de valores adecuado, omitiendo las partes de fecha de la estructura. Si alguno de los valores de hora está fuera del intervalo correcto, se produce un error en la función con el parámetro de código \_ no válido \_ . La función no devuelve ningún error para una cadena de formato incorrecto, pero simplemente forma la mejor cadena de tiempo posible.

> [!Note]  
> Las funciones de hora de NLS no incluyen los milisegundos como parte de una cadena de tiempo con formato.

 

Para obtener el formato de hora sin realizar ningún formato real, la aplicación puede usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) , especificando la constante [ \_ STIMEFORMAT de configuración regional](locale-stime-constants.md) en la llamada.

**Usar marcadores de tiempo**

Ejemplos de marcadores de hora son "AM" y "PM" para inglés (Estados Unidos) y "de". y "du". para español (México). Si \_ se especifica Time NOTIMEMARKER en la llamada a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex), la función quita los separadores anteriores y después del marcador de tiempo. Si existe un marcador de hora y la \_ marca Time NOTIMEMARKER no se establece en la llamada, la función localiza el marcador de tiempo en función del identificador de configuración regional especificado.

**Quitar separadores anteriores a los minutos y segundos**

La aplicación puede llamar a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con hora \_ NOMINUTESORSECONDS o Time \_ noseconds especificados para quitar los separadores que preceden a los elementos de minutos y/o segundos.

**Usar el formato de 24 horas**

Si la aplicación admite el formato de hora de 24 horas, puede llamar a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con la hora \_ FORCE24HOURFORMAT. A menos que \_ se establezca la marca Time NOTIMEMARKER, la función muestra cualquier marcador de tiempo existente.

## <a name="retrieve-date-information"></a>Recuperar información de fecha

Una aplicación puede recuperar cadenas para cualquier fecha en un formato adecuado para la configuración regional actual mediante las funciones [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) y [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) . Cualquiera de las funciones comprueba cada uno de los valores de fecha año, mes, día y día de la semana en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida, omitiendo las partes de tiempo de la estructura. El nombre del día, el nombre abreviado del día, el mes y el nombre abreviado del mes se localizan en función del identificador de configuración regional. Si el día de la semana es incorrecto, la función utiliza el valor correcto y no devuelve ningún error. Si alguno de los demás valores de fecha está fuera del intervalo correcto, se produce un error en la función y el parámetro de código \_ no es válido \_ . La función no devuelve ningún error para una cadena de formato incorrecto, pero simplemente forma la mejor cadena de fecha posible.

Si la aplicación requiere el formato de fecha para un calendario determinado, debe usar [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) o [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex), pasando el [**identificador de calendario**](calendar-identifiers.md)adecuado. Para devolver todos los formatos de fecha de un calendario determinado, la aplicación puede usar [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

**Especificar un calendario alternativo**

La aplicación puede llamar a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GETDATEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) con la fecha de marca \_ use \_ ALT \_ Calendar para usar el formato predeterminado para el calendario alternativo especificado. Si no hay ningún formato predeterminado para el calendario alternativo, la función usa invalidaciones de usuario.

Para obtener el formato de fecha de un calendario alternativo, la aplicación puede usar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ IOPTIONALCALENDAR de configuración regional](locale-ioptionalcalendar.md) .

**Especificar tipo de fecha**

Si la aplicación desea usar el formato de fecha corta, especifica \_ la fecha fechacorta en la llamada a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex). Se puede obtener un formato de fecha larga especificando \_ la fecha LONGDATE en la llamada de función. Si no se especifica ninguna marca y *lpFormat* se establece en **null**, la función usa la fecha \_ fechacorta como valor predeterminado.

Para obtener el formato de fecha corto y largo para el calendario de configuración regional predeterminado, la aplicación debe usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ SSHORTDATE](locale-sshortdate.md) o la [configuración regional \_ SLONGDATE](locale-slongdate.md) de configuración regional.

**Especificar la imagen de formato de fecha**

La aplicación puede especificar una imagen de formato de fecha que [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) usa para formar la cadena de fecha. Si se requiere el formato de fecha para la configuración regional especificada, la aplicación puede llamar a la función con *lpFormat* establecido en **null**. Si el parámetro no se establece en **null**, la función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen, por ejemplo, los nombres de día y mes de la configuración regional.

La aplicación puede incluir cualquier texto que deba permanecer en su forma exacta entre comillas simples. También se puede usar una comilla simple como carácter de escape para permitir que la marca se muestre en la cadena de fecha. Sin embargo, la secuencia de escape se debe incluir entre dos comillas simples. Por ejemplo, para mostrar la fecha como "may ' 93 ', la cadena de formato es:" MMMM ' ' ' ' YY '.

## <a name="retrieve-duration-information"></a>Recuperar información de duración

**Windows Vista y versiones posteriores:** Las funciones [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) y [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) están disponibles para obtener formatos de duración para configuraciones regionales, incluidas las configuraciones regionales personalizadas. Para obtener el formato de duración predeterminado para una configuración regional, la aplicación debe usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ SDURATION de configuración regional](locale-sduration.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[Fecha y hora](time-and-date.md)
</dt> <dt>

[Uso de datos de configuración regional persistentes](using-persistent-locale-data.md)
</dt> </dl>

 

 
