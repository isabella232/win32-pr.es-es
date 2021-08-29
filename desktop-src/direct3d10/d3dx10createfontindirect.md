---
description: Crea un objeto de fuente. Nota En lugar de usar esta función, se recomienda usar DirectWrite y la biblioteca DirectXTK, clase SpriteFont.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Función D3DX10CreateFontIndirect (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bfbbc2cdb0e8aad5851de40312bd7d646eb9e3af22e71f0638a7fa1e52f342f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989155"
---
# <a name="d3dx10createfontindirect-function"></a>Función D3DX10CreateFontIndirect

Crea un objeto de fuente.

> [!Note]  
> En lugar de usar esta función, se recomienda usar DirectWrite [y](../directwrite/direct-write-portal.md) la biblioteca [DirectXTK,](https://github.com/Microsoft/DirectXTK) **clase SpriteFont.**

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero a una [**interfaz ID3D10Device Interface.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*pDesc* \[ En\]
</dt> <dd>

Tipo: **const [**D3DX10 \_ FONT \_ DESC**](d3dx10-font-desc.md) \***

Puntero a una [**estructura \_ \_ DESC FONT de D3DX10,**](d3dx10-font-desc.md) que describe los atributos del objeto de fuente que se creará. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateFontIndirectW. De lo contrario, la llamada de función se resuelve en D3DXCreateFontIndirectA porque se usan cadenas ANSI.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Devuelve un puntero a una [**interfaz ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
