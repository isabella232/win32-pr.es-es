---
description: Las aplicaciones usan los métodos de la interfaz ID3DXSkinInfo para manipular matrices de hueso, que se usan para enmascarar los datos de vértices para la animación. Esta interfaz ya no está estrictamente ligada a ID3DXMesh y se puede usar para enmascarar cualquier conjunto de datos de vértice.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interfaz ID3DXSkinInfo (D3DX9Mesh. h)
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
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717687"
---
# <a name="id3dxskininfo-interface"></a>Interfaz ID3DXSkinInfo

Las aplicaciones usan los métodos de la interfaz ID3DXSkinInfo para manipular matrices de hueso, que se usan para enmascarar los datos de vértices para la animación. Esta interfaz ya no está estrictamente ligada a [**ID3DXMesh**](id3dxmesh.md) y se puede usar para enmascarar cualquier conjunto de datos de vértice.

## <a name="members"></a>Miembros

La interfaz **ID3DXSkinInfo** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSkinInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXSkinInfo** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](id3dxskininfo--clone.md)                                               | Clona un objeto de información de máscara.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de hueso. En la tabla se describen los huesos que afectan a los subconjuntos de la malla.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Toma una malla y devuelve una nueva malla con pesos de fusión, índices y una tabla de combinación de hueso por vértices. En la tabla se describen las paletas de hueso que afectan a los subconjuntos de la malla.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Recupera el índice de la influencia del hueso que afecta a un solo vértice.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Obtiene los vértices y pesos que un hueso influye.<br/>                                                                                                                               |
| [**GetBoneName**](id3dxskininfo--getbonename.md)                                   | Obtiene el nombre del hueso, del índice del hueso.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Obtiene la matriz de desplazamiento del hueso.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Recupera el factor de mezcla y el vértice afectados por una influencia del hueso especificada.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Obtiene la declaración de vértice.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Obtiene el valor de vértice de función fijo.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Obtiene el número máximo de influencias de caras en una malla de triángulo con el búfer de índice especificado.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Obtiene el número máximo de influencias para cualquier vértice de la malla.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Obtiene la influencia mínima del hueso. Los valores de influencia más pequeños se omiten.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Obtiene el número de influencias de un hueso.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Obtiene el número de huesos.<br/>                                                                                                                                                           |
| [**Mapeo**](id3dxskininfo--remap.md)                                               | Actualiza la información de influencia del hueso para que coincida con los vértices después de reordenar. Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Establece el valor de influencia de un hueso.<br/>                                                                                                                                                |
| [**SetBoneName**](id3dxskininfo--setbonename.md)                                   | Establece el nombre del hueso.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Establece la matriz de desplazamiento del hueso.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Establece un valor de influencia de un hueso en un solo vértice.<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | Establece la declaración de vértices.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Establece el tipo de formato de vértice flexible (FVF).<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Establece la influencia mínima del hueso. Los valores de influencia más pequeños se omiten.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Aplica los aspectos de software a los vértices de destino en función de las matrices actuales.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Cree una interfaz **ID3DXSkinInfo** con [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)o [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

El tipo LPD3DXSKININFO se define como un puntero a la interfaz **ID3DXSkinInfo** .


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
