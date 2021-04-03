---
description: Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: ID3DXFont::P método reloadGlyphs (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083802"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont::P método reloadGlyphs

Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Primero* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

IDENTIFICADOR del primer glifo que se va a cargar en la memoria de vídeo.

</dd> <dt>

*Última* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

IDENTIFICADOR del último glifo que se va a cargar en la memoria de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Este método genera texturas que contienen los glifos de entrada. Los glifos se dibujan como una serie de triángulos.

Los glifos no se representarán en el dispositivo; También se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar los glifos. Sin embargo, al precargar los glifos en la memoria de vídeo, **DrawText** usará prácticamente menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
