---
description: Establece las distancias mínima y máxima de intersección entre objetos 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: Método ID3DXPRTEngine::SetMinMaxIntersection (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2182714588e5d408c6928a677433e68dac44f09abf5ec6bd4cb4d6df7e4acf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629065"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>Método ID3DXPRTEngine::SetMinMaxIntersection

Establece las distancias mínima y máxima de intersección entre objetos 3D. Estos valores de distancia se pueden usar para controlar la distancia mínima o máxima que los objetos pueden sombrar o reflejar la luz. Por ejemplo, el método se puede usar para limitar el sombreado de características cercanas de un modelo 3D.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fMin* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distancia de intersección mínima. Debe ser positivo y menor que fMax.

</dd> <dt>

*fMax* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distancia de intersección máxima. Si es 0,0f, se usará el valor anterior; de lo contrario, debe ser mayor que fMin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método no se puede usar en simulaciones de transferencia de radiancia precalutadas (PRT) que se ejecutan en la GPU. Vea [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
