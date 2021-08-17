---
description: Esta tabla asigna miembros de una declaración D3DVERTEXELEMENT9 a un código FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Asignación entre una declaración de Direct3D y códigos FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35d28653eba57e99987fb67910f1bec87f4d5bd001fc6f3f6b0e25d65264c55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728431"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Asignación entre una declaración de Direct3D y códigos FVF (Direct3D 9)

Esta tabla asigna miembros de una [**declaración D3DVERTEXELEMENT9**](d3dvertexelement9.md) a un código FVF.



| Tipo de datos             | Uso                      | Índice de uso | Fvf                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ POSITION     | 0           | D3DFVF \_ XYZ               |
| D3DDECLTYPE \_ FLOAT4   | D3DDECLUSAGE \_ POSITIONT    | 0           | D3DFVF \_ XYZRHW            |
| D3DDECLTYPE \_ FLOATn   | D3DDECLUSAGE \_ BLENDWEIGHT  | 0           | D3DFVF \_ XYZBn             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ BLENDINDICES | 0           | D3DFVF \_ XYZB (nWeights+1) |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ NORMAL       | 0           | D3DFVF \_ NORMAL            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ PSIZE        | 0           | D3DFVF \_ PSIZE             |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ COLOR        | 0           | D3DFVF \_ DIFUSO           |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ COLOR        | 1           | D3DFVF \_ SPECULAR          |
| D3DDECLTYPE \_ FLOATm   | D3DDECLUSAGE \_ TEXCOORD     | n           | D3DFVF \_ TEXCOORDSIZEm(n)  |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ POSITION     | 1           | N/D                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ NORMAL       | 1           | N/D                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 



