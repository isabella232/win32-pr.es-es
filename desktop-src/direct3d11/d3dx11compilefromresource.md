---
title: Función D3DX11CompileFromResource (D3DX11async.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación HLSL, como la API D3DCompile. Compile un sombreador o un efecto a partir de un recurso.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- Función D3DX11CompileFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060861"
---
# <a name="d3dx11compilefromresource-function"></a>Función D3DX11CompileFromResource

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación HLSL, como la API [**D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile) [](/windows/desktop/menurc/resources-functions)

 

Compile un sombreador o un efecto a partir de un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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

*hSrcModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Identificador del módulo de recursos que contiene el sombreador. HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del recurso que contiene el sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pSrcFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Opcional. Nombre de archivo de efecto, que solo se usa para los mensajes de error. Puede ser **NULL.**

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Opcional. Puntero a una matriz de definiciones de macro (vea [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0. Si no se usa, establezca *pDefines* en **NULL.**

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Opcional. Puntero a una interfaz para controlar archivos de incluyen. Si se establece en **NULL,** se producirá un error de compilación si un sombreador contiene una \# include.

</dd> <dt>

*pFunctionName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de la función de punto de entrada del sombreador donde comienza la ejecución del sombreador. Al compilar un efecto, **D3DX11CompileFromResource** omite *pFunctionName*; Se recomienda establecer *pFunctionName* en **NULL** porque es una buena práctica de programación establecer un parámetro de puntero en **NULL** si la función llamada no lo usará.

</dd> <dt>

*pProfile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5. El perfil también puede ser para el tipo de efecto (por ejemplo, fx \_ 4 \_ 1).

</dd> <dt>

*Marcas1* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Marcas [**de compilación de sombreador**](/windows/desktop/direct3dhlsl/d3dcompile-constants).

</dd> <dt>

*Marcas2* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Marcas [**de compilación de efecto**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Al compilar un sombreador y no un archivo de efecto, **D3DX11CompileFromResource** omite *Flags2*; Se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no sea de punto de referencia en cero si la función llamada no lo usará.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Use **NULL** para especificar que esta función no debe devolverse hasta que se complete.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria que contiene el sombreador compilado, así como cualquier información incrustada de depuración y tabla de símbolos.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria que contiene una lista de errores y advertencias que se produjeron durante la compilación. Estos errores y advertencias son idénticos a la salida de depuración de un depurador.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

**D3DX11CompileFromResource** devuelve E INVALIDARG si se proporciona un valor null distinto de NULL al parámetro pHResult al proporcionar NULL al \_ parámetro *pPump.*    Para obtener más información sobre esta situación, vea Comentarios.

## <a name="remarks"></a>Observaciones

Para obtener más información **sobre D3DX11CompileFromResource**, vea [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Debe proporcionar **NULL al** parámetro *pHResult* si también proporciona **NULL** al *parámetro pPump.* De lo contrario, no se puede crear posteriormente un sombreador mediante el código de sombreador compilado que **D3DX11CompileFromResource** devuelve en la memoria a la que apunta *el parámetro ppShader.* Para crear un sombreador a partir de código de sombreador compatible, llame a uno de los métodos de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) siguientes:

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Además, si proporciona un valor distinto de **NULL** a *pHResult* al proporcionar **NULL** a *pPump,* **D3DX11CompileFromResource** devuelve el código de error E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

