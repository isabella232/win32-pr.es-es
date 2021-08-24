---
description: En este tema se incluyen instrucciones para usar las funciones nls en las aplicaciones para recuperar información de fecha y hora, así como datos de duración. Si la aplicación debe conservar los datos, consulte Uso de datos de configuración regional persistentes.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Recuperar información de fecha y hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f461f12cb1c6324892a415142c159ba570759128e61dd02b53a7cceebccc57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040415"
---
# <a name="retrieving-time-and-date-information"></a>Recuperar información de fecha y hora

En este tema se incluyen instrucciones para usar las funciones nls en las aplicaciones para recuperar información de fecha [y](time-and-date.md) hora, así como datos de duración. Si la aplicación debe conservar los datos, consulte [Uso de datos de configuración regional persistentes.](using-persistent-locale-data.md)

**Windows Vista y versiones posteriores:** Las funciones analizadas en este tema pueden recuperar datos de [configuraciones regionales personalizadas.](custom-locales.md) En concreto, se pueden usar para personalizar los formatos de fecha y hora. Por ejemplo, es posible tener un formato de hora como "hhHmm'ss'", lo que da lugar a cadenas de tiempo como "12H34'12'".

## <a name="retrieve-time-information"></a>Recuperar información de hora

La aplicación puede obtener cadenas para cualquier momento en un formato adecuado para la configuración regional actual mediante las funciones [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) y [**GetTimeFormatEx.**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) Cualquiera de las funciones comprueba cada uno de los valores de hora de una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida para determinar que se encuentra dentro del intervalo de valores adecuado, omitiendo las partes de fecha de la estructura. Si alguno de los valores de hora está fuera del intervalo correcto, se produce un error en la función con el código ERROR \_ INVALID \_ PARAMETER. La función no devuelve ningún error para una cadena de formato no correcto, sino que simplemente constituye la mejor cadena de tiempo posible.

> [!Note]  
> Las funciones de tiempo NLS no incluyen milisegundos como parte de una cadena de tiempo con formato.

 

Para obtener el formato de hora sin realizar ningún formato real, la aplicación puede usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) especificando la constante [ \_ LOCALE STIMEFORMAT](locale-stime-constants.md) en la llamada.

**Usar marcadores de tiempo**

Algunos ejemplos de marcadores de tiempo son "AM" y "PM" para inglés (Estados Unidos) y "de". y "du". para español (México). Si se especifica TIME NOTIMEMARKER en la llamada a \_ [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx,**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)la función quita los separadores anteriores y siguientes al marcador de hora. Si existe un marcador de tiempo y la marca TIME NOTIMEMARKER no está establecida en la llamada, la función localiza el marcador de tiempo en función del identificador de configuración \_ regional especificado.

**Quitar separadores que preceden a minutos y segundos**

La aplicación puede llamar a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con TIME \_ NOMINUTESORSECONDS o TIME NOSECONDS especificados para quitar los separadores anteriores a los elementos de minutos o \_ segundos.

**Usar el formato de hora de 24 horas**

Si la aplicación admite el formato de hora de 24 horas, puede llamar a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con \_ TIME FORCE24HOURFORMAT. A menos que se establezca la marca TIME \_ NOTIMEMARKER, la función muestra cualquier marcador de hora existente.

## <a name="retrieve-date-information"></a>Recuperar información de fecha

Una aplicación puede recuperar cadenas para cualquier fecha en un formato adecuado para la configuración regional actual mediante las funciones [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) y [**GetDateFormatEx.**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) Cualquiera de las funciones comprueba cada uno de los valores de fecha año, mes, día y día de la semana en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida, omitiendo las partes de hora de la estructura. El nombre de día, el nombre de día abreviado, el nombre del mes y el nombre abreviado del mes se localizan en función del identificador de configuración regional. Si el día de la semana es incorrecto, la función usa el valor correcto y no devuelve ningún error. Si alguno de los demás valores de fecha está fuera del intervalo correcto, se produce un error en la función con el código ERROR \_ INVALID \_ PARAMETER. La función no devuelve ningún error para una cadena de formato no correcto, sino que simplemente constituye la mejor cadena de fecha posible.

Si la aplicación requiere el formato de fecha para un calendario determinado, debe usar [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) o [**GetCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)pasando el identificador [**de calendario adecuado.**](calendar-identifiers.md) Para devolver todos los formatos de fecha de un calendario determinado, la aplicación puede usar [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex) [**EnumDateFormatsEx o**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

**Especificar un calendario alternativo**

La aplicación puede llamar a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) con la marca DATE USE ALT CALENDAR para usar el formato predeterminado para \_ el calendario alternativo \_ \_ especificado. Si no hay ningún formato predeterminado para el calendario alternativo, la función usa las invalidaciones de usuario.

Para obtener el formato de fecha de un calendario alternativo, la aplicación puede usar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la [constante \_ LOCALE IOPTIONALCALENDAR.](locale-ioptionalcalendar.md)

**Especificar tipo de fecha**

Si la aplicación quiere usar el formato de fecha corta, especifica DATE SHORTDATE en la llamada a \_ [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx.**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) Se puede obtener un formato de fecha larga especificando DATE \_ LONGDATE en la llamada de función. Si no se especifica ninguna marca y *lpFormat* se establece en **NULL,** la función usa DATE \_ SHORTDATE como valor predeterminado.

Para obtener el formato de fecha corta y larga para el calendario de configuración regional predeterminado, la aplicación debe usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [LOCALE \_ SSHORTDATE](locale-sshortdate.md) o [LOCALE \_ SLONGDATE.](locale-slongdate.md)

**Especificar la imagen de formato de fecha**

La aplicación puede especificar una imagen de formato de fecha [**que GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) usa para formar la cadena de fecha. Si se requiere el formato de fecha para la configuración regional especificada, la aplicación puede llamar a la función con *lpFormat* establecido en **NULL.** Si el parámetro no se establece en **NULL,** la función usa la configuración regional solo para la información no especificada en la cadena de imagen de formato, por ejemplo, los nombres de día y mes de la configuración regional.

La aplicación puede incluir cualquier texto que deba permanecer en su forma exacta entre comillas simples. También se puede usar una comilla simple como carácter de escape para permitir que la propia marca se muestre en la cadena de fecha. Sin embargo, la secuencia de escape debe incluirse entre dos comillas simples. Por ejemplo, para mostrar la fecha como "May '93", la cadena de formato es: "MMMM ''''yy".

## <a name="retrieve-duration-information"></a>Recuperar información de duración

**Windows Vista y versiones posteriores:** Las funciones [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) y [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) están disponibles para obtener los formatos de duración de las configuraciones regionales, incluidas las configuraciones regionales personalizadas. Para obtener el formato de duración predeterminado para una configuración regional, la aplicación debe usar la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la [constante \_ LOCALE SDURATION.](locale-sduration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[Fecha y hora](time-and-date.md)
</dt> <dt>

[Uso de datos de configuración regional persistentes](using-persistent-locale-data.md)
</dt> </dl>

 

 
