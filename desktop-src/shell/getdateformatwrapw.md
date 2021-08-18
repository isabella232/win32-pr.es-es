---
description: Da formato a una fecha como una cadena de fecha para una configuración regional especificada.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: Función GetDateFormatWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 9a45222c316d321ee151c19464d453827437514dd93ffe3da5b1a9849e8a7196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395885"
---
# <a name="getdateformatwrapw-function"></a>Función GetDateFormatWrapW

\[**GetDateFormatWrapW** está disponible para su uso en Windows XP. No estará disponible en versiones posteriores. Debe usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) en su lugar.\]

Da formato a una fecha como una cadena de fecha para una configuración regional especificada. La función da formato a una fecha especificada o a la fecha del sistema local.

> [!Note]  
> **GetDateFormatWrapW es** un contenedor de la **función GetDateFormatW.** Consulte la [**página GetDateFormat para**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ En\]
</dt> <dd>

Tipo: **LCID**

Configuración regional para la que se va a dar formato a la cadena de fecha. Si *pwzFormat* es **NULL,** la función da formato a la cadena según el formato de fecha de esta configuración regional. Si *pwzFormat* no es **NULL,** la función usa la configuración regional solo para la información no especificada en la cadena de imagen de formato (por ejemplo, los nombres de día y mes de la configuración regional).

Este parámetro puede ser un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) o uno de los siguientes valores predefinidos.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA**


</dt> <dd>

Configuración regional del sistema predeterminada.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO**


</dt> <dd>

Configuración regional de usuario predeterminada.

</dd> </dl> </dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Especifica varias opciones de función. Si *pwzFormat* no es **NULL,** este parámetro debe ser cero. Si *pwzFormat* **es NULL,** puede especificar una combinación de los valores siguientes. Si no especifica DATE \_ YEARMONTH, DATE SHORTDATE o \_ DATE \_ LONGDATE, *y pwzFormat* es **NULL,** date SHORTDATE se usa como valor \_ predeterminado.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE \_ NOUSEROVERRIDE**


</dt> <dd>

Si se establece, la función da formato a la cadena con el formato de fecha predeterminado del sistema para la configuración regional especificada. Si no se establece, la función da formato a la cadena utilizando cualquier invalidación de usuario al formato de fecha predeterminado de la configuración regional.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**CONFIGURACIÓN REGIONAL \_ USE \_ CP \_ ACP**


</dt> <dd>

Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de la configuración regional.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE \_ SHORTDATE**


</dt> <dd>

Usa el formato de fecha corta. Este valor no se puede usar con DATE \_ LONGDATE o DATE \_ YEARMONTH.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE \_ LONGDATE**


</dt> <dd>

Usa el formato de fecha larga. Este valor no se puede usar con DATE \_ SHORTDATE o DATE \_ YEARMONTH.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE \_ YEARMONTH**


</dt> <dd>

Usa el formato año/mes. Este valor no se puede usar con DATE \_ SHORTDATE o DATE \_ LONGDATE.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**FECHA \_ DE USO DEL CALENDARIO \_ \_ ALT**


</dt> <dd>

Usa el calendario alternativo, si existe, para dar formato a la cadena de fecha. Si se establece esta marca, la función usa el formato predeterminado para ese calendario alternativo, en lugar de usar invalidaciones de usuario. Las invalidaciones de usuario solo se usarán en caso de que no haya ningún formato predeterminado para el calendario alternativo especificado.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE \_ LTRREADING**


</dt> <dd>

Agrega marcas para el diseño de lectura de izquierda a derecha. Este valor no se puede usar con DATE \_ RTLREADING.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE \_ RTLREADING**


</dt> <dd>

Agrega marcas para el diseño de lectura de derecha a izquierda. Este valor no se puede usar con DATE \_ LTRREADING.

</dd> </dl> </dd> <dt>

*lpDate* \[ En\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \***

Puntero a una [**estructura SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de fecha a la que se va a dar formato. Si este puntero es **NULL,** la función utiliza la fecha actual del sistema local.

</dd> <dt>

*pwzFormat* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una imagen de formato que se usará para formar la cadena de fecha. Si *pwzFormat* es **NULL,** la función usa el formato de fecha de la configuración regional especificada. Consulte [**GetDateFormat para**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) obtener más detalles.

</dd> <dt>

*pwzDateStr* \[ out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntero a un búfer que recibe la cadena de fecha con formato.

</dd> <dt>

*cchDate* \[ En\]
</dt> <dd>

Tipo: **int**

Especifica el tamaño, en caracteres, del *búfer pwzDateStr.* Si *cchDate* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se usa el búfer al que *apunta pwzDateStr.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se realiza correctamente, el valor devuelto es el número de caracteres escritos en el búfer al que *apunta pwzDateStr*. Si el *parámetro cchDate* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de fecha con formato. El recuento incluye el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError puede** devolver uno de los siguientes códigos de error.

<dl> <dt>

**ERROR \_ BÚFER \_ INSUFICIENTE**
</dt> <dt>

**ERROR \_ MARCAS NO \_ VÁLIDAS**
</dt> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> </dl>

## <a name="remarks"></a>Comentarios

**GetDateFormatWrapW proporciona** la capacidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a GetDateFormatWrapW** directamente desde Shlwapi.dll, mediante ordinal 311.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
