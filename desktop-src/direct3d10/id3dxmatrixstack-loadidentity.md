---
description: 'Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h): carga la identidad en la matriz actual.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107993"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)

Carga la identidad en la matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto \[ los coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 4,4, que se establecen en \] \[ \] 1,0. La matriz de identidad es especial en que, cuando se aplica a los vértices, no se modifican. La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de vértice para crear rotaciones, traducciones y cualquier otra transformación que se pueda representar mediante una matriz de 4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




