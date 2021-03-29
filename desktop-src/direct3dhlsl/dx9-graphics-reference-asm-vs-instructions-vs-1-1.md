---
title: 'Instrucciones: vs_1_1'
description: Esta sección contiene información de referencia para las instrucciones de la versión 1 del sombreador de vértices \_ .
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b4def55dfaca19608599d9c79e20d3e0690832c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983626"
---
# <a name="instructions---vs_1_1"></a>Instrucciones-vs \_ 1 \_ 1

Esta sección contiene información de referencia para las instrucciones de la versión 1 del sombreador de vértices \_ .

Hay varios tipos de instrucciones de sombreador de vértices, tal como se muestra en la tabla. Las columnas a la derecha significan lo siguiente:

-   Ranuras de instrucciones: número de ranuras de instrucciones usadas por cada instrucción.
-   Instalación: instrucciones no aritméticas. Cada sombreador debe tener una instrucción de versión y debe ser la primera instrucción.
-   Aritmética: estas instrucciones proporcionan las operaciones matemáticas en un sombreador.
-   Nuevas: estas instrucciones son nuevas en esta versión.

## <a name="instruction-set"></a>Conjunto de instrucciones



| Nombre                                                                           | Descripción                                                                                                     | Ranuras de instrucciones | Configurar | Aritméticos | Nuevo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [Agregar vs](add---vs.md)                                                       | Agregar dos vectores                                                                                                 | 1                 |       | x          | x   |
| [\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Declarar registros de vértices de entrada (consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [DEF-vs](def---vs.md)                                                       | Definir constantes                                                                                                | 0                 | x     |            | x   |
| [DP3-vs](dp3---vs.md)                                                       | Producto de tres componentes                                                                                     | 1                 |       | x          | x   |
| [DP4-vs](dp4---vs.md)                                                       | Producto de cuatro componentes                                                                                      | 1                 |       | x          | x   |
| [DST-vs](dst---vs.md)                                                       | Calcular el vector de distancia                                                                                   | 1                 |       | x          | x   |
| [EXP-vs](exp---vs.md)                                                       | Precisión completa 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [EXP-vs](exp---vs.md)                                                       | Precisión parcial 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [FRC-vs](frc---vs.md)                                                       | Componente fraccionario                                                                                            | 3                 |       | x          | x   |
| [Lit-vs](lit---vs.md)                                                       | Cálculo de iluminación parcial                                                                                    | 1                 |       | x          | x   |
| [log-vs](log---vs.md)                                                       | ₂ de registro de precisión completa (x)                                                                                          | 10                |       | x          | x   |
| [logP-vs](logp---vs.md)                                                     | Registro de precisión parcial ₂ (x)                                                                                       | 1                 |       | x          | x   |
| [m3x2-vs](m3x2---vs.md)                                                     | 3x2 multiplicar                                                                                                    | 2                 |       | x          | x   |
| [M3x3-vs](m3x3---vs.md)                                                     | multiplicar 3x3                                                                                                    | 3                 |       | x          | x   |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 multiplicar                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 multiplicar                                                                                                    | 3                 |       | x          | x   |
| [M4x4-vs](m4x4---vs.md)                                                     | multiplicar 4x4                                                                                                    | 4                 |       | x          | x   |
| [Mad-vs](mad---vs.md)                                                       | Multiplicar y agregar                                                                                                | 1                 |       | x          | x   |
| [Max-vs](max---vs.md)                                                       | Máxima                                                                                                         | 1                 |       | x          | x   |
| [min-vs](min---vs.md)                                                       | Mínima                                                                                                         | 1                 |       | x          | x   |
| [MOV-vs](mov---vs.md)                                                       | Move                                                                                                            | 1                 |       | x          | x   |
| [mul-vs](mul---vs.md)                                                       | Multiplicar                                                                                                        | 1                 |       | x          | x   |
| [NOP-vs](nop---vs.md)                                                       | No hay ninguna operación                                                                                                    | 1                 |       | x          | x   |
| [RCP-vs](rcp---vs.md)                                                       | Quede                                                                                                      | 1                 |       | x          | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Raíz cuadrada recíproca                                                                                          | 1                 |       | x          | x   |
| [SGE-vs](sge---vs.md)                                                       | Comparación mayor o igual que                                                                                   | 1                 |       | x          | x   |
| [SLT-vs](slt---vs.md)                                                       | Menor que comparar                                                                                               | 1                 |       | x          | x   |
| [Sub-vs](sub---vs.md)                                                       | Restar                                                                                                        | 1                 |       | x          | x   |
| [virtual](vs---vs.md)                                                              | Versión                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




