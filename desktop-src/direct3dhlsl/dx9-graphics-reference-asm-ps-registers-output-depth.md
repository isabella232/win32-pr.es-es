---
title: Registro de profundidad de salida
description: El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo \ 0.. 1 \ que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357754"
---
# <a name="output-depth-register"></a>Registro de profundidad de salida

El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo \[ 0.. 1 \] que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad.

Sintaxis



| oDepth |
|--------|



 

Donde:



| Nombre   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad |



 

Es importante tener en cuenta que la escritura en oDepth provoca la pérdida de los algoritmos de optimización de búfer de profundidad específicos del hardware (es decir, la jerarquía Z) que aceleran el rendimiento de las pruebas de profundidad.

La replicación de origen swizzle (. x. \| y \| . z \| . w) es necesaria cuando se escribe en oDepth. No se permiten las máscaras de escritura explícitas.

La escritura en el registro oDepth reemplaza el valor de profundidad interpolada (y omite cualquier sesgo de profundidad/renderstates slopescale). Si no se ha creado o conectado ningún búfer de profundidad al dispositivo, se omite la escritura en oDepth.

Si va a realizar el muestreo múltiple y escribe en oDepth, dado que el sombreador de píxeles solo se ejecuta una vez por píxel, el valor de profundidad se replica para todas las ubicaciones de submuestras tratadas. La prueba de profundidad sigue ocurriendo por ejemplo, pero no tiene un valor de profundidad por muestra en la comparación desde el sombreador de píxeles como si no hubiera escrito oDepth.

Si una aplicación tiene un búfer de w establecido como su búfer de profundidad, debe tener en cuenta al escribir en oDepth. Es posible que necesite enviar información del rango de w al sombreador de píxeles y calcular el rango de w para escalar los valores w escritos en oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>\_ \_ restricciones de PS 2 0 y PS \_ 2 \_ x

-   oDepth solo se puede escribir con la instrucción [MOV-PS](mov---ps.md) y solo puede realizarse una vez.
-   No se permite ningún modificador de origen al escribir en oDepth.
-   No se permite ningún modificador de instrucción cuando se escribe en oDepth.
-   No se escribe en oDepth desde una construcción de control de flujo o cuando se usa predication.

### <a name="ps_3_0-restrictions"></a>Restricciones de PS \_ 3 \_ 0

-   En el caso de PS \_ 3 \_ 0, los registros de salida \# se pueden escribir en cualquier número de veces. La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador. Si no se produce una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador no lo escribió, el destino de representación correspondiente tampoco se actualiza. Si se escribe un subconjunto de los canales en un registro de salida, los valores no definidos se escribirán en los canales restantes.
-   Puede escribir en oDepth dentro de control de flujo o predication, siempre y cuando todas las rutas de acceso posibles escriban en el registro.
-   No puede realizar ningún cálculo de degradado (u operaciones que invoquen implícitamente los cálculos de degradado como [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían en función de la primitiva (por ejemplo: instrucciones de control de flujo dinámico). La instrucción predication no se considera el control de flujo dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




