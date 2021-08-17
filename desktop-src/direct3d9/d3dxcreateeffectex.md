---
description: Crea un efecto a partir de una descripción de efecto ASCII o binario. Esta función es una versión extendida de D3DXCreateEffect que permite a una aplicación controlar qué parámetros omite el sistema de efectos.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Función D3DXCreateEffectEx (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19321dde9f44a2262ee3875d40bd5822e65eff9b84d1fc01656993ea584a8dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988655"
---
# <a name="d3dxcreateeffectex-function"></a>Función D3DXCreateEffectEx

Crea un efecto a partir de una descripción de efecto ASCII o binario. Esta función es una versión extendida de [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite a una aplicación controlar qué parámetros omite el sistema de efectos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo que creará el efecto. Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene una descripción del efecto.

</dd> <dt>

*SrcDataLen* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Longitud de los datos del efecto, en bytes.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen definiciones de preprocesador. Este valor puede ser **NULL.**

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include. Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.

</dd> <dt>

*pSkipConstants* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena de parámetros de efecto que el sistema de efectos omitirá. La cadena debe terminar **en NULL** y debe contener el nombre de cada constante administrada por la aplicación separada por un punto y coma.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Si *pSrcData contiene* un efecto de texto, flags puede ser una combinación de marcas [D3DXSHADER](d3dxshader-flags.md) y [marcas D3DXFX;](d3dxfx.md) De lo contrario, *pSrcData* contiene un efecto binario y las únicas marcas respetadas son las marcas D3DXFX. El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.

</dd> <dt>

*pPool* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntero a un [**objeto ID3DXEffectPool**](id3dxeffectpool.md) que se usará para los parámetros compartidos. Si este valor es **NULL,** no se compartirá ningún parámetro.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Devuelve un puntero a una [**interfaz ID3DXEffect.**](id3dxeffect.md)

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores de compilación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función es una versión extendida de [**D3DXCreateEffect**](d3dxcreateeffect.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación. El sistema de efectos omite una constante administrada por la aplicación. Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que sea necesario.

Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:

-   Está enlazado a un registro constante.
-   Solo se usa en el código del sombreador HLSL.

Si una constante se denomina en la cadena que no está presente en el efecto, se omite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
