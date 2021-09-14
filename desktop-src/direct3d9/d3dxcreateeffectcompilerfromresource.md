---
description: Crea un ID3DXEffectCompiler a partir de una descripción de efecto ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Función D3DXCreateEffectCompilerFromResource (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970887"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a>Función D3DXCreateEffectCompilerFromResource

Crea un [**ID3DXEffectCompiler a partir de**](id3dxeffectcompiler.md) una descripción de efecto ASCII.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador de un módulo que contiene la descripción del efecto. Si este parámetro es **NULL,** se usará el módulo actual.

</dd> <dt>

*pSrcResource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero al recurso. Este parámetro admite cadenas Unicode y ANSI. Vea la sección Comentarios.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen definiciones de preprocesador. Este valor puede ser **NULL.**

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include. Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas (vea [D3DXSHADER Flags](d3dxshader-flags.md)). El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.

</dd> <dt>

*ppEffectCompiler* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Dirección de un puntero a una [**interfaz ID3DXEffectCompiler,**](id3dxeffectcompiler.md) que contiene el compilador de efectos.

</dd> <dt>

*ppParseErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer,**](id3dxbuffer.md) que contiene los mensajes de error que se produjeron durante la compilación. Este parámetro se puede establecer en **NULL para** omitir los mensajes de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateEffectCompilerFromResourceW. De lo contrario, la llamada de función se resuelve en D3DXCreateEffectCompilerFromResourceA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
