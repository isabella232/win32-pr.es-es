---
description: 'Función D3DXAssembleShaderFromFile: ensamblar un sombreador.'
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Función D3DXAssembleShaderFromFile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91aaf2924638b1db5b0e8ec0782b90fa964a9543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116033"
---
# <a name="d3dxassembleshaderfromfile-function"></a>Función D3DXAssembleShaderFromFile

Ensamblar un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matriz **terminada en NULL** opcional de estructuras [**D3DXMACRO.**](d3dxmacro.md) Este valor puede ser **NULL.**

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include. Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas. El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene el sombreador creado. Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación. Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración. Este valor puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXAssembleShaderFromFileW. De lo contrario, la llamada de función se resuelve en D3DXAssembleShaderFromFileA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
