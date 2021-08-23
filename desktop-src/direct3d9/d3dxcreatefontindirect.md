---
description: Crea indirectamente un objeto de fuente para un dispositivo y una fuente.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Función D3DXCreateFontIndirect (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 555c4b1f3615639d9da01fb7a2a96aa5cb15f697235c918d5130ffcd4d43baa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988665"
---
# <a name="d3dxcreatefontindirect-function"></a>Función D3DXCreateFontIndirect

Crea indirectamente un objeto de fuente para un dispositivo y una fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el dispositivo que se va a asociar al objeto de fuente.

</dd> <dt>

*pDesc* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Puntero a una [**estructura D3DXFONT \_ DESC,**](d3dxfont-desc.md) que describe los atributos del objeto de fuente que se creará. Si la configuración del compilador requiere Unicode, el tipo de datos D3DXFONT DESC se resuelve como D3DXFONT DESCW; de lo contrario, el tipo de datos se resuelve como \_ \_ D3DXFONT \_ DESCA. Vea la sección Comentarios.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Devuelve un puntero a una [**interfaz ID3DXFont,**](id3dxfont.md) que representa el objeto de fuente creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateFontIndirectW. De lo contrario, la llamada de función se resuelve en D3DXCreateFontIndirectA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
