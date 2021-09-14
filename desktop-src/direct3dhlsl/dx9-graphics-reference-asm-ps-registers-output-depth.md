---
title: Registro de profundidad de salida
description: El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo \ 0..1\ que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de galería de símbolos de profundidad.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263967"
---
# <a name="output-depth-register"></a>Registro de profundidad de salida

El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo 0..1 que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de galería de símbolos de \[ \] profundidad.

Sintaxis



| oDepth |
|--------|



 

Donde:



| Nombre   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Nuevo valor de profundidad para una prueba de profundidad en el búfer de galería de símbolos de profundidad |



 

Es importante tener en cuenta que escribir en oDepth provoca la pérdida de los algoritmos de optimización de búfer de profundidad específicos del hardware (es decir, Z jerárquico) que aceleran el rendimiento de las pruebas de profundidad.

Al escribir en oDepth, se requiere la replicación de swique de origen (.x \| \| .y .z \| .w). No se permiten máscaras de escritura explícitas.

Al escribir en el registro de oDepth, se reemplaza el valor de profundidad interpolada (y se omite cualquier sesgo de profundidad o representaciones de escala de pendiente). Si no se ha creado ni conectado ningún búfer de profundidad al dispositivo, se omite la escritura en oDepth.

Si está multimuestreo y escribe en oDepth, dado que el sombreador de píxeles solo se ejecuta una vez por píxel, el valor de profundidad se replica para todas las ubicaciones de submuestre cubiertas. La prueba de profundidad todavía se realiza por ejemplo, pero no tiene un valor de profundidad por muestra que vaya a la comparación desde el sombreador de píxeles como lo haría si no hubiera escrito oDepth.

Si una aplicación tiene un w-buffer establecido como búfer de profundidad, debe tenerlo en cuenta al escribir en oDepth. Es posible que necesite enviar información de intervalo w al sombreador de píxeles y calcular el intervalo w para escalar los valores w escritos en oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>ps \_ 2 \_ 0 y ps \_ 2 \_ x Restricciones

-   oDepth solo se puede escribir con la [instrucción mov - ps](mov---ps.md) y solo se puede realizar una vez.
-   No se permite ningún modificador de origen al escribir en oDepth.
-   No se permite ningún modificador de instrucción al escribir en oDepth.
-   No escribir en oDepth desde dentro de una construcción de control de flujo o cuando se usa predicado.

### <a name="ps_3_0-restrictions"></a>ps \_ 3 \_ 0 Restricciones

-   Para ps \_ 3 \_ 0, la salida registra oC# y oD \# se puede escribir cualquier número de veces. La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador. Si no se realiza una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador no lo ha escrito, tampoco se actualiza el destino de representación correspondiente. Si se escribe un subconjunto de los canales de un registro de salida, se escribirán valores no definidos en los canales restantes.
-   Puede escribir en oDepth dentro del control de flujo o el predicado siempre que todas las rutas de acceso posibles escriban finalmente en el registro.
-   No puede realizar cálculos de degradado (u operaciones que invoque implícitamente cálculos de degradado como [texld - ps \_ 2 \_ 0 y](texld---ps-2-0.md)hacia arriba, [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían por primitiva (es decir, instrucciones de control de flujo dinámico). El predicado de instrucciones no se considera control de flujo dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




