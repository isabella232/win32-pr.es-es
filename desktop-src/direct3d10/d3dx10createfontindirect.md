---
description: Crea un objeto Font. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar DirectWrite y la biblioteca DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Función D3DX10CreateFontIndirect (D3DX10Core. h)
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
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362496"
---
# <a name="d3dx10createfontindirect-function"></a>D3DX10CreateFontIndirect función)

Crea un objeto Font.

> [!Note]  
> En lugar de usar esta función, se recomienda usar [DirectWrite](../directwrite/direct-write-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.

 

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero a una interfaz de [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

</dd> <dt>

*pDesc* \[ de\]
</dt> <dd>

Tipo: **const [**D3DX10 \_ \_ Descripción**](d3dx10-font-desc.md) \*** de la fuente

Puntero a una estructura de [**\_ \_ DESC de fuente D3DX10**](d3dx10-font-desc.md) , que describe los atributos del objeto de fuente que se va a crear. Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontIndirectW. De lo contrario, la llamada de función se resuelve como D3DXCreateFontIndirectA porque se usan cadenas ANSI.

</dd> <dt>

*ppFont* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Devuelve un puntero a una [**interfaz ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
