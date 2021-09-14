---
title: 'Registros: vs_4_0'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 0 del sombreador de \_ vértices.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974710"
---
# <a name="registers---vs_4_0"></a>Registros: frente \_ a 4 \_ 0

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 4 0 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse      | Nombre | Count              | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | No               | None     | Sí          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | L/E | 4         | Sí              | None     | Sí          |
| V\#           |      | 16                 | R   | 4         | Sí              | None     | Sí          |
| T\#           |      | 128                | R   | 1         | No               | None     | Sí          |
| s\#           |      | 16                 | R   | 1         | No               | None     | Sí          |
| cb \# \[ index\] |      | 15                 | R   | 4         | Sí (contenido)    | None     | Sí          |
| Índice \[ icb\]  |      | 1                  | R   | 4         | Sí (contenido)    | None     | Sí          |



 

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre            | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Descartar resultado  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro de salida | 16    | W   | N/D       | N/D              | 4        | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




