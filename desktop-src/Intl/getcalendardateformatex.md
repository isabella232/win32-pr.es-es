---
description: Desusado.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687619"
---
# <a name="getcalendardateformatex-function"></a>GetCalendarDateFormatEx función)

En desuso. Recupera una cadena de fecha con el formato correcto para la configuración regional especificada utilizando la fecha y el calendario especificados. El usuario puede especificar el formato de fecha corta, el formato de fecha larga, el formato de mes o un modelo de formato personalizado.

> [!Note]  
> Esta función puede recuperar datos que cambian entre versiones, por ejemplo, debido a una configuración regional personalizada. Si la aplicación debe conservar o transmitir datos, consulte [uso de datos de configuración regional persistentes](using-persistent-locale-data.md).

 

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

*lpszLocale* \[ de\]
</dt> <dd>

Puntero a un nombre de configuración regional o a uno de los siguientes valores predefinidos.

-   [nombre de configuración regional \_ \_ invariable](locale-name-constants.md)
-   [nombre de configuración regional \_ \_ predeterminado del sistema \_](locale-name-constants.md)
-   [nombre de configuración regional \_ \_ predeterminado del usuario \_](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones de formato de fecha. Si *lpFormat* no está establecido en **null**, este parámetro debe establecerse en 0. Si *lpFormat* se establece en **null**, la aplicación puede especificar una combinación de los siguientes valores y [ \_ NOUSEROVERRIDE de configuración regional](locale-nouseroverride.md).



| Value                                                                                                                                                               | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**FECHA \_ fechacorta**</dt> </dl>    | Use el formato de fecha corta. Este es el valor predeterminado. Este valor no se puede usar con la fecha \_ LONGDATE o \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**FECHA \_ LONGDATE**</dt> </dl>       | Use el formato de fecha larga. Este valor no se puede usar con la fecha \_ fechacorta o \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**FECHA \_ YEARMONTH**</dt> </dl>    | Use el formato de año/mes. Este valor no se puede usar con la fecha \_ fechacorta o \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**FECHA \_ LTRREADING**</dt> </dl> | Agregue marcas para el diseño de lectura de izquierda a derecha. Este valor no se puede usar con la fecha \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**FECHA \_ RTLREADING**</dt> </dl> | Agregue marcas para el diseño de lectura de derecha a izquierda. Este valor no se puede usar con la fecha \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ de\]
</dt> <dd>

Puntero a una estructura [**CALDATETIME**](caldatetime.md) que contiene la información de fecha y de calendario a la que se va a dar formato.

</dd> <dt>

*lpFormat* \[ de\]
</dt> <dd>

Puntero a una cadena de imagen de formato que se usa para formar la cadena de fecha. Los valores posibles de la cadena de formato de imagen se definen en [imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md).

La cadena de formato de imagen debe terminar en NULL. La función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen, por ejemplo, los nombres de día y mes de la configuración regional. La aplicación establece este parámetro en **null** si la función va a usar el formato de fecha de la configuración regional especificada.

</dd> <dt>

*lpDateStr* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que esta función recibe la cadena de fecha con formato.

</dd> <dt>

*cchDate* \[ de\]
</dt> <dd>

Tamaño, en caracteres, del búfer *lpDateStr* . Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se usa el parámetro *lpDateStr* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres que se escriben en el búfer de *lpDateStr* si se realiza correctamente. Si el parámetro *cchDate* se establece en 0, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato, incluido el carácter nulo de terminación.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   \_fecha \_ de error fuera \_ del \_ intervalo. La fecha especificada estaba fuera del intervalo.
-   ERROR \_ de \_ búfer insuficiente. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.
-   ERROR en \_ marcas no válidas \_ . Los valores proporcionados para marcas no eran válidos.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

La primera fecha admitida por esta función es el 1 de enero de 1601.

Esta función no tiene asociado un archivo de encabezado o archivo de biblioteca. La aplicación puede llamar a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de DLL (Kernel32.dll) para obtener un identificador de módulo. Después, puede llamar a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el nombre de esta función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> <dt>

[Imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: ejemplo de API basadas en nombre](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
