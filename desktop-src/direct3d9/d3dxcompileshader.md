---
description: Compilar un archivo de sombreador.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Función D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362545"
---
# <a name="d3dxcompileshader-function"></a>D3DXCompileShader función)

Compilar un archivo de sombreador.

> [!Note]  
> En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
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

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que contiene el sombreador.

</dd> <dt>

*srcDataLen* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Longitud de los datos en bytes.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** . Este valor puede ser **null**.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include. Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.

</dd> <dt>

*pFunctionName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que contiene el nombre de la función del punto de entrada del sombreador en el que comienza la ejecución.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador. Vea [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas. El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.

</dd> <dt>

*ppShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene el sombreador creado. Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.

</dd> <dt>

*ppErrorMsgs* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación. Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración. Este valor puede ser **null**.

</dd> <dt>

*ppConstantTable* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Devuelve una interfaz [**ID3DXConstantTable**](id3dxconstanttable.md) , que se puede usar para tener acceso a las constantes de sombreador. Este valor puede ser **null**. Si compila la aplicación como compatible con direcciones grandes (es decir, usa la opción del vinculador/LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede utilizar este parámetro y debe establecerlo en **null**. En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla de constantes del sombreador que está incrustada en el sombreador. En esta llamada a **D3DXGetShaderConstantTableEx** , debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar que se tenga acceso a un máximo de 4 GB de espacio de direcciones virtuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
