---
description: El operador + concatenation une dos cadenas y devuelve un objeto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: CHString::operator+ (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ce52e8740fcd420600aaebb192c23ab7269c4ddf14c068a4980c59df3e7773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097355"
---
# <a name="chstringoperator"></a>CHString::operator+

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El operador + concatenation une dos cadenas y devuelve un [**objeto CHString.**](chstring.md)

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

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*
</dt> <dd>

[**Cadenas CHString**](chstring.md) que se concatenan.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Carácter que se concatena con una cadena o una cadena que se concatena con un carácter.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntero a una cadena de caracteres terminada en **NULL.**

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Este operador de concatenación devuelve [**un objeto CHString**](chstring.md) que es el resultado temporal de la concatenación. Este valor devuelto permite combinar varias concatenaciones en la misma expresión.

## <a name="remarks"></a>Comentarios

Una de las dos cadenas de argumento debe ser un [**objeto CHString;**](chstring.md) el otro puede ser un puntero de carácter o un carácter. Tenga en cuenta que se pueden producir excepciones de memoria cada vez que use el operador de concatenación, ya que se puede asignar nuevo almacenamiento para contener datos temporales.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el **uso de CHString::operator +**:


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
| Header<br/>                   | <dl> <dt>ChString.h (include FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

