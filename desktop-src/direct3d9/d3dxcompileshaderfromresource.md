---
description: 'Función D3DXCompileShaderFromResource: compila un archivo de sombreador.'
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: Función D3DXCompileShaderFromResource (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de94754004cc42bcc6914d9513588a71a1a593dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115813"
---
# <a name="d3dxcompileshaderfromresource-function"></a>Función D3DXCompileShaderFromResource

Compile un archivo de sombreador.

> [!Note]  
> En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos Fxc.exe o usar la API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
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

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre del recurso.

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

*pFunctionName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a la función de punto de entrada del sombreador donde comienza la ejecución.

</dd> <dt>

*pProfile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador. Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.

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

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Devuelve una [**interfaz ID3DXConstantTable,**](id3dxconstanttable.md) que se puede usar para tener acceso a las constantes del sombreador. Este valor puede ser **NULL.** Si compila la aplicación como una dirección grande (es decir, usa la opción del vinculador /LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede usar este parámetro y debe establecerlo en **NULL.** En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla shader-constant incrustada dentro del sombreador. En esta **llamada a D3DXGetShaderConstantTableEx,** debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar el acceso a hasta 4 GB de espacio de direcciones virtuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

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

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
