---
description: Crea un mapa de entorno de representación.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Función D3DXCreateRenderToEnvMap (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575232"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>Función D3DXCreateRenderToEnvMap

Crea un mapa de entorno de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que es el dispositivo que se va a asociar a la superficie de representación.

</dd> <dt>

*Tamaño* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño de la superficie de representación.

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles de asignación mip.

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT](d3dformat.md) que describe el formato de píxel del mapa de entorno.

</dd> <dt>

*Galería de detalles* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** la superficie de representación admite una superficie de galería de símbolos de profundidad. De lo contrario, este miembro se establece en **FALSE.**

</dd> <dt>

*DepthStencilFormat* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Si DepthStencil se establece en **TRUE,** este parámetro es un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) que describe el formato de galería de símbolos de profundidad del mapa de entorno.

</dd> <dt>

*ppRenderToEnvMap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Dirección de un puntero a una [**interfaz ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) que representa el mapa de entorno de representación creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[De uso general functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
