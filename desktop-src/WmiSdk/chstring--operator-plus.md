---
description: El operador de concatenación + combina dos cadenas y devuelve un objeto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815982"
---
# <a name="chstringoperator"></a>CHString:: Operator +

\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El operador de concatenación + combina dos cadenas y devuelve un objeto [**CHString**](chstring.md) .

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, Str1, str2*
</dt> <dd>

Cadenas [**CHString**](chstring.md) que se concatenan.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Cam*
</dt> <dd>

Carácter que se concatena con una cadena o una cadena que se concatena con un carácter.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntero a una cadena de caracteres terminada en **null**.

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Este operador de concatenación devuelve un objeto [**CHString**](chstring.md) que es el resultado temporal de la concatenación. Este valor devuelto permite combinar varias concatenaciones en la misma expresión.

## <a name="remarks"></a>Observaciones

Una de las dos cadenas de argumentos debe ser un objeto [**CHString**](chstring.md) ; el otro puede ser un puntero de carácter o un carácter. Tenga en cuenta que pueden producirse excepciones de memoria cada vez que se usa el operador de concatenación, ya que se puede asignar un nuevo almacenamiento para almacenar datos temporales.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el uso de **CHString:: Operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>ChString. h (incluye FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

