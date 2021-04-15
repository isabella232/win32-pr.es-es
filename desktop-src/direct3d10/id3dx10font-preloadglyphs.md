---
description: Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font::P método reloadGlyphs (D3DX10. h)
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
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707894"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font::P método reloadGlyphs

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

Los glifos no se representarán en el dispositivo; ID3DX10Font: se debe llamar a:D rawText para representar los glifos. Sin embargo, al precargar los glifos en la memoria de vídeo, ID3DX10Font::D rawText usarán prácticamente menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
