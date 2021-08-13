---
description: Las coordenadas de textura en Direct3D pueden incluir uno, dos, tres o cuatro elementos de punto flotante para direccionar texturas con distintos niveles de dimensión.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formatos de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519888"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Formatos de coordenadas de textura (Direct3D 9)

Las coordenadas de textura en Direct3D pueden incluir uno, dos, tres o cuatro elementos de punto flotante para direccionar texturas con distintos niveles de dimensión. Una textura 1D, una superficie de textura con dimensiones de 1 por n elementos de textura, se dirige mediante una coordenada de textura. El caso más común, las texturas 2D, se abordan con dos coordenadas de textura que normalmente se denominan you y v. Direct3D admite dos tipos de texturas 3D, mapas de entorno cúbica y texturas de volumen. Los mapas de entornos cúbicas no son realmente 3D, pero se abordan con un vector de tres elementos. Para más información, consulte [Asignación de entorno cúbica (Direct3D 9).](cubic-environment-mapping.md)

Como se describe en Códigos FVF de función fija [(Direct3D 9),](fixed-function-fvf-codes.md)las aplicaciones codifican coordenadas de textura en formato de vértice. El formato de vértice puede incluir varios conjuntos de coordenadas de textura. Use D3DFVF \_ TEX0 a D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) para describir un formato de vértice que no incluye coordenadas de textura o hasta ocho conjuntos.

Cada conjunto de coordenadas de textura puede tener entre uno y cuatro elementos. Las marcas \_ TEXTUREFORMAT1 a D3DFVF TEXTUREFORMAT4 de D3DFVF describen el número de elementos de una coordenada de textura en un conjunto, pero estas marcas no las usan \_ ellos mismos. En su lugar, el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa estas marcas para crear patrones de bits que describen el número de elementos usados por un conjunto determinado de coordenadas de textura en el formato de vértice. Estas macros aceptan un único parámetro que identifica el índice del conjunto de coordenadas cuyo número de elementos se está definindo. En el ejemplo siguiente se muestra cómo se usan estas macros.


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> A excepción de los mapas de entorno cúbica y las texturas de volumen, los rasterizadores no pueden dirigir las texturas utilizando más de dos elementos. Las aplicaciones pueden proporcionar hasta tres elementos para una coordenada de textura, pero solo si la textura es un mapa de cubo, una textura de volumen o se usa la marca de transformación de textura PROJECTED de D3DTTFF. \_ La marca D3DTTFF PROJECTED hace que el rasterizador divida los dos primeros elementos por el \_ tercer elemento (o n). Para obtener más información, vea [Transformaciones de coordenadas de textura (Direct3D 9).](texture-coordinate-transformations.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 



