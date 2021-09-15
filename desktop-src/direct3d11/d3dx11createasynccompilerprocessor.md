---
title: Función D3DX11CreateAsyncCompilerProcessor (D3DX11async.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios. Cree un procesador de datos asincrónicos para un sombreador.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Función D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566300"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>Función D3DX11CreateAsyncCompilerProcessor

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios.

 

Cree un procesador de datos asincrónicos para un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que contiene el nombre de archivo del sombreador.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const D3D11 \_ SHADER \_ MACRO \***

Matriz terminada en NULL de macros de sombreador; establezca esta opción **en NULL** para no especificar macros.

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntero a una interfaz include. Este parámetro puede ser **NULL**.

</dd> <dt>

*pFunctionName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de la función de punto de entrada del sombreador donde comienza la ejecución del sombreador. Al compilar un efecto, **D3DX11CreateAsyncCompilerProcessor** omite *pFunctionName*; Se recomienda establecer *pFunctionName* en **NULL** porque es una buena práctica de programación establecer un parámetro de puntero en **NULL** si la función a la que se llama no lo usará.

</dd> <dt>

*pProfile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que especifica el perfil de sombreador o el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5. El perfil también puede ser para el tipo de efecto (por ejemplo, fx \_ 4 \_ 1).

</dd> <dt>

*Marcas1* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Marcas de compilación del sombreador.

</dd> <dt>

*Marcas2* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Marcas de compilación de efecto. Al compilar un sombreador y no un archivo de efecto, **D3DX11CreateAsyncCompilerProcessor** omite *Flags2*; Se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no sea de punto de referencia en cero si la función llamada no lo usará.

</dd> <dt>

*ppCompiledShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero al efecto compilado.

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero para compilar errores.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

Para Windows Store, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica de Windows Runtime [**(AsyncBase).**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))

En el caso de las aplicaciones de escritorio Win32, puede usar el Runtime de simultaneidad [para](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementar algo similar al modelo de programación asincrónica de Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

