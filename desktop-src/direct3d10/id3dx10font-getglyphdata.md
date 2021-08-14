---
description: Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: Método ID3DX10Font::GetGlyphData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302895"
---
# <a name="id3dx10fontgetglyphdata-method"></a>Método ID3DX10Font::GetGlyphData

Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Glifo* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de glifo.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Dirección de un puntero a un objeto ID3D10Texture que contiene el glifo.

</dd> <dt>

*pBlackBox* \[ En\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo. Vea [RECT](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ En\]
</dt> <dd>

Tipo: **\* POINT**

Puntero al vector bidimensional que conecta el origen de la celda de caracteres actual con el origen de la celda de caracteres siguiente. Vea [POINT](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

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

 

 
