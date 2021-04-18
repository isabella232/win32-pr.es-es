---
description: Carga la identidad en la matriz actual.
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'ID3DXMATRIXStack:: LoadIdentity (método) (D3DX10. h)'
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
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718542"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>ID3DXMATRIXStack:: LoadIdentity (método) (D3DX10. h)

Carga la identidad en la matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto los \[ \] \[ coeficientes 1, 1 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , que se establecen en 1,0. La matriz de identidad es especial, ya que, cuando se aplica a los vértices, no cambian. La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de los vértices para crear giros, traducciones y otras transformaciones que se pueden representar mediante una matriz de 4x4.

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

 

 




