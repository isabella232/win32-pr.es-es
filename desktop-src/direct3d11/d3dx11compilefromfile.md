---
title: Función D3DX11CompileFromFile (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API D3DCompileFromFile. Compilar un sombreador o un efecto desde un archivo.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Función D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157220"
---
# <a name="d3dx11compilefromfile-function"></a>D3DX11CompileFromFile función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .

 

Compilar un sombreador o un efecto desde un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del archivo que contiene el código del sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Tipo: **[**D3D10 de \_ sombreador \_ const**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Opcional. Puntero a una matriz de definiciones de macro (vea [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0. Si no se usa, establezca *pDefines* en **null**.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Puntero a una interfaz para controlar archivos de inclusión. Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.

</dd> <dt>

*pFunctionName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador. Al compilar un efecto, **D3DX11CompileFromFile** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que especifica el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5. El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Marcas de [**compilación**](/windows/desktop/direct3dhlsl/d3dcompile-constants)del sombreador.

</dd> <dt>

*Flags2* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Marcas de compilación**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efectos. Al compilar un sombreador y no un archivo de efectos, **D3DX11CompileFromFile** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.

</dd> <dt>

*pPump* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)). Use **null** para especificar que esta función no debe devolver hasta que se complete.

</dd> <dt>

*ppShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria que contiene el sombreador compilado, así como cualquier información de depuración incrustada y de tabla de símbolos.

</dd> <dt>

*ppErrorMsgs* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria que contiene una lista de errores y advertencias que se produjeron durante la compilación. Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.

</dd> <dt>

*pHResult* \[ enuncia\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**. Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromFile** devuelve E \_ INVALIDARG si proporciona un valor distinto de **null** al parámetro *pHResult* cuando se proporciona **null** al parámetro *pPump* . Para obtener más información sobre esta situación, consulte la sección Comentarios.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre **D3DX11CompileFromFile**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Debe proporcionar un **valor null** al parámetro *pHResult* si también proporciona **null** al parámetro *pPump* . De lo contrario, no se puede crear un sombreador mediante el código del sombreador compilado que **D3DX11CompileFromFile** devuelve en la memoria a la que apunta el parámetro *ppShader* . Para crear un sombreador a partir del código de sombreador compatible, llame a uno de los siguientes métodos de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Además, si se proporciona un valor distinto de **null** a *pHResult* cuando se proporciona **null** a *pPump*, **D3DX11CompileFromFile** devuelve el código de \_ error E INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

