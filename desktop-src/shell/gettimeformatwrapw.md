---
description: Da formato a la hora como una cadena de tiempo para una configuración regional especificada.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Función GetTimeFormatWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 6a23a615030b357eec4e40bbd8d6bc4a210bc7115b7aec76b45d6999de49f52c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679121"
---
# <a name="gettimeformatwrapw-function"></a>Función GetTimeFormatWrapW

\[**GetTimeFormatWrapW** está disponible para su uso en Windows XP. Es posible que no esté disponible en versiones posteriores. Debe usar [**GetTimeFormatW en**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) su lugar.\]

Da formato a la hora como una cadena de tiempo para una configuración regional especificada. La función da formato a una hora especificada o a la hora del sistema local.

> [!Note]  
> **GetTimeFormatWrapW es** un contenedor para la **función GetTimeFormatW.** Consulte la [**página GetTimeFormat para**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ En\]
</dt> <dd>

Tipo: **LCID**

Especifica la configuración regional para la que se va a dar formato a la cadena de tiempo. Si *pwzFormat* es **NULL,** la función da formato a la cadena según el formato de hora de esta configuración regional. Si *pwzFormat* no es **NULL,** la función usa la configuración regional solo para la información no especificada en la cadena de imagen de formato (por ejemplo, los marcadores de hora de la configuración regional).

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

Especifica varias opciones de función. Puede especificar una combinación de los valores siguientes.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE \_ NOUSEROVERRIDE**


</dt> <dd>

Si se establece, la función da formato a la cadena con el formato de hora predeterminado del sistema para la configuración regional especificada. Si no se establece, la función da formato a la cadena mediante cualquier invalidación de usuario al formato de hora predeterminado de la configuración regional. Esta marca solo se puede establecer si *pwzFormat* es **NULL.**

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**CONFIGURACIÓN REGIONAL \_ USE \_ CP \_ ACP**


</dt> <dd>

Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de configuración regional.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME \_ NOMINUTESORSECONDS**


</dt> <dd>

No usa minutos ni segundos.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME \_ NOSECONDS**


</dt> <dd>

No usa segundos.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME \_ NOTIMEMARKER**


</dt> <dd>

No usa un marcador de tiempo.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME \_ FORCE24HOURFORMAT**


</dt> <dd>

Siempre usa un formato de hora de 24 horas.

</dd> </dl> </dd> <dt>

*lpTime* \[ En\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \***

Puntero a una [**estructura SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de hora a la que se va a dar formato. Si este puntero es **NULL,** la función usa la hora actual del sistema local.

</dd> <dt>

*pwzFormat* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a un formato que se usará para formar la cadena de tiempo. Si *pwzFormat* es **NULL,** la función usa el formato de hora de la configuración regional especificada. Consulte [**GetTimeFormat para**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) obtener más detalles.

</dd> <dt>

*pwzTimeStr* \[ out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntero a un búfer que recibe la cadena de tiempo con formato.

</dd> <dt>

*cchTime* \[ En\]
</dt> <dd>

Tipo: **int**

Tamaño, en caracteres, del *búfer pwzTimeStr.* Si *cchTime* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de tiempo con formato y no se usa el búfer al que apunta *pwzTimeStr.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se realiza correctamente, el valor devuelto es el número de caracteres escritos en el búfer al que *apunta pwzTimeStr*. Si el *parámetro cchTime* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de tiempo con formato. El recuento incluye el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError puede** devolver uno de los siguientes códigos de error.

<dl> <dt>

**ERROR \_ BÚFER \_ INSUFICIENTE**
</dt> <dt>

**ERROR \_ MARCAS NO \_ VÁLIDAS**
</dt> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> </dl>

## <a name="remarks"></a>Comentarios

**GetTimeFormatWrapW proporciona** la capacidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a GetTimeFormatWrapW** directamente desde Shlwapi.dll, mediante el ordinal 310.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
