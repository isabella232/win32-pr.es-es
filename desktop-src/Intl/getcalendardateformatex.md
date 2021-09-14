---
description: Desusado.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Función GetCalendarDateFormatEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274631"
---
# <a name="getcalendardateformatex-function"></a>Función GetCalendarDateFormatEx

En desuso. Recupera una cadena de fecha con el formato correcto para la configuración regional especificada mediante la fecha y el calendario especificados. El usuario puede especificar el formato de fecha corta, el formato de fecha larga, el formato de mes del año o un patrón de formato personalizado.

> [!Note]  
> Esta función puede recuperar datos que cambian entre versiones, por ejemplo, debido a una configuración regional personalizada. Si la aplicación debe conservar o transmitir datos, consulte [Uso de datos de configuración regional persistentes.](using-persistent-locale-data.md)

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszLocale* \[ En\]
</dt> <dd>

Puntero a un nombre de configuración regional o uno de los siguientes valores predefinidos.

-   [NOMBRE DE \_ CONFIGURACIÓN REGIONAL \_ INVARIABLE](locale-name-constants.md)
-   [VALOR PREDETERMINADO DEL \_ SISTEMA DE NOMBRES DE CONFIGURACIÓN \_ \_ REGIONAL](locale-name-constants.md)
-   [CONFIGURACIÓN REGIONAL NOMBRE \_ DE \_ USUARIO \_ PREDETERMINADO](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de formato de fecha. Si *lpFormat* no está establecido en **NULL,** este parámetro debe establecerse en 0. Si *lpFormat* se establece en **NULL,** la aplicación puede especificar una combinación de los valores siguientes y [LOCALE \_ NOUSEROVERRIDE](locale-nouseroverride.md).



| Value                                                                                                                                                               | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**DATE \_ SHORTDATE**</dt> </dl>    | Use el formato de fecha corta. Este es el valor predeterminado. Este valor no se puede usar con DATE \_ LONGDATE o DATE \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**DATE \_ LONGDATE**</dt> </dl>       | Use el formato de fecha larga. Este valor no se puede usar con DATE \_ SHORTDATE o DATE \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**DATE \_ YEARMONTH**</dt> </dl>    | Use el formato año/mes. Este valor no se puede usar con DATE \_ SHORTDATE o DATE \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**DATE \_ LTRREADING**</dt> </dl> | Agregue marcas para el diseño de lectura de izquierda a derecha. Este valor no se puede usar con DATE \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**DATE \_ RTLREADING**</dt> </dl> | Agregue marcas para el diseño de lectura de derecha a izquierda. Este valor no se puede usar con DATE \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ En\]
</dt> <dd>

Puntero a una [**estructura CALDATETIME**](caldatetime.md) que contiene la información de fecha y calendario a la que se debe dar formato.

</dd> <dt>

*lpFormat* \[ En\]
</dt> <dd>

Puntero a una cadena de imagen de formato que se usa para formar la cadena de fecha. Los valores posibles para la cadena de imagen de formato se definen en Imágenes de formato de [día, mes, año y era.](day--month--year--and-era-format-pictures.md)

La cadena de imagen de formato debe terminar en NULL. La función usa la configuración regional solo para la información no especificada en la cadena de imagen de formato, por ejemplo, los nombres de día y mes de la configuración regional. La aplicación establece este parámetro en **NULL** si la función va a usar el formato de fecha de la configuración regional especificada.

</dd> <dt>

*lpDateStr* \[ out\]
</dt> <dd>

Puntero a un búfer en el que esta función recibe la cadena de fecha con formato.

</dd> <dt>

*cchDate* \[ En\]
</dt> <dd>

Tamaño, en caracteres, del *búfer lpDateStr.* Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se usa el parámetro *lpDateStr.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres escritos en el *búfer lpDateStr* si se realiza correctamente. Si el *parámetro cchDate* se establece en 0, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato, incluido el carácter nulo de terminación.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   FECHA \_ DE ERROR FUERA DEL \_ \_ \_ INTERVALO. La fecha especificada estaba fuera del intervalo.
-   ERROR \_ BÚFER \_ INSUFICIENTE. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **NULL.**
-   ERROR \_ MARCAS NO \_ VÁLIDAS. Los valores proporcionados para las marcas no eran válidos.
-   ERROR \_ PARÁMETRO NO \_ VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

La fecha más temprana admitida por esta función es el 1 de enero de 1601.

Esta función no tiene un archivo de encabezado o archivo de biblioteca asociado. La aplicación puede llamar [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Kernel32.dll) para obtener un identificador de módulo. A continuación, puede llamar [**a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: ejemplo de API basadas en nombres](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
