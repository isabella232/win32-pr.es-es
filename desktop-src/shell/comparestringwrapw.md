---
description: Compara dos cadenas de caracteres Unicode mediante una configuración regional especificada.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Función CompareStringWrapW
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
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861516"
---
# <a name="comparestringwrapw-function"></a>Función CompareStringWrapW

\[**CompareStringWrapW** está disponible para su uso en Windows XP. No estará disponible en versiones posteriores. Debe usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) en su lugar.\]

Compara dos cadenas de caracteres Unicode mediante una configuración regional especificada.

> [!Note]  
> **CompareStringWrapW es** un contenedor para la **función CompareStringW.** Consulte la [**página CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) para obtener más notas de uso.

 

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

*Configuración regional* \[ En\]
</dt> <dd>

Tipo: **LCID**

Identificador de configuración regional usado para la comparación. Este parámetro puede ser uno de los siguientes identificadores de configuración regional predefinidos o un identificador de configuración regional creado por la macro [**MAKELCID.**](/windows/win32/api/winnt/nf-winnt-makelcid)

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA**


</dt> <dd>

Configuración regional predeterminada del sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO**


</dt> <dd>

Configuración regional predeterminada del usuario actual.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Marcas que indican cómo compara la función las dos cadenas. De forma predeterminada, estas marcas no están establecidas. Establezca en cero para obtener el comportamiento predeterminado o en cualquier combinación de los valores siguientes.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM \_ IGNORECASE**


</dt> <dd>

Omitir mayúsculas y minúsculas.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM \_ IGNOREKANATYPE**


</dt> <dd>

No diferencie entre los caracteres Hiragana y Katakana. Los caracteres Hiragana y Katakana correspondientes se comparan como iguales.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM \_ IGNORENONSPACE**


</dt> <dd>

Pasar por alto los caracteres que no son de espacio.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM \_ IGNORESYMBOLS**


</dt> <dd>

Omitir símbolos.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM \_ IGNOREWIDTH**


</dt> <dd>

No diferencie entre un carácter de un solo byte y el mismo carácter que un carácter de doble byte.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT \_ STRINGSORT**


</dt> <dd>

Trate los signos de puntuación igual que los símbolos.

</dd> </dl> </dd> <dt>

*lpString1* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la primera cadena Unicode que se va a comparar.

</dd> <dt>

*cchCount1* \[ En\]
</dt> <dd>

Tipo: **int**

Número de caracteres de la cadena a los que apunta el *parámetro lpString1.* El recuento no incluye el carácter nulo de terminación. Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.

</dd> <dt>

*lpString2* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la segunda cadena Unicode que se va a comparar.

</dd> <dt>

*cchCount2* \[ En\]
</dt> <dd>

Tipo: **int**

Número de caracteres de la cadena a los que apunta el *parámetro lpString2.* El recuento no incluye el carácter nulo de terminación. Si este parámetro es un valor negativo, se supone que la cadena termina en NULL y la longitud se calcula automáticamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError puede** devolver uno de los siguientes códigos de error.

-   ERROR \_ MARCAS NO \_ VÁLIDAS
-   ERROR \_ PARÁMETRO NO \_ VÁLIDO

Si la función se realiza correctamente, el valor devuelto es uno de los siguientes valores. 

| Requisito | Valor |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ MENOR \_ QUE    | La cadena a la que apunta el parámetro *lpString1* tiene menos valor léxico que la cadena a la que apunta *el parámetro lpString2.* |
| CSTR \_ EQUAL         | La cadena a la que *apunta lpString1 es* igual en valor léxico a la cadena a la que *apunta lpString2.*                              |
| CSTR \_ MAYOR \_ QUE | La cadena a la que *apunta lpString1* es mayor en valor léxico que la cadena a la que *apunta lpString2*                           |



 

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso incorrecto de esta función puede poner en peligro la seguridad de la aplicación. Las cadenas que no se comparan correctamente pueden generar entradas no válidas. Pruebe las cadenas para asegurarse de que son válidas antes de usarlos y proporcione controladores de errores. Para obtener más información, vea [Security Considerations: International Features (Consideraciones de seguridad: características internacionales).](../intl/security-considerations--international-features.md)

El método preferido es usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a CompareStringWrapW** directamente desde Shlwapi.dll, mediante ordinal 45.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
