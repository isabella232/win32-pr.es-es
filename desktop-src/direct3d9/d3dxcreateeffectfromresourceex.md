---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios. Se trata de una versión extendida de D3DXCreateEffectFromResource que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Función D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718397"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a>D3DXCreateEffectFromResourceEx función)

Cree un efecto a partir de una descripción de efectos ASCII o binarios. Se trata de una versión extendida de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite a una aplicación controlar qué parámetros se omiten en el sistema de efectos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al dispositivo.

</dd> <dt>

*hSrcModule* \[ de\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador de un módulo que contiene la descripción del efecto. Si este parámetro es **null**, se usará el módulo actual.

</dd> <dt>

*pSrcResource* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero al recurso. Este parámetro admite cadenas Unicode y ANSI. Vea la sección Comentarios.

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

*pSkipConstants* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Una cadena de parámetros de efecto que el sistema de efectos omitirá. La cadena debe terminar en **null** y debe contener el nombre de cada constante administrada por la aplicación separada por un punto y coma.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Si *pSrcResource* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcResource* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX. El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.

</dd> <dt>

*pPool* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos. Si este valor es **null**, no se compartirá ningún parámetro.

</dd> <dt>

*ppEffect* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Devuelve un búfer que contiene el efecto compilado.

</dd> <dt>

*ppCompilationErrors* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores de compilación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función es una versión extendida de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) que permite a una aplicación especificar qué constantes de efecto administrará la aplicación. El sistema de efectos omite una constante administrada por la aplicación. Es decir, la aplicación es responsable de inicializar la constante, así como de guardar y restaurar su estado siempre que sea necesario.

Esta función comprueba cada constante de pSkipConstants para ver lo siguiente:

-   Está enlazado a un registro constante.
-   Solo se usa en el código del sombreador HLSL.

Si se asigna un nombre a una constante en la cadena que no está presente en el efecto, se omite.

Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectFromResourceW. De lo contrario, la llamada de función se resuelve como D3DXCreateEffectFromResourceA porque se usan cadenas ANSI.

D3DXCreateEffectFromResource carga los datos de un recurso de tipo RT \_ RCDATA. Consulte MSDN para obtener más información acerca de los recursos de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de efecto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
