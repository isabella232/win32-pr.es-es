---
title: 'Registros: vs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de vértices \_ .
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983727"
---
# <a name="registers---vs_5_0"></a>Registros-vs \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de vértices \_ .

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                      | Count              | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| entrada de bit 32 (v \# )                                 | 32                 | R   | 4         | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                 | 128                | R   | 1         | No               | None     | Sí          |
| Muestras (s \# )                                      | 16                 | R   | 1         | No               | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )           | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| referencia de ConstantBuffer de iImmediate (índice de ICB \[ \] ) | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                                      | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento de datos de vértice de salida de 32 bits (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




