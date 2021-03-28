---
description: Da formato a una fecha como una cadena de fecha para una configuración regional especificada.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW función)
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
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276754"
---
# <a name="getdateformatwrapw-function"></a>GetDateFormatWrapW función)

\[**GetDateFormatWrapW** está disponible para su uso en Windows XP. No estará disponible en las versiones posteriores. Debe usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) en su lugar.\]

Da formato a una fecha como una cadena de fecha para una configuración regional especificada. La función da formato a una fecha especificada o a la fecha del sistema local.

> [!Note]  
> **GetDateFormatWrapW** es un contenedor para la función **GetDateFormatW** . Vea la página [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener más notas de uso.

 

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

*Configuración regional* \[ de\]
</dt> <dd>

Tipo: **LCID**

La configuración regional para la que se va a dar formato a la cadena de fecha. Si *pwzFormat* es **null**, la función da formato a la cadena de acuerdo con el formato de fecha de esta configuración regional. Si *pwzFormat* no es **null**, la función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen (por ejemplo, los nombres de día y mes de la configuración regional).

Este parámetro puede ser un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , o uno de los siguientes valores predefinidos.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**configuración \_ predeterminada del sistema local \_**


</dt> <dd>

Configuración regional predeterminada del sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_valor predeterminado del usuario de configuración regional \_**


</dt> <dd>

Configuración regional predeterminada del usuario.

</dd> </dl> </dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Especifica varias opciones de función. Si *pwzFormat* no es **null**, este parámetro debe ser cero. Si *pwzFormat* es **null**, puede especificar una combinación de los valores siguientes. Si no especifica la fecha \_ YEARMONTH, la fecha \_ fechacorta o la fecha \_ LONGDATE, y *pwzFormat* es **null**, se \_ usará la fecha fechacorta como valor predeterminado.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**configuración regional \_ NOUSEROVERRIDE**


</dt> <dd>

Si se establece, la función da formato a la cadena con el formato de fecha predeterminado del sistema para la configuración regional especificada. Si no se establece, la función da formato a la cadena mediante cualquier invalidación de usuario en el formato de fecha predeterminado de la configuración regional.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**configuración regional \_ use \_ CP \_ ACP**


</dt> <dd>

Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de la configuración regional.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**FECHA \_ fechacorta**


</dt> <dd>

Utiliza el formato de fecha corta. Este valor no se puede usar con la fecha \_ LONGDATE o \_ YEARMONTH.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**FECHA \_ LONGDATE**


</dt> <dd>

Utiliza el formato de fecha larga. Este valor no se puede usar con la fecha \_ fechacorta o \_ YEARMONTH.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**FECHA \_ YEARMONTH**


</dt> <dd>

Usa el formato de año/mes. Este valor no se puede usar con la fecha \_ fechacorta o \_ LONGDATE.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**FECHA \_ usar \_ \_ calendario Alt**


</dt> <dd>

Utiliza el calendario alternativo, si existe, para dar formato a la cadena de fecha. Si se establece esta marca, la función usa el formato predeterminado para ese calendario alternativo, en lugar de utilizar las invalidaciones de usuario. Las invalidaciones de usuario solo se utilizarán en caso de que no haya ningún formato predeterminado para el calendario alternativo especificado.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**FECHA \_ LTRREADING**


</dt> <dd>

Agrega marcas para el diseño de lectura de izquierda a derecha. Este valor no se puede usar con la fecha \_ RTLREADING.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**FECHA \_ RTLREADING**


</dt> <dd>

Agrega marcas para el diseño de lectura de derecha a izquierda. Este valor no se puede usar con la fecha \_ LTRREADING.

</dd> </dl> </dd> <dt>

*lpDate* \[ de\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Puntero a una estructura [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de fecha a la que se va a dar formato. Si este puntero es **null**, la función usa la fecha actual del sistema local.

</dd> <dt>

*pwzFormat* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una imagen de formato que se va a usar para formar la cadena de fecha. Si *pwzFormat* es **null**, la función usa el formato de fecha de la configuración regional especificada. Consulte [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) para obtener más información.

</dd> <dt>

*pwzDateStr* \[ enuncia\]
</dt> <dd>

Tipo: **LPWStr**

Un puntero a un búfer que recibe la cadena de fecha con formato.

</dd> <dt>

*cchDate* \[ de\]
</dt> <dd>

Tipo: **int**

Especifica el tamaño, en caracteres, del búfer de *pwzDateStr* . Si *cchDate* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de fecha con formato y no se utiliza el búfer al que apunta *pwzDateStr* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se ejecuta correctamente, el valor devuelto es el número de caracteres que se escriben en el búfer al que apunta *pwzDateStr*. Si el parámetro *cchDate* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de fecha con formato. El recuento incluye el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** puede devolver uno de los siguientes códigos de error.

<dl> <dt>

**ERROR \_ de \_ búfer insuficiente**
</dt> <dt>

**ERROR de \_ marcas no válidas \_**
</dt> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> </dl>

## <a name="remarks"></a>Observaciones

**GetDateFormatWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **GetDateFormatWrapW** directamente desde Shlwapi.dll, mediante el ordinal 311.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
