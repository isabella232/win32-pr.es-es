---
description: Compara dos cadenas de caracteres Unicode con una configuración regional especificada.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984351"
---
# <a name="comparestringwrapw-function"></a>CompareStringWrapW función)

\[**CompareStringWrapW** está disponible para su uso en Windows XP. No estará disponible en las versiones posteriores. Debe usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) en su lugar.\]

Compara dos cadenas de caracteres Unicode con una configuración regional especificada.

> [!Note]  
> **CompareStringWrapW** es un contenedor para la función **CompareStringW** . Vea la página [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ de\]
</dt> <dd>

Tipo: **LCID**

Identificador de configuración regional que se usa para la comparación. Este parámetro puede ser uno de los siguientes identificadores de configuración regional predefinidos o un identificador de configuración regional creado por la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**configuración \_ predeterminada del sistema local \_**


</dt> <dd>

La configuración regional predeterminada del sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_valor predeterminado del usuario de configuración regional \_**


</dt> <dd>

Configuración regional predeterminada del usuario actual.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Marcas que indican cómo la función compara las dos cadenas. De forma predeterminada, no se establecen estas marcas. Establezca en cero para obtener el comportamiento predeterminado o en cualquier combinación de los valores siguientes.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORMA \_ IGNORECASE**


</dt> <dd>

Omitir mayúsculas y minúsculas.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORMA \_ IGNOREKANATYPE**


</dt> <dd>

No diferencie entre caracteres hiragana y katakana. Los caracteres hiragana y katakana correspondientes se comparan como iguales.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORMA \_ IGNORENONSPACE**


</dt> <dd>

Omitir caracteres que no sean de espacio.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORMA \_ IGNORESYMBOLS**


</dt> <dd>

Omitir símbolos.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORMA \_ IGNOREWIDTH**


</dt> <dd>

No diferencie entre un carácter de un solo byte y el mismo carácter que un carácter de doble byte.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**ORDENAR \_ STRINGSORT**


</dt> <dd>

Trate los signos de puntuación iguales que los símbolos.

</dd> </dl> </dd> <dt>

*lpString1* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la primera cadena Unicode que se va a comparar.

</dd> <dt>

*cchCount1* \[ de\]
</dt> <dd>

Tipo: **int**

Número de caracteres de la cadena a la que apunta el parámetro *lpString1* . El recuento no incluye el carácter nulo de terminación. Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.

</dd> <dt>

*lpString2* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la segunda cadena Unicode que se va a comparar.

</dd> <dt>

*cchCount2* \[ de\]
</dt> <dd>

Tipo: **int**

Número de caracteres de la cadena a la que apunta el parámetro *lpString2* . El recuento no incluye el carácter nulo de terminación. Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** puede devolver uno de los siguientes códigos de error.

-   ERROR de \_ marcas no válidas \_
-   ERROR \_ de \_ parámetro no válido

Si la función se ejecuta correctamente, el valor devuelto es uno de los valores siguientes. 

| Requisito | Value |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ menor \_ que    | La cadena a la que apunta el parámetro *lpString1* es menos en el valor léxico que la cadena a la que apunta el parámetro *lpString2* . |
| CSTR \_ igual         | La cadena a la que apunta *lpString1* tiene el mismo valor léxico que la cadena a la que apunta *lpString2*.                              |
| CSTR \_ mayor \_ que | La cadena a la que apunta *lpString1* es mayor en el valor léxico que la cadena a la que apunta *lpString2*                           |



 

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de esta función puede poner en peligro la seguridad de la aplicación. Las cadenas que no se comparan correctamente pueden generar entradas no válidas. Pruebe las cadenas para asegurarse de que son válidas antes de utilizarlas y proporcionar controladores de errores. Para obtener más información, vea [consideraciones de seguridad: características internacionales](../intl/security-considerations--international-features.md)

El método preferido es usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **CompareStringWrapW** directamente desde Shlwapi.dll, mediante el ordinal 45.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
