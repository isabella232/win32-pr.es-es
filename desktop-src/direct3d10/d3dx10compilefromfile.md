---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API D3DCompile. Compilar un sombreador o un efecto desde un archivo.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: Función D3DX10CompileFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718441"
---
# <a name="d3dx10compilefromfile-function"></a>D3DX10CompileFromFile función)

> [!Note]  
> En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

Compilar un sombreador o un efecto desde un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D_SHADER_MACRO *pDefines,
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

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nombre del archivo que contiene el código del sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const

Opcional. Puntero a una matriz de definiciones de macro (vea la [**\_ \_ macro del sombreador de D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0. Si no se usa, establezca *pDefines* en **null**.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Puntero a una interfaz de [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para administrar archivos de inclusión. Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.

</dd> <dt>

*pFunctionName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador. Al compilar un efecto, **D3DX10CompileFromFile** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador [2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), el [modelo de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o el [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).

</dd> <dt>

*Flags1* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Marcas de compilación del sombreador](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md). Al compilar un sombreador y no un archivo de efectos, **D3DX10CompileFromFile** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.

</dd> <dt>

*pPump* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **null** para especificar que esta función no debe devolver hasta que se complete.

</dd> <dt>

*ppShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene el sombreador compilado, así como cualquier información de depuración y de tabla de símbolos incrustada.

</dd> <dt>

*ppErrorMsgs* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Un puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene una lista de errores y advertencias que se produjeron durante la compilación. Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.

</dd> <dt>

*pHResult* \[ enuncia\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**. Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
