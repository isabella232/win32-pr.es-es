---
description: Construye patrones de bits que se usan para identificar formatos de coordenadas de textura dentro de una descripción de FVF. Los resultados de estas macros se pueden combinar dentro de una descripción de FVF mediante el operador OR.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060744"
---
# <a name="d3dfvf_texcoordsizen"></a>D3DFVF \_ TEXCOORDSIZEN

Construye patrones de bits que se usan para identificar formatos de coordenadas de textura dentro de una descripción de FVF. Los resultados de estas macros se pueden combinar dentro de una descripción de FVF mediante el operador OR.

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a>Parámetros



| Parámetro                                                                                                    | Descripción                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex<br/> | Valor que identifica el conjunto de coordenadas de textura al que se aplica el tamaño de la coordenada de textura (1-, 2-, 3-, o 4Dimensional). <br/> |



 

## <a name="remarks"></a>Observaciones

Las macros **D3DFVF \_ TEXCOORDSIZEN** usan las constantes siguientes.


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



La siguiente descripción de FVF identifica un formato de vértice que tiene una posición; un normal; colores difusos y especulares; y dos conjuntos de coordenadas de textura. El primer conjunto de coordenadas de textura incluye un único elemento y el segundo conjunto incluye dos elementos:


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DFVF](d3dfvf.md)
</dt> </dl>

 

 




