---
description: Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont:: GetGlyphData (método) (D3dx9core. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689884"
---
# <a name="id3dxfontgetglyphdata-method"></a>ID3DXFont:: GetGlyphData (método)

Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.

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

*Glifo* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador del glifo.

</dd> <dt>

*ppTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Dirección de un puntero a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que contiene el glifo.

</dd> <dt>

*pBlackBox* \[ enuncia\]
</dt> <dd>

Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo.

</dd> <dt>

*pCellInc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **Point**](../winprog/windows-data-types.md)\***

Puntero al vector bidimensional que conecta el origen de la celda de carácter actual con el origen de la celda de carácter siguiente. Vea [**Point**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
