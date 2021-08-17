---
description: Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: Método ID3DX10Font::P reloadGlyphs (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540341"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>Método ID3DX10Font::P reloadGlyphs

Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*En primer lugar* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del primer glifo que se va a cargar en la memoria de vídeo.

</dd> <dt>

*Último* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del último glifo que se va a cargar en la memoria de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Este método genera texturas que contienen los glifos de entrada. Los glifos se dibujan como una serie de triángulos.

Los glifos no se representarán en el dispositivo; Todavía se debe llamar a ID3DX10Font::D rawText para representar los glifos. Sin embargo, al cargar previamente glifos en la memoria de vídeo, ID3DX10Font::D rawText usará muchos menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
