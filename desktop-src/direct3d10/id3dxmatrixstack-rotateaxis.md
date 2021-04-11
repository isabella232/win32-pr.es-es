---
description: Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'ID3DXMATRIXStack:: RotateAxis (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362799"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a>ID3DXMATRIXStack:: RotateAxis (método) (D3DX10. h)

Gira (respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero al eje arbitrario de rotación. Vea [**D3DXVECTOR3**](d3d10-d3dxvector3.md).

</dd> <dt>

*Ángulo* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ángulo de giro alrededor del eje arbitrario, en radianes. Los ángulos se miden en sentido contrario a las agujas del reloj al mirar el eje arbitrario hacia el origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método agrega la rotación a la pila de la matriz con la matriz de rotación calculada similar a la siguiente:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Dado que la rotación se multiplica a la derecha en la pila de la matriz, la rotación es relativa al espacio de coordenadas universal.

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

 

 
