---
title: 'Registros: gs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ geometría.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023505"
---
# <a name="registers---gs_5_0"></a>Registros: gs \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ geometría.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count              | L/E | Dimensión         | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096(r \# +x \# \[ n \] ) | L/E | 4                 | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | L/E | 4                 | Sí              | None     | Sí          |
| Entrada de 32 bits (elemento \[ de vértice \] \[ v \] )             | 32                 | R   | 4(comp) \* 32(vert) | Sí              | None     | Sí          |
| Identificador primitivo de entrada de 32 bits (vPrim)                 | 1                  | R   | 1                 | No               | None     | Sí          |
| Identificador de instancia de entrada de 32 bits (vInstanceID)            | 1                  | R   | 1                 | No               | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                | R   | 1                 | No               | None     | Sí          |
| Sampler (s \# )                                     | 16                 | R   | 1                 | No               | None     | Sí          |
| Referencia de ConstantBuffer (índice \# \[ \] cb)          | 15                 | R   | 4                 | Sí (contenido)    | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] ) | 1                  | R   | 4                 | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                               | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento de datos vertex de salida de 32 bits (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




