---
description: Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Función D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718401"
---
# <a name="d3dxcomputenormalmap-function"></a>D3DXComputeNormalMap función)

Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de destino.

</dd> <dt>

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de mapa de alto de origen.

</dd> <dt>

*pSrcPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a un tipo [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene la paleta de origen de 256 colores o **null**.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Una o varias marcas de [ \_ NORMALMAP de D3DX](d3dx-normalmap.md) que controlan la generación de asignaciones normales.

</dd> <dt>

*Canal* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Una marca de [ \_ canal de D3DX](d3dx-channel.md) que especifica el origen de la información de alto.

</dd> <dt>

*Amplitud* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Multiplicador de valor constante que aumenta (o reduce) los valores del mapa normal. Los valores más altos normalmente hacen que los golpes sean más visibles, los valores más bajos normalmente hacen que los golpes sean menos visibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método calcula el normal mediante el uso de la diferencia central con el tamaño del kernel 3x3. El denominador de diferencia central usado es 2,0. Los canales RGB del destino contienen componentes sesgados (x, y, z) de la normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
