---
description: Nota En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos Fxc.exe o usar la API D3DCompile. Compile un sombreador o un efecto que se cargue en memoria.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Función D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5cd6772079f872fe575a3a2f49fee536b89dab00f29a62dba151842dbc99b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281715"
---
# <a name="d3dx10compilefrommemory-function"></a>Función D3DX10CompileFromMemory

> [!Note]  
> En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos Fxc.exe o usar la API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

Compile un sombreador o un efecto que se cargue en memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al sombreador en memoria.

</dd> <dt>

*SrcDataLen* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamaño del sombreador en memoria.

</dd> <dt>

*pFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del archivo que contiene el código del sombreador.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Opcional. Puntero a una matriz de definiciones de macro (vea [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0. Si no se usa, establezca *pDefines* en **NULL.**

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Puntero a una [**interfaz ID3D10Incluir interfaz**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para controlar archivos de incluyen. Si se establece en **NULL,** se producirá un error de compilación si un sombreador contiene una \# include.

</dd> <dt>

*pFunctionName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la función de punto de entrada del sombreador donde comienza la ejecución del sombreador. Al compilar un efecto, **D3DX10CompileFromMemory** omite *pFunctionName*; Se recomienda establecer *pFunctionName* en **NULL** porque es una buena práctica de programación establecer un parámetro de puntero en **NULL** si la función llamada no lo usará.

</dd> <dt>

*pProfile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo [de sombreador 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md)el modelo [de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o el [modelo de sombreador 4.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)

</dd> <dt>

*Marcas1* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Marcas de compilación de sombreador](d3d10-shader.md).

</dd> <dt>

*Marcas2* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Marcas de compilación de efecto](d3d10-graphics-reference-effect-constants.md). Al compilar un sombreador y no un archivo de efecto, **D3DX10CompileFromMemory** omite *Flags2*; Se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no sea de punto de referencia en cero si la función llamada no lo usará.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Use **NULL** para especificar que esta función no debe devolverse hasta que se complete.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a una interfaz [**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene el sombreador compilado, así como cualquier información incrustada de depuración y tabla de símbolos.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene una lista de errores y advertencias que se produjeron durante la compilación. Estos errores y advertencias son idénticos a la salida de depuración de un depurador.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
