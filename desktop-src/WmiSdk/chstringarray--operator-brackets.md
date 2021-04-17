---
description: Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado. Estos operadores son un sustituto práctico de los métodos SetAt y GetAd.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray:: Operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716767"
---
# <a name="chstringarrayoperator--"></a>CHStringArray:: Operator \[\]

\[La clase [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado. Estos operadores son un sustituto práctico de los métodos [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) y [**GetAd**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .

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

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*
</dt> <dd>

Índice entero que es mayor o igual que cero y menor o igual que el valor devuelto por [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Los operadores de subíndice devuelven el elemento de puntero [**CHString**](chstring.md) actualmente en este índice.

## <a name="remarks"></a>Observaciones

Puede usar el primer operador, que llama a las matrices que no son **const**, tanto en la parte derecha (r-value) como en el lado izquierdo (valor l) de una instrucción de asignación. La segunda, que llama a las matrices **const** , solo se puede usar a la derecha.

La versión de depuración de la biblioteca valida si el subíndice (ya sea en el lado izquierdo o derecho de una instrucción de asignación) está fuera de los límites.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el uso de [**CHStringArray \[ \] :: Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


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
| Encabezado<br/>                   | <dl> <dt>ChStrArr. h (incluye FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHStringArray:: Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray:: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

