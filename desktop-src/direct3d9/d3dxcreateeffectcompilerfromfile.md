---
description: 'Función D3DXCreateEffectCompilerFromFile: crea un compilador de efectos a partir de una descripción de efecto ASCII.'
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Función D3DXCreateEffectCompilerFromFile (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087983"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a>Función D3DXCreateEffectCompilerFromFile

Crea un compilador de efectos a partir de una descripción de efecto ASCII.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero al nombre de archivo. Este parámetro admite cadenas Unicode y ANSI. Vea la sección Comentarios.

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

*Flags* \[in\]
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

## <a name="remarks"></a>Comentarios

Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos LPCTSTR se resuelve en LPCSTR.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXCreateEffectCompilerFromFileW. De lo contrario, la llamada de función se resuelve en D3DXCreateEffectCompilerFromFileA porque se usan cadenas ANSI.

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

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
