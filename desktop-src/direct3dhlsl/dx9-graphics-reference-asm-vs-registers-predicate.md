---
title: Registro de predicado (referencia de HLSL VS)
description: Este registro de salida del sombreador de vértices contiene un valor booleano por canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119579"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Registro de predicado (referencia de HLSL VS)

Este registro de salida del sombreador de vértices contiene un valor booleano por canal.

Las versiones siguientes admiten un registro de predicado.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| registro de predicado     |      |      |       | x    | x    | x     |



 

Estas son las propiedades de registro.



| Tipo de registro | Count | L/E | \# Puertos de lectura | \# Lecturas/inst | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicate(p)  | 1     | L/E | 1             | 1             | 4         | N/D     | None     | N            |



 

El registro de predicado se puede modificar con [setp \_ comp - frente a](setp-comp---vs.md). No hay valores predeterminados para este registro, una aplicación debe establecer el registro antes de su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




