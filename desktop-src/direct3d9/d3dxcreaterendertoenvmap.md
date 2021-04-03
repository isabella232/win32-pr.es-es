---
description: Crea un mapa de entorno de representación.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Función D3DXCreateRenderToEnvMap (D3dx9core. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083726"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap función)

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que es el dispositivo que se va a asociar a la superficie de representación.

</dd> <dt>

*Tamaño* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño de la superficie de representación.

</dd> <dt>

*MipLevels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de niveles de mipmap.

</dd> <dt>

*Formato* \[ de\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) que describe el formato de píxel del mapa de entorno.

</dd> <dt>

*DepthStencil* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si **es true**, la superficie de representación admite una superficie de estarcido de profundidad. De lo contrario, este miembro se establece en **false**.

</dd> <dt>

*DepthStencilFormat* \[ de\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Si DepthStencil se establece en **true**, este parámetro es un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) que describe el formato de la galería de símbolos de profundidad del mapa de entorno.

</dd> <dt>

*ppRenderToEnvMap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Dirección de un puntero a una interfaz [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) que representa la asignación de entorno de representación creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
