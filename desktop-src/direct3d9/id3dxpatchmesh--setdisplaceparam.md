---
description: Establece los parámetros de desplazamiento de la geometría de malla.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'ID3DXPatchMesh:: SetDisplaceParam (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670246"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a>ID3DXPatchMesh:: SetDisplaceParam (método)

Establece los parámetros de desplazamiento de la geometría de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Textura* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Textura que contiene los datos de desplazamiento.

</dd> <dt>

*MinFilter* \[ de\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Nivel de minificación. Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ de\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Nivel de ampliación. Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ de\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Nivel de filtro MIP. Para obtener más información, vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Ajustar* \[ de\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**

Modo de ajuste de dirección de textura. Para obtener más información, consulte [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)

</dd> <dt>

*dwLODBias* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Nivel de valor de diferencia de detalle.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Los mapas de desplazamiento solo pueden ser texturas 2D. Mipmapping se omite para la teselación no adaptable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
