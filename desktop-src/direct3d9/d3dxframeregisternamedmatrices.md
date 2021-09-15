---
description: Dada una jerarquía de fotogramas, registra todas las matrices con nombre en el mezclador de animación.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Función D3DXFrameRegisterNamedMatrices (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567925"
---
# <a name="d3dxframeregisternamedmatrices-function"></a>Función D3DXFrameRegisterNamedMatrices

Dada una jerarquía de fotogramas, registra todas las matrices con nombre en el mezclador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrameRoot* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Nodo de nivel superior de la jerarquía de fotogramas.

</dd> <dt>

*pAnimController* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Puntero al objeto de controlador de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




