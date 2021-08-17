---
title: 'Registros: vs_1_1'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 11 del sombreador de \_ vértices.
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908009"
---
# <a name="registers---vs_1_1"></a>Registros: vs \_ 1 \_ 1

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 11 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                  | Count      | L/E | \# Puertos de lectura | \# Reads/inst | Dimensión  | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | L/E | 1             | ilimitadas       | Consulte la nota 3. | No      | Ninguno         | No           |
| c\#      | [Registro flotante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Consulte la nota 2. | R   | 1             | ilimitadas       | 4          | a0.x    | (0, 0, 0, 0) | No           |
| V\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | ilimitadas       | 4          | No      | Consulte la nota 1   | Sí          |
| R\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | L/E | 3             | ilimitadas       | 4          | No      | Ninguno         | No           |



 

Notas:

1.  Parcial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, el valor predeterminado de los canales restantes será (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 96 para vs \_ 1 \_ 1).
3.  Solo está disponible el canal .x.

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre                        | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | Registro de posición           | 1     | W   | 4         | No      | Ninguno     | No           |
| oFog     | Registro de Registrar                | 1     | W   | 1         | No      | Ninguno     | No           |
| Opta     | Registro de tamaño de punto         | 1     | W   | 1         | No      | Ninguno     | No           |
| Od\#     | Registro de color; Consulte la nota 1.  | 2     | W   | 4         | No      | Ninguno     | No           |
| Ot\#     | Registro de coordenadas de textura | 8     | W   | 4         | No      | Ninguno     | No           |



 

Notas:

-   oD0 es la salida de color difuso; oD1 es la salida de color especular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




