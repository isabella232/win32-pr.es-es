---
description: Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado. Estos operadores son un sustituto práctico de los métodos SetAt y GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: CHStringArray::operator [ ] (ChStrArr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859cfe52535aea0fb43d6195648215431f80cff86f0525b9ef7c5247b6a831a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131777"
---
# <a name="chstringarrayoperator--"></a>CHStringArray::operator \[\]

\[La [**clase CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado. Estos operadores son un sustituto práctico de los [**métodos SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) [**y GetAt.**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*Nindex*
</dt> <dd>

Índice entero mayor o igual que cero y menor o igual que el valor devuelto por [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Los operadores de subíndice devuelven el elemento de puntero [**CHString**](chstring.md) actualmente en este índice.

## <a name="remarks"></a>Comentarios

Puede usar el primer operador , que llama a para matrices que no son **const**, en el lado derecho (r-value) o en el lado izquierdo (valor L) de una instrucción de asignación. El segundo, que llama a matrices **const,** solo se puede usar a la derecha.

La versión de depuración de la biblioteca declara si el subíndice (ya sea a la izquierda o a la derecha de una instrucción de asignación) está fuera de los límites.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el [**uso de \[ \] CHStringArray::operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChStrArr.h (include FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHStringArray::Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

