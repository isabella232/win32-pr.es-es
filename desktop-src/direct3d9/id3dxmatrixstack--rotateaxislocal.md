---
description: 'Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h): gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e46aa8767506aaabfcff6107ad184fad6dd8166097fbde955ac068f8f934ca22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629485"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)

Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero al eje arbitrario de rotación. Vea [**D3DXVECTOR3.**](d3dxvector3.md)

</dd> <dt>

*Ángulo* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ángulo de rotación sobre el eje arbitrario, en radianes. Los ángulos se miden en sentido contrario a las agujas del reloj al mirar a lo largo del eje arbitrario hacia el origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método agrega la rotación a la pila de matriz con la matriz de rotación calculada similar a la siguiente:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Dado que la rotación se multiplica a la izquierda en la pila de matriz, la rotación es relativa al espacio de coordenadas local del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
