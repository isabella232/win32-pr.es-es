---
description: Miembro de la decl del vértice en el que se debe realizar el desnasado de software. Se usa con la API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: D3DX10_SKINNING_CHANNEL estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566716"
---
# <a name="d3dx10_skinning_channel-structure"></a>Estructura DEL CANAL \_ DE SKINNING de D3DX10 \_

Miembro de la decl del vértice en el que se debe realizar el desnasado de software. Se usa con la API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Members

<dl> <dt>

**SrcOffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de cada vértice de origen.

</dd> <dt>

**DestOffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento desde el principio de cada vértice de destino.

</dd> <dt>

**IsNormal**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Determina qué matriz de matrices se va a usar en la API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md) Si esto es así, *se usará pInverseTransposeDivencias;* de lo contrario, se usará *pBoneMatrices.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
