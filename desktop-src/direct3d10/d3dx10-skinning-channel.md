---
description: El miembro del vértice que se decl para realizar el desnasado de software. Se usa con la API ID3DX10SkinInfo::D oSoftwareSkinning.
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
ms.openlocfilehash: b8e976ba1aecdeb792ba45fc4f60f25e7feb5a7dde3f7fc845a22962e441bf2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753535"
---
# <a name="d3dx10_skinning_channel-structure"></a>Estructura del CANAL \_ DE SKINNING de D3DX10 \_

El miembro del vértice que se decl para realizar el desnasado de software. Se usa con la API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Miembros

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

Determina qué matriz de matrices se va a usar en la API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md) Si esto es así, *se usará pInverseTransposeDivers;* de lo contrario, *se usará pDivers.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
