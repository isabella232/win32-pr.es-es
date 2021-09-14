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
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974709"
---
# <a name="registers---vs_4_1"></a>Registros: vs \_ 4 \_ 1

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 1 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse      | Nombre | Count              | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| V\#           |      | 32                 | R   | 4         | Sí              | None     | Sí          |
| T\#           |      | 128                | R   | 1         | No               | None     | Sí          |
| s\#           |      | 16                 | R   | 1         | No               | None     | Sí          |
| cb \# \[ index\] |      | 15                 | R   | 4         | Sí (contenido)    | None     | Sí          |
| Índice \[ icb\]  |      | 1                  | R   | 4         | Sí (contenido)    | None     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre            | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro de salida | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




