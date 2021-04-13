---
description: ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los huesos y los vértices de las mallas (consulte la animación del esqueleto en Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interfaz ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362585"
---
# <a name="id3dx10skininfo-interface"></a>Interfaz ID3DX10SkinInfo

ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los huesos y los vértices de las mallas (consulte la [animación del esqueleto en Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). Es más útil para hacer que los archivos. x exportados por las aplicaciones de DCC (por ejemplo, 3DS Max y Maya) sean más fáciles de utilizar para el hardware y para mejorar la velocidad de representación de las mallas estratificadas en el modo de representación de software.

## <a name="members"></a>Miembros

La interfaz **ID3DX10SkinInfo** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10SkinInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10SkinInfo** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddBoneInfluences**](id3dx10skininfo-addboneinfluences.md)           | Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.<br/>     |
| [**AddBones**](id3dx10skininfo-addbones.md)                             | Asigne espacio para más huesos.<br/>                                                                                          |
| [**AddVertices**](id3dx10skininfo-addvertices.md)                       | Asigne espacio para los vértices adicionales.<br/>                                                                                 |
| [**ClearBoneInfluences**](id3dx10skininfo-clearboneinfluences.md)       | Borre la lista de vértices de un hueso a los que influye.<br/>                                                                     |
| [**Compacto**](id3dx10skininfo-compact.md)                               | Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | Realice la piel de software en una matriz de vértices.<br/>                                                                           |
| [**FindBoneInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influida de un hueso determinado.<br/>                    |
| [**GetBoneInfluence**](id3dx10skininfo-getboneinfluence.md)             | Obtiene la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.<br/>                                                       |
| [**GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | Obtiene el número de vértices a los que afecta un hueso determinado.<br/>                                                                |
| [**GetBoneInfluences**](id3dx10skininfo-getboneinfluences.md)           | Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.<br/> |
| [**GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Obtiene el número de vértices a los que puede afectar máximamente el hueso.<br/>                                                              |
| [**GetNumBones**](id3dx10skininfo-getnumbones.md)                       | Obtiene el número de huesos en ID3DX10SkinInfo.<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | Obtiene el número de vértices en ID3DX10SkinInfo.<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | Cambiar los huesos influyen en los vértices.<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | Cambiar los vértices afectados por los huesos.<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | Quitar un hueso.<br/>                                                                                                          |
| [**SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md)             | Establece la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

Cree una interfaz ID3DX10SkinInfo con [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** o **D3DX10CreateSkinInfoFVF**.

El tipo LPD3DX10SKININFO se define como un puntero a la interfaz **ID3DX10SkinInfo** .


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
