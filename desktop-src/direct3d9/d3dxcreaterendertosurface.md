---
description: Crea una superficie de representación.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Función D3DXCreateRenderToSurface (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 632225dcad44324f88d8c126eb3f74d7779ff5ec698581514717dc1e0c54d3f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988635"
---
# <a name="d3dxcreaterendertosurface-function"></a>Función D3DXCreateRenderToSurface

Crea una superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el dispositivo que se va a asociar a la superficie de representación.

</dd> <dt>

*Ancho* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho de la superficie de representación, en píxeles.

</dd> <dt>

*Alto* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Alto de la superficie de representación, en píxeles.

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel de la superficie de representación.

</dd> <dt>

*Galería de detalles* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** la superficie de representación admite una superficie de galería de símbolos de profundidad. De lo contrario, este miembro se establece en **FALSE.** Esta función creará un nuevo búfer de profundidad.

</dd> <dt>

*DepthStencilFormat* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Si *DepthStencil* se establece en **TRUE,** este parámetro es un miembro del tipo enumerado [D3DFORMAT,](d3dformat.md) que describe el formato de galería de símbolos de profundidad de la superficie de representación.

</dd> <dt>

*ppRenderToSurface* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Dirección de un puntero a una [**interfaz ID3DXRenderToSurface,**](id3dxrendertosurface.md) que representa la superficie de representación creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
