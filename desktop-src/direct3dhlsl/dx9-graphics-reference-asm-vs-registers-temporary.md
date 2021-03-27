---
title: Registro temporal (HLSL VS Reference)
description: Un registro temporal del sombreador de vértices se usa para almacenar resultados intermedios.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358526"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Registro temporal (HLSL VS Reference)

Un registro temporal del sombreador de vértices se usa para almacenar resultados intermedios.

Un registro temporal debe inicializarse antes de usarse. Cada registro temporal tiene acceso de una sola escritura y de lectura triple. Esto significa que una sola instrucción del sombreador puede utilizar hasta tres registros temporales como entradas.

No se pueden usar los valores de un registro temporal que permanecen desde las invocaciones anteriores del sombreador de vértices.

Un registro consta de propiedades que determinan el comportamiento de cada registro.



| Propiedad        | Descripción                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre            | r \[ n \] . n es un número de registro opcional. El valor predeterminado es 0 y es el valor que se usa si no se especifica ningún valor.                                                                                 |
| Count           | Un máximo de 12 registros.                                                                                                                                                                  |
| Permisos de e/s | Lectura/escritura Este registro puede ser leído o escrito por la API o por el sombreador.                                                                                                               |
| Leer puertos      | El número de veces que un registro se puede leer en una sola instrucción es 3. Un registro temporal es el único registro que se puede leer y escribir más de una vez en una sola instrucción. |



 

Cada registro temporal tiene acceso de una sola escritura y de lectura triple. Por lo tanto, una instrucción puede tener hasta tres registros temporales en su conjunto de operandos de origen de entrada.

No se puede usar ningún valor en un registro temporal que permanezca de las invocaciones anteriores del sombreador de vértices. Los sombreadores de vértices que leen un valor de un registro temporal antes de escribir en él producirán un error en la llamada a la API de Direct3D para crear el sombreador de vértices.

## <a name="example"></a>Ejemplo

Este es un ejemplo de uso de un registro temporal:


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro temporal     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




