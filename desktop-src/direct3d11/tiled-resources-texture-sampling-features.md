---
title: Características de muestreo de textura de recursos en mosaico
description: En esta sección se describen las características de muestreo de textura de recursos en mosaico.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792694"
---
# <a name="tiled-resources-texture-sampling-features"></a>Características de muestreo de textura de recursos en mosaico

En esta sección se describen las características de muestreo de textura de recursos en mosaico.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisitos de los recursos en mosaico características de muestreo de textura

Las características de muestreo de textura que se describen aquí requieren el nivel de nivel 2 de compatibilidad con los recursos [en](tier-2.md) mosaico.

## <a name="shader-feedback-about-mapped-areas"></a>Comentarios del sombreador sobre áreas asignadas

Cualquier instrucción del sombreador que lee y/o escribe en un recurso en mosaico hace que se registre la información de estado. Este estado se expone como un valor de devolución adicional opcional en todas las instrucciones de acceso a recursos que entran en un registro temporal de 32 bits. El contenido del valor devuelto es opaco. Es decir, no se permite la lectura directa por parte del programa de sombreador. Sin embargo, puede usar la función [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) para extraer la información de estado.

## <a name="fully-mapped-check"></a>Comprobación totalmente asignada

La función [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta el estado devuelto desde un acceso a la memoria e indica si todos los datos a los que se tiene acceso se han asignado en el recurso. **CheckAccessFullyMapped** devuelve true (0xFFFFFFFF) si los datos se asignaron o false (0x00000000) si los datos se han desasignado.

Durante las operaciones de filtro, a veces el peso de un textura determinado termina en 0,0. Un ejemplo es una muestra lineal con coordenadas de textura que se encuentran directamente en un centro de textura: 3 otros textura (que pueden variar según el hardware) contribuyen al filtro pero con 0 peso. Estos 0 pesos textura no contribuyen al resultado del filtro, por lo que si se producen en iconos **nulos** , no se cuentan como accesos no asignados. Tenga en cuenta que la misma garantía se aplica a los filtros de textura que incluyen varios niveles de MIP. Si el textura de uno de los mapas de información no está asignado, pero el peso de esos textura es 0, esos textura no cuentan como un acceso sin asignar.

Cuando se realiza un muestreo de un formato que tiene menos de 4 componentes (como el formato de DXGI \_ \_ R8 \_ UNORM), cualquier textura que se encuentra en mosaicos **null** da como resultado un acceso asignado **nulo** que se está informando independientemente de los componentes en los que el sombreador mira realmente en el resultado. Por ejemplo, la lectura de R8 \_ UNORM y el enmascaramiento del resultado de lectura en el sombreador con. GBA/. YZW parecería que no necesitara leer la textura en absoluto. Pero si la dirección textura es un mosaico asignado **nulo** , la operación todavía cuenta como un acceso de asignación **null** .

El sombreador puede comprobar el estado y llevar a cabo cualquier curso de acción deseado en caso de error. Por ejemplo, un curso de acción puede ser el registro de "errores" (por ejemplo, a través de UAV Write) o la emisión de otra lectura fijada a un LOD más general que se sabe que está asignado. Es posible que una aplicación desee realizar un seguimiento de los accesos correctos también con el fin de obtener una idea de qué parte del conjunto de mosaicos asignados tiene acceso.

Una complicación para el registro es que no existe ningún mecanismo para informar del conjunto exacto de mosaicos al que se habría tenido acceso. La aplicación puede hacer conjeturas conservadoras en función de conocer las coordenadas utilizadas para el acceso, así como de usar la instrucción LOD (por ejemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que devuelve el cálculo del uso de hardware de LOD.

Otra complicación es que muchos de los accesos serán a los mismos iconos, por lo que se producirá una gran cantidad de registros redundantes y posiblemente contención en la memoria. Podría ser conveniente si el hardware pudiera tener la opción de no molestarse en el acceso al icono de informe si se notificaba en otro lugar antes. Quizás el estado de este seguimiento podría restablecerse desde la API (probablemente en los límites del marco).

## <a name="per-sample-minlod-clamp"></a>Abrazadera MinLOD por muestra

Para ayudar a los sombreadores a evitar áreas de mipmapped recursos en mosaico que se sabe que no están asignados, la mayoría de las instrucciones del sombreador que implican el uso de una muestra (filtrado) tienen un nuevo modo que permite al sombreador pasar un parámetro de la abrazadera de float32 MinLOD adicional al ejemplo de textura. Este valor se encuentra en el espacio de número de mipmap de la vista, en lugar del recurso subyacente.

El hardware realiza la operación [**Max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(FShaderMinLODClamp, fComputedLOD) en el mismo lugar del cálculo LOD en el que se produce la abrazadera MinLOD por recurso, que también es un **Max**().

Si el resultado de aplicar la abrazadera de LOD por muestra y cualquier otra abrazadera de LOD definida en la muestra es un conjunto vacío, el resultado es el mismo que el resultado de acceso fuera del límite como la abrazadera minLOD por recurso: 0 para los componentes en el formato de superficie y los valores predeterminados para los componentes que faltan.

La instrucción LOD (por ejemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que preasigna la abrazadera minLOD por muestra que se describe aquí, devuelve un LOD desgarrado y desgarrado. El LOD fijado devuelto por esta instrucción LOD refleja todas las abrazaderas, incluida la abrazadera por recurso, pero no una abrazadera por muestra. De todos modos, el sombreador controla y conoce la abrazadera por muestra, por lo que el autor del sombreador puede aplicar manualmente esa abrazadera al valor devuelto de la instrucción LOD si lo desea.

## <a name="minmax-reduction-filtering"></a>Filtrado de reducción mín./máx.

Las aplicaciones pueden optar por administrar sus propias estructuras de datos que les informan del aspecto de las asignaciones para un recurso en mosaico. Un ejemplo sería una superficie que contiene un textura para contener información para cada mosaico de un recurso en mosaico. Podría almacenar el primer LOD que está asignado en una ubicación de mosaico determinada. Al realizar un muestreo cuidadoso de esta estructura de datos de forma similar a como se pretende que se muestree el recurso en mosaico, es posible que descubra cuál será el valor de LOD mínimo que está totalmente asignado para una superficie de filtro de textura completa. Para facilitar este proceso, Direct3D 11,2 presenta un nuevo modo de muestra de uso general, filtrado mínimo y máximo.

La utilidad de filtrado mínimo/máximo para el seguimiento de LOD puede ser útil para otros propósitos, como, quizás el filtrado de superficies de profundidad.

El filtrado de reducción mínimo/máximo es un modo en los muestreadores que capturan el mismo conjunto de textura que un filtro de textura normal debería obtener. Pero en lugar de combinar los valores para generar una respuesta, devuelve el valor mínimo () o máximo () de textura recuperado, por componente (por ejemplo, el valor mínimo de todos los valores de R, independientemente del valor mínimo de todos los valores G, etc.).

Las operaciones Min/Max siguen las reglas de precisión aritmética de Direct3D. No importa el orden de las comparaciones.

Durante las operaciones de filtro que no son Min/Max, a veces el peso de un textura determinado termina siendo 0,0. Un ejemplo es una muestra lineal con coordenadas de textura que se encuentran directamente en textura Center-3 otros textura (que pueden variar según el hardware) contribuyen al filtro pero con 0 peso. En el caso de cualquiera de estos textura que sería 0 peso en un filtro distinto de Min/Max, si el filtro es Min/Max, estos textura todavía no contribuyen al resultado (y los pesos no afectan a la operación de filtro min/max).

La lista completa de modos de filtro se muestra en la enumeración de [**\_ filtros D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) con el valor mínimo y el máximo en los valores de enumeración.

La compatibilidad con esta característica depende de la compatibilidad de [nivel 2](tier-2.md) con recursos en mosaico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 