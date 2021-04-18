---
description: Cree un procesador de datos asincrónicos para un efecto.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: Función D3DX10CreateAsyncEffectCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718280"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a>D3DX10CreateAsyncEffectCompilerProcessor función)

Cree un procesador de datos asincrónicos para un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
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

Cadena que contiene el nombre de archivo del efecto.

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

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Opciones de compilación de HLSL](d3d10-graphics-reference-effect-constants.md).

</dd> <dt>

*FXFlags* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Opciones de compilación de efectos](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*ppCompiledShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero a búfer (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el efecto compilado.

</dd> <dt>

*ppErrorBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero a un búfer (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene errores de compilación.

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

 

 
