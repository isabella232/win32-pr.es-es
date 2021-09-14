---
description: Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: Método ID3DXFont::GetGlyphData (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060607"
---
# <a name="id3dxfontgetglyphdata-method"></a>Método ID3DXFont::GetGlyphData

Devuelve información sobre la colocación y orientación de un glifo en una celda de caracteres.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
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

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Dirección de un puntero a [**un objeto IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contiene el glifo.

</dd> <dt>

*pBlackBox* \[ out\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo.

</dd> <dt>

*pCellInc* \[ out\]
</dt> <dd>

Tipo: **[ **POINT**](../winprog/windows-data-types.md)\***

Puntero al vector bidimensional que conecta el origen de la celda de caracteres actual con el origen de la celda de caracteres siguiente. Vea [**POINT**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
