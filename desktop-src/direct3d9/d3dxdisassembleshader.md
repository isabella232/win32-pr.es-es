---
description: Desensambla un sombreador.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Función D3DXDisassembleShader (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b185945098d4439753b5582a81d4d112c7984f53155e2901af8560afb404bf62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857075"
---
# <a name="d3dxdisassembleshader-function"></a>Función D3DXDisassembleShader

Desensambla un sombreador.

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API [**D3DDisassemble.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble)

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pShader* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a un búfer de memoria que contiene los datos del sombreador.

</dd> <dt>

*EnableColorCode* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Habilite el código de color para facilitar la lectura del desensamblado.

</dd> <dt>

*pComments* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena de comentario opcional terminada en NULL. Este valor puede ser **NULL.**

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene el sombreador desensamblado. Vea [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
