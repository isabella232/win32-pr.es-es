---
title: 'Registros: gs_4_1'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por las versiones 4 0 y 4 1 del sombreador \_ de \_ geometría.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974716"
---
# <a name="registers---gs_4_1"></a>Registros: gs \_ 4 \_ 1

Esta sección contiene información de referencia para los registros de entrada y salida implementados por las versiones 4 0 y 4 1 del sombreador \_ de \_ geometría.

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

 

 




