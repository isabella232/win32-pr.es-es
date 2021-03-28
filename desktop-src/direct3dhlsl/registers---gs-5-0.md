---
title: 'Registros: gs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de geometría \_ .
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282b32dd1c8fcb327c273b0fbf3aa51bdb002c2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357606"
---
# <a name="registers---gs_5_0"></a>Registros-GS \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de geometría \_ .

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count              | L/E | Dimensión         | Indexable por r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | L/E | 4                 | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | L/E | 4                 | Sí              | None     | Sí          |
| Entrada de bit 32 ( \[ elemento de vértice v \] \[ \] )             | 32                 | R   | 4 (COMP) \* 32 (Vert) | Sí              | None     | Sí          |
| IDENTIFICADOR primitivo de entrada de 32 bits (vPrim)                 | 1                  | R   | 1                 | No               | None     | Sí          |
| IDENTIFICADOR de instancia de entrada de 32 bits (vInstanceID)            | 1                  | R   | 1                 | No               | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                | R   | 1                 | No               | None     | Sí          |
| Muestras (s \# )                                     | 16                 | R   | 1                 | No               | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )          | 15                 | R   | 4                 | Sí (contenido)    | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] ) | 1                  | R   | 4                 | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                               | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento de datos de vértice de salida de 32 bits (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




