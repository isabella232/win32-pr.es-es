---
description: Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font:: GetGlyphData (método) (D3DX10. h)'
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
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707995"
---
# <a name="id3dx10fontgetglyphdata-method"></a>ID3DX10Font:: GetGlyphData (método)

Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.

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

*Glifo* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador del glifo.

</dd> <dt>

*ppTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Dirección de un puntero a un objeto ID3D10Texture que contiene el glifo.

</dd> <dt>

*pBlackBox* \[ de\]
</dt> <dd>

Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Puntero al objeto de rectángulo más pequeño que incluye completamente el glifo. Vea [Rect](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ de\]
</dt> <dd>

Tipo: **Point \***

Puntero al vector bidimensional que conecta el origen de la celda de carácter actual con el origen de la celda de carácter siguiente. Vea [Point](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

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

 

 
