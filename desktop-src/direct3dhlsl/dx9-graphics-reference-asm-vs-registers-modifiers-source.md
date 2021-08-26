---
title: Modificadores de registro de origen del sombreador de vértices
description: Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción utilice los datos.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f50942d32691d9dc76aa30ddcef36df390fccfe058c31af3527c0eafe0d7df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067985"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificadores de registro de origen del sombreador de vértices

Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción utilice los datos.

## <a name="negate"></a>Negate

Nega el contenido del registro de origen.



| Modificador de componente | Descripción     |
|--------------------|-----------------|
| \- R               | Negación de origen |



 

El modificador negate no se puede usar en el segundo registro de origen de estas instrucciones: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valor absoluto

Tome el valor absoluto del registro.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Si algún sombreador de la versión 3 lee de uno o varios registros float constantes \# (c), debe cumplirse una de las siguientes condiciones.

-   Todos los registros de punto flotante constantes deben usar el modificador abs.
-   Ninguno de los registros de punto flotante constantes puede usar el modificador abs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




