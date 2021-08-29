---
description: 'Método ID3DXMATRIXStack::RotateYawPitchRoll (D3dx9math.h): gira (con respecto al espacio de coordenadas universal) alrededor de un eje arbitrario.'
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: Método ID3DXMATRIXStack::RotateYawPitchRoll (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d054c125f5db545067b3fd105e7c27d7857cd5c1388a18b29ed0e4175c999f0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987215"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::RotateYawPitchRoll (D3dx9math.h)

Gira (en relación con el espacio de coordenadas universal) alrededor de un eje arbitrario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Yaw* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

La yaw alrededor del eje Y en radianes.

</dd> <dt>

*Pitch* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

El tono alrededor del eje X en radianes.

</dd> <dt>

*Roll* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

La rotación alrededor del eje Z en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Comentarios

Este método agrega la rotación a la pila de matriz con la matriz de rotación calculada similar a la siguiente:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Dado que la rotación se multiplica a la derecha en la pila de matriz, la rotación es relativa al espacio de coordenadas universal.

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

[**ID3DXMATRIXStack::RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
