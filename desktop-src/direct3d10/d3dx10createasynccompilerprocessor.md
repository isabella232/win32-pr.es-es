---
description: Cree un procesador de datos asincrónico para un sombreador.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Función D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280281"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a>D3DX10CreateAsyncCompilerProcessor función)

Cree un procesador de datos asincrónico para un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que contiene el nombre de archivo del sombreador.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const

Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Este parámetro puede ser **NULL**.

</dd> <dt>

*pFunctionName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador. Al compilar un efecto, **D3DX10CreateAsyncCompilerProcessor** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.

</dd> <dt>

*Flags1* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Marcas de compilación del sombreador](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md). Al compilar un sombreador y no un archivo de efectos, **D3DX10CreateAsyncCompilerProcessor** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.

</dd> <dt>

*ppCompiledShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero al efecto compilado (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppErrorBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero para compilar errores (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
