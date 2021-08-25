---
description: Realiza la teselación adaptable en función del criterio de teselación adaptable basado en z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: Método ID3DXPatchMesh::TessellateAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6365cfcf50debfeeb28fd493b76ac60943ee14f27a2dadec168b3dd4d31ace1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856295"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>Método ID3DXPatchMesh::TessellateAdaptive

Realiza la teselación adaptable en función del criterio de teselación adaptable basado en z.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTrans* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Especifica un vector 4D que está punteado con los vértices para obtener la cantidad de teselación adaptable por vértice. Cada borde se tesela al valor medio de los niveles de teselación de los dos vértices a los que se conecta.

</dd> <dt>

*dwMaxTessLevel* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Límite máximo de teselación adaptable. Este es el número de vértices introducidos entre los vértices existentes. Este valor entero puede oscilar entre 1 y 32, ambos inclusive.

</dd> <dt>

*dwMinTessLevel* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Límite mínimo para teselación adaptable. Este es el número de vértices introducidos entre los vértices existentes. Este valor entero puede oscilar entre 1 y 32, ambos inclusive.

</dd> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla teselada resultante. Vea [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función funcionará de forma más eficaz si la malla de revisión se ha optimizado mediante [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
