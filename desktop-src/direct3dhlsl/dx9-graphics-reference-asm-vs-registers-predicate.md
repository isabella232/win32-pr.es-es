---
title: Predicado Register (HLSL VS Reference)
description: Este registro de salida del sombreador de vértices contiene un valor booleano por canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104077144"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Predicado Register (HLSL VS Reference)

Este registro de salida del sombreador de vértices contiene un valor booleano por canal.

Un registro de predicado es compatible con las siguientes versiones.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| registro de predicado     |      |      |       | x    | x    | x     |



 

Estas son las propiedades de registro.



| Tipo de registro | Count | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicado (p)  | 1     | L/E | 1             | 1             | 4         | N/D     | None     | N            |



 

El registro de predicado se puede modificar con [SETP \_ COMP-vs](setp-comp---vs.md). No hay valores predeterminados para este registro, una aplicación debe establecer el registro antes de que se use.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




