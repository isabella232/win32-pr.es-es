---
title: 'Registros: ps_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de píxeles \_ .
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d945e06ed3ae1847e15a32da973709b8ceb241ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994534"
---
# <a name="registers---ps_5_0"></a>Registros-PS \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de píxeles \_ .

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count              | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| Atributo de entrada de 32 bits (v \# )                      | 32                 | R   | 4         | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                | R   | 1         | No               | None     | Sí          |
| Muestras (s \# )                                     | 16                 | R   | 1         | No               | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )          | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] ) | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                                      | Count                   | L/E | Dimensión                                | Indexable por r\# | Valores predeterminados | Requiere DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D                     | W   | N/D                                      | N/D              | N/D      | No           |
| Elemento output de 32 bits (o \# )                                        | 8                       | W   | 4                                        | N/D              | N/D      | No           |
| Vista de acceso desordenado (u \# )                                        | 8- \# de Rendertargets | L/E | D3D11 \_ PS \_ CS \_ UAV \_ Registrar \_ componentes | No               | No       | Sí          |
| 32 bit \[ 0.0 f.. 1.0 f \] profundidad de salida de punto flotante (oDepth)                  | 1                       | W   | 1                                        | N/D              | N/D      | Sí          |
| máscara de ejemplo de salida UINT de 32 bits (oMask)                             | 1                       | W   | 1                                        | N/D              | N/D      | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




