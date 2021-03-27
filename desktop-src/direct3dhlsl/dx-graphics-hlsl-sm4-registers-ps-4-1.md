---
title: 'Registros: ps_4_1'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 4 \_ 1.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994226"
---
# <a name="registers---ps_4_1"></a>Registros: PS \_ 4 \_ 1

Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 4 \_ 1.

## <a name="input-registers"></a>Registros de entrada



| Registrarse      | Nombre | Count              | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| c\#           |      | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| v\#           |      | 32                 | R   | 4         | Sí              | None     | Sí          |
| h\#           |      | 128                | R   | 1         | No               | None     | Sí          |
| s\#           |      | 16                 | R   | 1         | No               | None     | Sí          |
| \# \[ Índice CB\] |      | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| Índice de ICB \[\]  |      | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre             | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado   | N/D   | W   | N/D       | N/D              | N/D      | No           |
| aceptar\#      | Registro de salida  | 8     | W   | N/D       | N/D              | 4        | No           |
| oDepth   | Profundidad de salida     | 1     | W   | N/D       | N/D              | 1        | N/D          |
| oMask    | Máscara de MSAA de salida | 1     | W   | N/D       | N/D              | 1        | N/D          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




