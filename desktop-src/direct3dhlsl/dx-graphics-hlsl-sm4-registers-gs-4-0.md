---
title: 'Registros: gs_4_0'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 0 del sombreador de \_ geometría.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974715"
---
# <a name="registers---gs_4_0"></a>Registros: gs \_ 4 \_ 0

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 0 del sombreador de \_ geometría.

## <a name="input-registers"></a>Registros de entrada



| Registrarse                 | Nombre | Count              | L/E | Dimensión        | Indexable by r\# | Valores predeterminados | Requiere DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| r\#                      |      | 4096(r \# +x \# \[ n \] ) | L/E | 4                | No               | None     | Sí          |
| x \# \[ n\]                 |      | 4096(r \# +x \# \[ n \] ) | L/E | 4                | Sí              | None     | Sí          |
| Elemento \# \[ de vértice \] \[ v\] |      | 32                 | R   | 4(comp) \* 6(vert) | Sí              | None     | Sí          |
| vprim                    |      | 1                  | R   | 1                | No               | None     | Sí          |
| T\#                      |      | 128                | R   | 1                | No               | None     | Sí          |
| s\#                      |      | 16                 | R   | 1                | No               | None     | Sí          |
| cb \# \[ index\]            |      | 15                 | R   | 4                | Sí (contenido)    | None     | Sí          |
| Índice \[ icb\]             |      | 1                  | R   | 4                | Sí (contenido)    | None     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre            | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro de salida | 32    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




