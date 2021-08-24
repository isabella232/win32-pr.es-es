---
title: 'Registros: vs_5_0'
description: Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ vértices.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9c80125a4640e558872e29e435d48e7420bbd6c504577a5e0c84781f8a47d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853905"
---
# <a name="registers---vs_5_0"></a>Registros: vs \_ 5 \_ 0

Los siguientes registros de entrada y salida se implementan en la versión 5 0 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                      | Count              | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                  | 4096(r \# +x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )             | 4096(r \# +x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| Entrada de 32 bits (v \# )                                 | 32                 | R   | 4         | Sí              | None     | Sí          |
| Elemento de un recurso de entrada (t \# )                 | 128                | R   | 1         | No               | None     | Sí          |
| Sampler (s \# )                                      | 16                 | R   | 1         | No               | None     | Sí          |
| Referencia de ConstantBuffer (índice \# \[ \] cb)           | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| Referencia de ConstantBuffer de iImmediate (índice \[ \] icb) | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Tipo de registro                                                      | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (descartar resultado, útil para operaciones con varios resultados) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento de datos vertex de salida de 32 bits (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




