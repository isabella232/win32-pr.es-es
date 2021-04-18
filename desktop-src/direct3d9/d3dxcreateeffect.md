---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Función D3DXCreateEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721473"
---
# <a name="d3dxcreateeffect-function"></a>D3DXCreateEffect función)

Cree un efecto a partir de una descripción de efectos ASCII o binarios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo que va a crear el efecto. Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene una descripción de efecto.

</dd> <dt>

*SrcDataLen* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Longitud de los datos del efecto, en bytes.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador. Este valor puede ser **null**.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include. Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Si *pSrcData* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcData* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX. El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.

</dd> <dt>

*pPool* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos. Si este valor es **null**, no se compartirá ningún parámetro.

</dd> <dt>

*ppEffect* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Devuelve un puntero a una interfaz [**ID3DXEffect**](id3dxeffect.md) .

</dd> <dt>

*ppCompilationErrors* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores de compilación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
