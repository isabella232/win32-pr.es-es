---
title: 'Registros: cs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de cálculo \_ .
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9a1164a1b3b4d623ced8453bbee50f561d4666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419064"
---
# <a name="registers---cs_5_0"></a>Registros: CS \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de cálculo \_ .

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                        | Count                                                  | L/E | Dimensión                        | Indexable por r\# | Valores predeterminados | Requiere DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                    | 4096 (r \# + x \# \[ n \] )                                     | L/E | 4                                | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )               | 4096 (r \# + x \# \[ n \] )                                     | L/E | 4                                | Sí              | None     | Sí          |
| Memoria compartida de grupo de subprocesos de 32 bits (g \# \[ n \] )         | 8192 (suma de todos los Decls de memoria compartida para el grupo de subprocesos) | L/E | 1 (se pueden declarar de varias maneras) | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                   | 128                                                    | R   | 1                                | No               | None     | Sí          |
| Muestras (s \# )                                        | 16                                                     | R   | 1                                | No               | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )             | 15                                                     | R   | 4                                | Sí (contenido)   | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] )    | 1                                                      | R   | 4                                | Sí (contenido)    | Ninguno     | Sí          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | No               | N/D      | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                               | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Vista de acceso desordenado (u \# )                                 | 8     | L/E | 1         | No               | No       | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




