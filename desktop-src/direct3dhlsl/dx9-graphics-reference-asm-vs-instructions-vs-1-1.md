---
title: 'Instrucciones: vs_1_1'
description: Esta sección contiene información de referencia para las instrucciones de la versión 11 del sombreador \_ de vértices.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f980640009158c6c4dc684158836d1514ca47755fea700ac7cc619f6e7574409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789095"
---
# <a name="instructions---vs_1_1"></a>Instrucciones: vs \_ 1 \_ 1

Esta sección contiene información de referencia para las instrucciones de la versión 11 del sombreador \_ de vértices.

Hay varios tipos de instrucciones de sombreador de vértices, como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucción: número de ranuras de instrucción utilizadas por cada instrucción.
-   Configuración: instrucciones no aritméticas. Cada sombreador debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Nuevo: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                                           | Descripción                                                                                                     | Ranuras de instrucción | Configurar | Aritméticos | Nuevo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [add - vs](add---vs.md)                                                       | Agregar dos vectores                                                                                                 | 1                 |       | x          | x   |
| [dcl \_ usage input (sm1, sm2, sm3 - vs asm)](dcl-usage-input-register---vs.md) | Declarar registros de vértices de entrada [(consulte Registros - frente \_ a \_ 1 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def - vs](def---vs.md)                                                       | Definición de constantes                                                                                                | 0                 | x     |            | x   |
| [dp3: vs](dp3---vs.md)                                                       | Producto de puntos de tres componentes                                                                                     | 1                 |       | x          | x   |
| [dp4: vs](dp4---vs.md)                                                       | Producto de punto de cuatro componentes                                                                                      | 1                 |       | x          | x   |
| [dst - vs](dst---vs.md)                                                       | Calcular el vector de distancia                                                                                   | 1                 |       | x          | x   |
| [exp : frente a](exp---vs.md)                                                       | Precisión completa 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp : frente a](exp---vs.md)                                                       | Precisión parcial 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [frc - vs](frc---vs.md)                                                       | Componente fraccionrio                                                                                            | 3                 |       | x          | x   |
| [lit: vs](lit---vs.md)                                                       | Cálculo de iluminación parcial                                                                                    | 1                 |       | x          | x   |
| [log: vs](log---vs.md)                                                       | Registro de precisión completa( x)                                                                                          | 10                |       | x          | x   |
| [logp- vs](logp---vs.md)                                                     | Registro de precisión parcial( x)                                                                                       | 1                 |       | x          | x   |
| [m3x2- vs](m3x2---vs.md)                                                     | Multiplicación de 3x2                                                                                                    | 2                 |       | x          | x   |
| [m3x3: vs](m3x3---vs.md)                                                     | Multiplicación de 3x3                                                                                                    | 3                 |       | x          | x   |
| [m3x4: vs](m3x4---vs.md)                                                     | Multiplicación de 3x4                                                                                                    | 4                 |       | x          | x   |
| [m4x3: vs](m4x3---vs.md)                                                     | Multiplicación de 4x3                                                                                                    | 3                 |       | x          | x   |
| [m4x4: vs](m4x4---vs.md)                                                     | Multiplicación de 4x4                                                                                                    | 4                 |       | x          | x   |
| [loca: vs](mad---vs.md)                                                       | Multiplicar y agregar                                                                                                | 1                 |       | x          | x   |
| [max - vs](max---vs.md)                                                       | Máximo                                                                                                         | 1                 |       | x          | x   |
| [min- vs](min---vs.md)                                                       | Mínima                                                                                                         | 1                 |       | x          | x   |
| [mov: frente a](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          | x   |
| [mul - vs](mul---vs.md)                                                       | Multiplicar                                                                                                        | 1                 |       | x          | x   |
| [nop - vs](nop---vs.md)                                                       | No hay ninguna operación                                                                                                    | 1                 |       | x          | x   |
| [rcp - vs](rcp---vs.md)                                                       | Recíproco                                                                                                      | 1                 |       | x          | x   |
| [rsq- vs](rsq---vs.md)                                                       | Raíz cuadrada recíproca                                                                                          | 1                 |       | x          | x   |
| [sge- vs](sge---vs.md)                                                       | Comparación mayor o igual                                                                                   | 1                 |       | x          | x   |
| [slt- vs](slt---vs.md)                                                       | Menor que compare                                                                                               | 1                 |       | x          | x   |
| [sub - vs](sub---vs.md)                                                       | Restar                                                                                                        | 1                 |       | x          | x   |
| [Vs](vs---vs.md)                                                              | Versión                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




