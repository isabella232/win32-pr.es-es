---
description: El operador de concatenación + = une los caracteres al final de esta cadena. El operador acepta otro objeto CHString, un puntero de carácter o un carácter único.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716211"
---
# <a name="chstringoperator"></a>CHString:: Operator + =

\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El operador de concatenación + = une los caracteres al final de esta cadena. El operador acepta otro objeto [**CHString**](chstring.md) , un puntero de carácter o un carácter único.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*String@*
</dt> <dd>

Una cadena [**CHString**](chstring.md) que se concatena con esta cadena.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Cam*
</dt> <dd>

Carácter que se va a concatenar con esta cadena.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntero a una cadena terminada en **null** que se va a concatenar con esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que se pueden producir excepciones de memoria cada vez que utilice este operador de concatenación porque se puede asignar un nuevo almacenamiento para los caracteres agregados a este objeto [**CHString**](chstring.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de **CHString:: Operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
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

 

