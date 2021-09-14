---
title: Registro de predicado (referencia de HLSL PS)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263964"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registro de predicado (referencia de HLSL PS)

Este registro de salida del sombreador de píxeles contiene un valor booleano por canal.

Las siguientes versiones admiten un registro de predicado:



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro de predicado    |      |      |      |      |      |       | x    | x    | x     |



 

Estas son las propiedades de registro.



| Tipo de registro | Count | L/E | \# Lectura de puertos | \# Lecturas/inst | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicate(p)  | 1     | L/E | 1             | 1             | 4         | N/D     | None     | N            |



 

El registro de predicado se puede modificar con [setp \_ comp - ps](setp-comp---ps.md). No hay valores predeterminados para este registro; una aplicación debe establecer el registro antes de que se utilice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




