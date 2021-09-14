---
description: Cree un efecto a partir de una descripción de efecto ASCII o binario. Esta función es una versión extendida de D3DXCreateEffectFromFile que permite a una aplicación controlar qué parámetros omite el sistema de efectos.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Función D3DXCreateEffectFromFileEx (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970876"
---
# <a name="d3dxcreateeffectfromfileex-function"></a>Función D3DXCreateEffectFromFileEx

Cree un efecto a partir de una descripción de efecto ASCII o binario. Esta función es una versión extendida de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite a una aplicación controlar qué parámetros omite el sistema de efectos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
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

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero al nombre de archivo. Este parámetro admite cadenas Unicode y ANSI. Vea la sección Comentarios.

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matriz opcional terminada en NULL de definiciones de macro de preprocesador. Vea [**D3DXMACRO.**](d3dxmacro.md)

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

Si *pSrcFile contiene* un efecto de texto, las marcas pueden ser una combinación de marcas [D3DXSHADER](d3dxshader-flags.md) y [marcas D3DXFX;](d3dxfx.md) De lo contrario, *pSrcFile* contiene un efecto binario y las únicas marcas respetadas son las marcas D3DXFX. El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.

</dd> <dt>

*pPool* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntero a un [**objeto ID3DXEffectPool**](id3dxeffectpool.md) que se usará para los parámetros compartidos. Si este valor es **NULL,** no se compartirá ningún parámetro.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Devuelve un puntero a un búfer que contiene el efecto compilado. Vea [**ID3DXEffect**](id3dxeffect.md).

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un puntero a un búfer que contiene una lista de errores de compilación. Vea [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función es una versión extendida de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación. El sistema de efectos omite una constante administrada por la aplicación. Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que corresponda.

Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:

-   Está enlazado a un registro constante.
-   Solo se usa en el código del sombreador HLSL.

Si se denomina una constante en la cadena que no está presente en el efecto, se omite.

Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos LPCTSTR se resuelve en LPCSTR.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXCreateEffectFromFileW. De lo contrario, la llamada de función se resuelve en D3DXCreateEffectFromFileA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
