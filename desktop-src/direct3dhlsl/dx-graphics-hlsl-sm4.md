---
title: Modelo de sombreador 4
description: El modelo de sombreador 4 es un supraconjunto de las funcionalidades del modelo de sombreador 3, con la excepción de que el modelo de sombreador 4 no es compatible con las características del modelo de sombreador 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420175"
---
# <a name="shader-model-4"></a>Modelo de sombreador 4

El modelo de sombreador 4 es un supraconjunto de las funcionalidades del [modelo de sombreador 3](dx-graphics-hlsl-sm3.md), con la excepción de que el modelo de sombreador 4 no es compatible con las características del modelo de sombreador 1. Se ha diseñado con un núcleo de sombreador común que proporciona un conjunto común de características a todos los sombreadores programables, que solo se pueden programar mediante HLSL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Característica</th>
<th>Funcionalidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conjunto de instrucciones</td>
<td><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones de HLSL</strong></a></td>
</tr>
<tr class="even">
<td>Conjunto de registros</td>
<td>Se puede tener acceso al conjunto de registros a través de los miembros de búferes de constantes y texturas mediante la semántica de HLSL para elementos como el empaquetado de componentes.
<ul>
<li>Registros del sombreador de píxeles (consulte <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">registros-ps_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registros-ps_4_1</a>)</li>
<li>Registros del sombreador de vértices (consulte <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">registros-vs_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registros-vs_4_1</a>)</li>
<li>Registros del sombreador de geometría (consulte <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registros-gs_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registros-gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sombreador de vértices máximo</td>
<td>Sin restricción</td>
</tr>
<tr class="even">
<td>Sombreador de píxeles máximo</td>
<td>Sin restricción</td>
</tr>
<tr class="odd">
<td>Nuevos perfiles de sombreador agregados</td>
<td>gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 *</td>
</tr>
<tr class="even">
<td>Nuevo perfil de Effect-Framework agregado</td>
<td>fx_4_0, fx_4_1 *</td>
</tr>
</tbody>
</table>



 

\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 y FX \_ 4 \_ 1 se admiten en Direct3D 10,1 o superior.

El modelo de sombreador 4 admite una nueva fase de canalización, la fase de sombreador de geometría, que se puede usar para crear o modificar la geometría existente. También incluye dos nuevos tipos de objeto: un objeto de salida de flujo diseñado para la transmisión de datos fuera de la fase de geometría y un objeto de textura con plantilla que implementa funciones de muestreo de textura.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Constantes](dx-graphics-hlsl-constants.md)
-   [Geometry: objeto de sombreador](dx-graphics-hlsl-geometry-shader.md)
-   [Stream: salida de objeto](dx-graphics-hlsl-so-type.md)
-   [Objeto Texture](dx-graphics-hlsl-to-type.md)

El modelo de sombreador 4 admite reglas de empaquetado que determinan la forma en que los datos se pueden organizar cuando se almacenan. Estas reglas se describen en [reglas de empaquetado para variables constantes](dx-graphics-hlsl-packing-rules.md)

En la sección del [ensamblado modelo 4 del sombreador](dx-graphics-hlsl-sm4-asm.md) se describen las instrucciones de ensamblado que admiten el modelo de sombreador 4 y el modelo de sombreador 4,1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




