---
description: 'Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h): carga la identidad en la matriz actual.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663559db0746b9d689066e537c1473f467341cbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565924"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)

Carga la identidad en la matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto \[ los coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 4,4, que se establecen en \] \[ \] 1,0. La matriz de identidad es especial en que, cuando se aplica a los vértices, no se modifican. La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de vértice para crear rotaciones, traducciones y cualquier otra transformación que se pueda representar mediante una matriz de 4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




