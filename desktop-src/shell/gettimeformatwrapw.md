---
description: Da formato a la hora como una cadena de hora para una configuración regional especificada.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW función)
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
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985483"
---
# <a name="gettimeformatwrapw-function"></a>GetTimeFormatWrapW función)

\[**GetTimeFormatWrapW** está disponible para su uso en Windows XP. Puede que no esté disponible en versiones posteriores. Debe usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) en su lugar.\]

Da formato a la hora como una cadena de hora para una configuración regional especificada. La función da formato a una hora especificada o a la hora del sistema local.

> [!Note]  
> **GetTimeFormatWrapW** es un contenedor para la función **GetTimeFormatW** . Vea la página [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obtener más notas de uso.

 

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

*Configuración regional* \[ de\]
</dt> <dd>

Tipo: **LCID**

Especifica la configuración regional para la que se va a dar formato a la cadena de hora. Si *pwzFormat* es **null**, la función da formato a la cadena según el formato de hora de esta configuración regional. Si *pwzFormat* no es **null**, la función usa la configuración regional solo para la información que no se especifica en la cadena de formato de imagen (por ejemplo, los marcadores de hora de la configuración regional).

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

Especifica varias opciones de función. Puede especificar una combinación de los valores siguientes.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**configuración regional \_ NOUSEROVERRIDE**


</dt> <dd>

Si se establece, la función da formato a la cadena con el formato de hora predeterminado del sistema para la configuración regional especificada. Si no se establece, la función da formato a la cadena mediante cualquier reemplazo de usuario al formato de hora predeterminado de la configuración regional. Esta marca solo se puede establecer si *pwzFormat* es **null**.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**configuración regional \_ use \_ CP \_ ACP**


</dt> <dd>

Usa la página de códigos ANSI del sistema para la traducción de cadenas en lugar de la página de códigos de configuración regional.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**HORA \_ NOMINUTESORSECONDS**


</dt> <dd>

No usa minutos ni segundos.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIEMPO \_ NOsegundos**


</dt> <dd>

No utiliza segundos.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**HORA \_ NOTIMEMARKER**


</dt> <dd>

No utiliza un marcador de hora.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**HORA \_ FORCE24HOURFORMAT**


</dt> <dd>

Siempre usa un formato de hora de 24 horas.

</dd> </dl> </dd> <dt>

*lpTime* \[ de\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Puntero a una estructura [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene la información de hora a la que se va a dar formato. Si este puntero es **null**, la función utiliza la hora actual del sistema local.

</dd> <dt>

*pwzFormat* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a un formato que se va a usar para formar la cadena de hora. Si *pwzFormat* es **null**, la función usa el formato de hora de la configuración regional especificada. Consulte [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) para obtener más información.

</dd> <dt>

*pwzTimeStr* \[ enuncia\]
</dt> <dd>

Tipo: **LPWStr**

Puntero a un búfer que recibe la cadena de hora con formato.

</dd> <dt>

*cchTime* \[ de\]
</dt> <dd>

Tipo: **int**

Tamaño, en caracteres, del búfer *pwzTimeStr* . Si *cchTime* es cero, la función devuelve el número de caracteres necesarios para contener la cadena de tiempo con formato y no se utiliza el búfer al que apunta *pwzTimeStr* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se ejecuta correctamente, el valor devuelto es el número de caracteres que se escriben en el búfer al que apunta *pwzTimeStr*. Si el parámetro *cchTime* es cero, el valor devuelto es el número de caracteres necesarios para contener la cadena de hora con formato. El recuento incluye el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** puede devolver uno de los siguientes códigos de error.

<dl> <dt>

**ERROR \_ de \_ búfer insuficiente**
</dt> <dt>

**ERROR de \_ marcas no válidas \_**
</dt> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> </dl>

## <a name="remarks"></a>Observaciones

**GetTimeFormatWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **GetTimeFormatWrapW** directamente desde Shlwapi.dll, mediante el ordinal 310.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
