---
title: Registro temporal (referencia de HLSL VS)
description: Un registro temporal del sombreador de vértices se usa para contener resultados intermedios.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eb8d1ee47b224103724ba61fa6c8763069acc0564758a9e531d5d5edb6e2a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119559"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Registro temporal (referencia de HLSL VS)

Un registro temporal del sombreador de vértices se usa para contener resultados intermedios.

Se debe inicializar un registro temporal antes de que se utilice. Cada registro temporal tiene acceso de escritura única y triple lectura. Esto significa que una sola instrucción de sombreador puede usar hasta tres registros temporales como entradas.

No se pueden usar los valores de un registro temporal que permanecen desde invocaciones anteriores del sombreador de vértices.

Un registro consta de propiedades que determinan cómo se comporta cada registro.



| Propiedad        | Descripción                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre            | r \[ n \] . n es un número de registro opcional. El valor predeterminado es 0 y es el valor utilizado si no se especifica ningún valor.                                                                                 |
| Count           | Un máximo de 12 registros.                                                                                                                                                                  |
| Permisos de E/S | Lectura/escritura La API o el sombreador pueden leer o escribir este registro.                                                                                                               |
| Lectura de puertos      | El número de veces que se puede leer un registro dentro de una sola instrucción es 3. Un registro temporal es el único registro que se puede leer y escribir más de una vez en una sola instrucción. |



 

Cada registro temporal tiene acceso de escritura única y triple lectura. Por lo tanto, una instrucción puede tener hasta tres registros temporales en su conjunto de operandos de origen de entrada.

No se puede usar ningún valor en un registro temporal que permanezca de las invocaciones anteriores del sombreador de vértices. Los sombreadores de vértices que leen un valor de un registro temporal antes de escribir en él producirán un error en la llamada API de Direct3D para crear el sombreador de vértices.

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





| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro temporal     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




