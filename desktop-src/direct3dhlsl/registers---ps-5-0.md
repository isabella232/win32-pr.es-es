---
title: 'Registros: ps_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ píxeles.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d432e53626d547bcaf421a4b4ffd9c2aa0f5d0a78ecc3aff9f0b87059c40c0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095345"
---
# <a name="registers---ps_5_0"></a>Registros: ps \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ píxeles.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count              | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096(r \# +x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| Atributo de entrada de 32 bits (v \# )                      | 32                 | R   | 4         | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                | R   | 1         | No               | None     | Sí          |
| Sampler (s \# )                                     | 16                 | R   | 1         | No               | None     | Sí          |
| Referencia de ConstantBuffer (índice \# \[ \] cb)          | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] ) | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                                      | Count                   | L/E | Dimensión                                | Indexable by r\# | Valores predeterminados | Requiere DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D                     | W   | N/D                                      | N/D              | N/D      | No           |
| Elemento de salida de 32 bits (o \# )                                        | 8                       | W   | 4                                        | N/D              | N/D      | No           |
| Vista de acceso sin ordenar (u \# )                                        | 8 - \# de rendertargets | L/E | D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ COMPONENTS | No               | No       | Sí          |
| \[0,0f. de 32 bits. Profundidad de salida float de 1,0f \] (oDepth)                  | 1                       | W   | 1                                        | N/D              | N/D      | Sí          |
| Máscara de ejemplo de salida UINT de 32 bits (oMask)                             | 1                       | W   | 1                                        | N/D              | N/D      | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




