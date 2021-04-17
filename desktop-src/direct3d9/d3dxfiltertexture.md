---
description: Filtra los niveles de mipmap de una textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Función D3DXFilterTexture (D3dx9tex. h)
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
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718211"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture función)

Filtra los niveles de mipmap de una textura.

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

*pBaseTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntero a una interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa el objeto de textura que se va a filtrar.

</dd> <dt>

*pPalette* \[ enuncia\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null** para los formatos nonpalettized. Si no se especifica una paleta, se proporciona la paleta de Direct3D predeterminada (una paleta blanca opaca). Vea la sección Comentarios.

</dd> <dt>

*SrcLevel* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nivel cuya imagen se usa para generar los niveles posteriores. Especificar \_ el valor predeterminado de D3DX para este parámetro equivale a especificar 0.

</dd> <dt>

*MipFilter* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra el mipmap. Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el cuadro de filtro de d3dx \_ \_ si el tamaño de la textura es una potencia de dos y la interpolación de filtros de d3dx del \_ cuadro de filtro de \_ \| d3dx \_ \_ en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Un filtro se aplica de forma recursiva a cada nivel de textura para generar el siguiente nivel de textura.

La escritura en una superficie sin nivel cero de la textura no hará que se actualice el rectángulo sucio. Si se llama a **D3DXFilterTexture** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la textura.

Las texturas creadas en el grupo predeterminado ( \_ valor predeterminado de D3DPOOL) no se pueden usar con **D3DXFilterTexture** (a menos que se cree con D3DUSAGE \_ Dynamic) porque se necesita una operación de bloqueo en el objeto. Tenga en cuenta que los bloqueos están prohibidos en las texturas en el grupo predeterminado (a menos que sean dinámicos).

Para obtener más información sobre [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vea el SDK de la plataforma. Tenga en cuenta que, a partir de DirectX 8,0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de la plataforma. El miembro peFlags es ahora el canal alfa para formatos de paleta de 8 bits.

Solo hay una función de filtrado de texturas, pero dos macros que llaman a este método.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
