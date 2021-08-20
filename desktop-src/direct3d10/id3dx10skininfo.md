---
description: ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los animales y los vértices de las mallas (consulte Animación de esqueletos en Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interfaz ID3DX10SkinInfo (D3DX10.h)
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
ms.openlocfilehash: 49ddcd4eba2f99a18992ce9b63cb4af5c93bfe7f7e40cf5fc7b1fe9003de281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100244"
---
# <a name="id3dx10skininfo-interface"></a>Interfaz ID3DX10SkinInfo

ID3DX10SkinInfo le permite optimizar, procesar y establecer manualmente la relación entre los animales y los vértices de las mallas (consulte Animación de esqueletos en [Wikipedia).](https://en.wikipedia.org/wiki/Skeletal_animation) Resulta muy útil para hacer que los archivos .x exportados por las aplicaciones DCC (como 3DS Max y Maya) sea más fácil de usar en el hardware y para mejorar la velocidad de representación de las mallas con máscara en el modo de representación de software.

## <a name="members"></a>Miembros

La **interfaz ID3DX10SkinInfo** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10SkinInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10SkinInfo** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddIonalInfluences**](id3dx10skininfo-addboneinfluences.md)           | Habilite un tejido existente para influir en un grupo de vértices y definir cuánta influencia tiene el pórtico en cada vértice.<br/>     |
| [**AddBones**](id3dx10skininfo-addbones.md)                             | Asigne espacio para más espacios.<br/>                                                                                          |
| [**AddVertices**](id3dx10skininfo-addvertices.md)                       | Asigne espacio para vértices adicionales.<br/>                                                                                 |
| [**ClearIonalInfluences**](id3dx10skininfo-clearboneinfluences.md)       | Borrar la lista de vértices de un borde que influye.<br/>                                                                     |
| [**Compacto**](id3dx10skininfo-compact.md)                               | Limitar el número de vértices que pueden influir en un vértice o limitar la cantidad de influencia que puede tener un póreo en un vértice.<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | Realice el desnasado de software en una matriz de vértices.<br/>                                                                           |
| [**FindIonalInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influenciados de un ángulo determinado.<br/>                    |
| [**GetIonalInfluence**](id3dx10skininfo-getboneinfluence.md)             | Obtiene la cantidad de influencia que tiene un ángulo determinado sobre un vértice determinado.<br/>                                                       |
| [**GetIonalInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | Obtiene el número de vértices que influye en un dado.<br/>                                                                |
| [**GetIonalInfluences**](id3dx10skininfo-getboneinfluences.md)           | Obtenga una lista de vértices en los que influye un ángulo determinado y una lista de la cantidad de influencia que tiene el pórtico en cada vértice.<br/> |
| [**GetMaxIonalInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Obtiene el número de vértices que un pórtico puede influir al máximo.<br/>                                                              |
| [**GetNumIonals**](id3dx10skininfo-getnumbones.md)                       | Obtenga el número de esqueletos en ID3DX10SkinInfo.<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | Obtenga el número de vértices en ID3DX10SkinInfo.<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | Cambiar qué influencia tienen los vértices.<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | Cambiar los vértices que se ven influenciados por los pórticos.<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | Quite un póreo.<br/>                                                                                                          |
| [**SetIonalInfluence**](id3dx10skininfo-setboneinfluence.md)             | Establezca la cantidad de influencia que tiene un ángulo determinado sobre un vértice determinado.<br/>                                                       |



 

## <a name="remarks"></a>Comentarios

Cree una interfaz ID3DX10SkinInfo con [**D3DX10CreateSkinInfo,**](d3d10-d3dx10createskininfo.md) **D3DX10CreateSkinInfoFromBlendedMesh** o **D3DX10CreateSkinInfoFVF.**

El tipo LPD3DX10SKININFO se define como un puntero a la **interfaz ID3DX10SkinInfo.**


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
