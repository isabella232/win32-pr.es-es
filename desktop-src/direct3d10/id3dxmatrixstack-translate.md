---
description: Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'ID3DXMATRIXStack:: translate (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708101"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a>ID3DXMATRIXStack:: translate (método) (D3DX10. h)

Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de traslación en la dirección x.

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de traslación en la dirección y.

</dd> <dt>

*z* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de traslación en la dirección z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Observaciones

Este método multiplica la matriz actual con la matriz de traslación calculada (la transformación es sobre el origen mundial actual).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
