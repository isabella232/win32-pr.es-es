---
description: Filtra los niveles de asignación mip de una textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Función D3DXFilterTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc07336edb5f7bb8672fbbec415b0a3b312335a3a3a4b0de32aec4fdde558363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988505"
---
# <a name="d3dxfiltertexture-function"></a>Función D3DXFilterTexture

Filtra los niveles de asignación mip de una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBaseTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntero a una [**interfaz IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa el objeto de textura que se filtrará.

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores para rellenar, o **NULL** para formatos nopaleizados. Si no se especifica una paleta, se proporciona la paleta predeterminada de Direct3D (una paleta de blanco opaca). Vea la sección Comentarios.

</dd> <dt>

*SrcLevel* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel cuya imagen se usa para generar los niveles posteriores. Especificar D3DX \_ DEFAULT para este parámetro equivale a especificar 0.

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios [filtros D3DX \_ que](d3dx-filter.md) controlan cómo se filtra el mapa mip. Especificar D3DX DEFAULT para este parámetro equivale a especificar D3DX FILTER BOX si el tamaño de textura es una potencia de \_ \_ dos y \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Un filtro se aplica de forma recursiva a cada nivel de textura para generar el siguiente nivel de textura.

La escritura en una superficie que no sea de nivel cero de la textura no hará que se actualice el rectángulo desnuciado. Si se llama a **D3DXFilterTexture** y la superficie aún no estaba desasesuada (es poco probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la textura.

Las texturas creadas en el grupo predeterminado (D3DPOOL DEFAULT) no se pueden usar con \_ **D3DXFilterTexture** (a menos que se cree con D3DUSAGE DYNAMIC) porque se necesita una operación de bloqueo en el objeto \_ . Tenga en cuenta que los bloqueos están prohibidos en las texturas del grupo predeterminado (a menos que sean dinámicos).

Para más información sobre [**PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)consulte el SDK de plataforma. Tenga en cuenta que a partir de DirectX 8.0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de plataforma. El miembro peFlags es ahora el canal alfa para los formatos de 8 bits.

Solo hay una función de filtrado de textura, pero dos macros que llaman a este método.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
