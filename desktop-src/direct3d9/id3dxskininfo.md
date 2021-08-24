---
description: Las aplicaciones usan los métodos de la interfaz ID3DXSkinInfo para manipular matrices de póricos, que se usan para la máscara de datos de vértices para la animación. Esta interfaz ya no está estrictamente vinculada a ID3DXMesh y se puede usar para desenmascarar cualquier conjunto de datos de vértices.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interfaz ID3DXSkinInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727765"
---
# <a name="id3dxskininfo-interface"></a>Interfaz ID3DXSkinInfo

Las aplicaciones usan los métodos de la interfaz ID3DXSkinInfo para manipular matrices de póricos, que se usan para la máscara de datos de vértices para la animación. Esta interfaz ya no está estrictamente vinculada a [**ID3DXMesh**](id3dxmesh.md) y se puede usar para desenmascarar cualquier conjunto de datos de vértices.

## <a name="members"></a>Miembros

La **interfaz ID3DXSkinInfo** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSkinInfo también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXSkinInfo tiene** estos métodos.



| Método                                                                              | Descripción                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](id3dxskininfo--clone.md)                                               | Clona un objeto de información de máscara.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de triángulos. En la tabla se describe qué esqueletos afectan a qué subconjuntos de la malla.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice, índices y una tabla de combinación de teclas. En la tabla se describe qué paletas de paletas afectan a qué subconjuntos de la malla.<br/> |
| [**FindVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Recupera el índice de la influencia del pórmico que afecta a un solo vértice.<br/>                                                                                                                |
| [**GetIqueInfluence**](id3dxskininfo--getboneinfluence.md)                         | Obtiene los vértices y pesos que influye en un pórtico.<br/>                                                                                                                               |
| [**GetName**](id3dxskininfo--getbonename.md)                                   | Obtiene el nombre del pie, del índice de la columna.<br/>                                                                                                                                            |
| [**GetIonalOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Obtiene la matriz de desplazamiento de desplazamiento de desplazamiento de desplazamiento de desplazamiento.<br/>                                                                                                                                                        |
| [**GetVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Recupera el factor de mezcla y el vértice afectados por una influencia de póralo especificada.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Obtiene la declaración de vértice.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Obtiene el valor fijo del vértice de la función.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Obtiene las influencias máximas de la cara en una malla de triángulo con el búfer de índice especificado.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Obtiene el número máximo de influencias para cualquier vértice de la malla.<br/>                                                                                                                   |
| [**GetMinIonalInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Obtiene la influencia mínima del pórmo. Los valores de influencia menores que se omiten.<br/>                                                                                                    |
| [**GetNumIonalInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Obtiene el número de influencias para un pánseo.<br/>                                                                                                                                           |
| [**GetNumNumNums**](id3dxskininfo--getnumbones.md)                                   | Obtiene el número de esqueletos.<br/>                                                                                                                                                           |
| [**Remap**](id3dxskininfo--remap.md)                                               | Actualiza la información de influencia de los aires para que coincidan con los vértices después de reordenarlos. Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.<br/>              |
| [**SetIonalInfluence**](id3dxskininfo--setboneinfluence.md)                         | Establece el valor de influencia de un póreo.<br/>                                                                                                                                                |
| [**SetName**](id3dxskininfo--setbonename.md)                                   | Establece el nombre de la columna.<br/>                                                                                                                                                                 |
| [**SetOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Establece la matriz de desplazamiento de desplazamiento de desplazamiento de desplazamiento de desplazamiento.<br/>                                                                                                                                                        |
| [**SetVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Establece un valor de influencia de un triángulo en un solo vértice.<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | Establece la declaración de vértice.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Establece el tipo de formato de vértice flexible (FVF).<br/>                                                                                                                                         |
| [**SetMinIonalInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Establece la influencia mínima de los depósitos. Los valores de influencia menores que se omiten.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Aplica el desnasado de software a los vértices de destino en función de las matrices actuales.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Cree una **interfaz ID3DXSkinInfo** con [**D3DXCreateSkinInfo,**](d3dxcreateskininfo.md) [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)o [**D3DXCreateSkinInfoFVF.**](d3dxcreateskininfofvf.md)

El tipo LPD3DXSKININFO se define como un puntero a la **interfaz ID3DXSkinInfo.**


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
