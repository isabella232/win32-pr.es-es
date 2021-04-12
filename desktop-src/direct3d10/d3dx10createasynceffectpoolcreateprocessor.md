---
description: Cree un procesador de datos asincrónico para un bloque de memoria.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Función D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280378"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a>D3DX10CreateAsyncEffectPoolCreateProcessor función)

Cree un procesador de datos asincrónico para un bloque de memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
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

Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.

</dd> <dt>

*pProfile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opciones de compilación de HLSL (consulte [marcas de sombreador](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*FXFlags* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.

</dd> <dt>

*ppErrorBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.

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

 

 
