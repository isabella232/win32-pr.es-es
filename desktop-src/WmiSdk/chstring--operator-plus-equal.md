---
description: El operador de concatenación += une caracteres al final de esta cadena. El operador acepta otro objeto CHString, un puntero de carácter o un solo carácter.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: CHString::operator+= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316f5272c7b5a4ef5b59e93dd480ade215e3279ea754f1da5432448d46fcce17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679885"
---
# <a name="chstringoperator"></a>CHString::operator+=

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El operador de concatenación += une caracteres al final de esta cadena. El operador acepta otro [**objeto CHString,**](chstring.md) un puntero de carácter o un solo carácter.

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

<span id="string"></span><span id="STRING"></span>*Cadena*
</dt> <dd>

Cadena [**CHString**](chstring.md) que se concatena con esta cadena.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Carácter que se va a concatenar a esta cadena.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntero a una **cadena terminada** en NULL para concatenar a esta cadena.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que se pueden producir excepciones de memoria cada vez que use este operador de concatenación, ya que se puede asignar nuevo almacenamiento para los caracteres agregados a este [**objeto CHString.**](chstring.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el **uso de CHString::operator +=**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

