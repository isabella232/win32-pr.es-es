---
title: 'Registros: gs_4_1'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por las versiones 4 \_ 0 y 4 1 del sombreador de geometría \_ .
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268961"
---
# <a name="registers---gs_4_1"></a>Registros: GS \_ 4 \_ 1

Esta sección contiene información de referencia de los registros de entrada y salida implementados por las versiones 4 \_ 0 y 4 1 del sombreador de geometría \_ .

## <a name="input-registers"></a>Registros de entrada



| Registrarse                 | Nombre | Count              | L/E | Dimensión        | Indexable por r\# | Valores predeterminados | Requiere DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| c\#                      |      | 4096 (r \# + x \# \[ n \] ) | L/E | 4                | No               | None     | Sí          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | L/E | 4                | Sí              | None     | Sí          |
| \# \[ elemento de vértice \] \[ v\] |      | 32                 | R   | 4 (COMP) \* 6 (Vert) | Sí              | None     | Sí          |
| vprim                    |      | 1                  | R   | 1                | No               | None     | Sí          |
| h\#                      |      | 128                | R   | 1                | No               | None     | Sí          |
| s\#                      |      | 16                 | R   | 1                | No               | None     | Sí          |
| \# \[ Índice CB\]            |      | 15                 | R   | 4                | Sí (contenido)    | Ninguno     | Sí          |
| Índice de ICB \[\]             |      | 1                  | R   | 4                | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre            | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| aceptar\#      | Registro de salida | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




