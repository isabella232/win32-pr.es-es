---
title: 'Registros: gs_4_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de geometría versión 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532194"
---
# <a name="registers---gs_4_0"></a>Registros-GS \_ 4 \_ 0

Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de geometría versión 4 \_ 0.

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

 

 




