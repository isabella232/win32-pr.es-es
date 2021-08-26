---
title: 'Registros: cs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ proceso.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01d761fba2b126559e18caf7cf917482d83fec952798b80c3ffc756a5bf3418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023585"
---
# <a name="registers---cs_5_0"></a>Registros: cs \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ proceso.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                        | Count                                                  | L/E | Dimensión                        | Indexable by r\# | Valores predeterminados | Requiere DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                    | 4096(r \# +x \# \[ n \] )                                     | L/E | 4                                | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )               | 4096(r \# +x \# \[ n \] )                                     | L/E | 4                                | Sí              | None     | Sí          |
| Memoria compartida del grupo de subprocesos de 32 bits (g \# \[ n \] )         | 8192 (suma de todas las decls de memoria compartida para el grupo de subprocesos) | L/E | 1 (se puede declarar de varias maneras) | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                   | 128                                                    | R   | 1                                | No               | None     | Sí          |
| Sampler (s \# )                                        | 16                                                     | R   | 1                                | No               | None     | Sí          |
| Referencia de ConstantBuffer (índice cb \# \[ \] )             | 15                                                     | R   | 4                                | Sí (contenido)   | Ninguno     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] )    | 1                                                      | R   | 4                                | Sí (contenido)    | Ninguno     | Sí          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | No               | N/D      | Sí          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | No               | N/D      | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                               | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Vista de acceso desordenado (u \# )                                 | 8     | L/E | 1         | No               | No       | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




