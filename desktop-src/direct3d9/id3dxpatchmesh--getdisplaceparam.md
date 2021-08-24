---
description: Obtiene los parámetros de desplazamiento de geometría de malla.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: Método ID3DXPatchMesh::GetDisplaceParam (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f079e66f20bfd9b2fab673a0f8c2310a9fd85d84fe4e7d0b8c5ad59d1d61e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847455"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>Método ID3DXPatchMesh::GetDisplaceParam

Obtiene los parámetros de desplazamiento de geometría de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Textura* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Textura que contiene los datos de desplazamiento.

</dd> <dt>

*MinFilter* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Nivel de minificación. Para obtener más información, [**vea D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Nivel de ampliación. Para obtener más información, [**vea D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Nivel de filtro mip. Para obtener más información, [**vea D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Encapsulado* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Modo de encapsulado de direcciones de textura. Para obtener más información, [**vea D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*dwLODBias* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Nivel de valor de sesgo de detalle.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Los mapas de desplazamiento solo pueden ser texturas 2D. Mipmapping se omite para la teselación no pornóptica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
