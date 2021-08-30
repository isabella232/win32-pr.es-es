---
description: Cargue una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: Método ID3DX10Font::P reloadCharacters (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a6c0ac515457aee430dea7cc3f785ed2832aed5c566f84b9d4ee262ba8b5cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953575"
---
# <a name="id3dx10fontpreloadcharacters-method"></a>Método ID3DX10Font::P reloadCharacters

Cargue una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*En primer lugar* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del primer carácter que se va a cargar en la memoria de vídeo.

</dd> <dt>

*Último* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador del último carácter que se va a cargar en la memoria de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Este método genera texturas que contienen glifos que representan los caracteres de entrada. Los glifos se dibujan como una serie de triángulos.

Los caracteres no se representarán en el dispositivo; Todavía se debe llamar a ID3DX10Font::D rawText para representar los caracteres. Sin embargo, al cargar previamente caracteres en la memoria de vídeo, ID3DX10Font::D rawText usará muchos menos recursos de CPU.

Este método convierte internamente caracteres en glifos mediante la función GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
