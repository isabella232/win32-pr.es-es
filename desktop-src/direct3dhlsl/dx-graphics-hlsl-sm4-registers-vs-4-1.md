---
title: 'Registros: vs_4_1'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 1 del sombreador de \_ vértices.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119929"
---
# <a name="registers---vs_4_1"></a>Registros: vs \_ 4 \_ 1

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 1 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse      | Nombre | Count              | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| V\#           |      | 32                 | R   | 4         | Sí              | None     | Sí          |
| t\#           |      | 128                | R   | 1         | No               | None     | Sí          |
| s\#           |      | 16                 | R   | 1         | No               | None     | Sí          |
| cb \# \[ index\] |      | 15                 | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |
| Índice \[ icb\]  |      | 1                  | R   | 4         | Sí (contenido)    | Ninguno     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre            | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro de salida | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




