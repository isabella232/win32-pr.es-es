---
description: Calcula la esfera de límite de todas las mallas de la jerarquía de fotogramas.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Función D3DXFrameCalculateBoundingSphere (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a8a4706fcbd421072e2b82cd9e228fe24c35651c17ce4ab0f48e05b946946fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123221"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>Función D3DXFrameCalculateBoundingSphere

Calcula la esfera de límite de todas las mallas de la jerarquía de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrameRoot* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Puntero al nodo raíz.

</dd> <dt>

*pObjectCenter* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Devuelve el centro de la esfera de límite.

</dd> <dt>

*pObjectRadius* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Devuelve el radio de la esfera de límite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
