---
title: Predicado Register (referencia de PS de HLSL)
description: Este registro de salida del sombreador de píxeles contiene un valor booleano por canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785068"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Predicado Register (referencia de PS de HLSL)

Este registro de salida del sombreador de píxeles contiene un valor booleano por canal.

Un registro de predicado es compatible con las siguientes versiones:



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro de predicado    |      |      |      |      |      |       | x    | x    | x     |



 

Estas son las propiedades de registro.



| Tipo de registro | Count | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicado (p)  | 1     | L/E | 1             | 1             | 4         | N/D     | None     | N            |



 

El registro de predicado se puede modificar con [SETP \_ COMP-PS](setp-comp---ps.md). No hay valores predeterminados para este registro; una aplicación debe establecer el registro antes de que se use.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




