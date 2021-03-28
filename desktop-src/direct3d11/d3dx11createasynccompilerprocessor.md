---
title: Función D3DX11CreateAsyncCompilerProcessor (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un procesador de datos asincrónico para un sombreador.
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998563"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>D3DX11CreateAsyncCompilerProcessor función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.

 

Cree un procesador de datos asincrónico para un sombreador.

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

*pFileName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que contiene el nombre de archivo del sombreador.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Tipo: **D3D11 de \_ sombreador \_ \* const**

Una matriz terminada en NULL de macros de sombreador; Establezca este **valor en NULL** para no especificar ninguna macro.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntero a una interfaz de inclusión. Este parámetro puede ser **NULL**.

</dd> <dt>

*pFunctionName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador. Al compilar un efecto, **D3DX11CreateAsyncCompilerProcessor** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Una cadena que especifica el perfil del sombreador o el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5. El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Marcas de compilación del sombreador.

</dd> <dt>

*Flags2* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Marcas de compilación de efectos. Al compilar un sombreador y no un archivo de efectos, **D3DX11CreateAsyncCompilerProcessor** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.

</dd> <dt>

*ppCompiledShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero al efecto compilado.

</dd> <dt>

*ppErrorBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero para compilar errores.

</dd> <dt>

*ppDataProcessor* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

