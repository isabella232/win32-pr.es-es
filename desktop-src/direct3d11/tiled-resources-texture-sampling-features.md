---
title: Características de muestreo de textura de recursos en mosaico
description: En esta sección se describen las características de muestreo de textura de recursos en mosaico.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1356b274b5e101a730e3de92a6cdf98b1f293515228fb420a77642f4603757c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119485"
---
# <a name="tiled-resources-texture-sampling-features"></a>Características de muestreo de textura de recursos en mosaico

En esta sección se describen las características de muestreo de textura de recursos en mosaico.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisitos de características de muestreo de textura de recursos en mosaico

Las características de muestreo de textura descritas aquí requieren compatibilidad con recursos en mosaico de nivel [2.](tier-2.md)

## <a name="shader-feedback-about-mapped-areas"></a>Comentarios del sombreador sobre las áreas asignadas

Cualquier instrucción de sombreador que lea o escriba en un recurso en mosaico hace que se grabe la información de estado. Este estado se expone como un valor devuelto adicional opcional en cada instrucción de acceso a recursos que entra en un registro temporal de 32 bits. El contenido del valor devuelto es opaco. Es decir, no se permite la lectura directa por parte del programa de sombreador. Sin embargo, puede usar la [**función CheckAccessFullyMapped para**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) extraer la información de estado.

## <a name="fully-mapped-check"></a>Comprobación totalmente asignada

La [**función CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta el estado devuelto desde un acceso a memoria e indica si todos los datos a los que se accede se asignaron en el recurso. **CheckAccessFullyMapped** devuelve true (0xFFFFFFFF) si los datos se asignaron o false (0x00000000) si los datos no se asignaron.

Durante las operaciones de filtro, a veces el peso de un texel determinado termina siendo 0,0. Un ejemplo es una muestra lineal con coordenadas de textura que se encuentran directamente en un centro de textura: otros tres elementos de textura (que pueden variar según el hardware) contribuyen al filtro, pero con 0 peso. Estos elementos de textura de 0 pesos no contribuyen en absoluto al resultado del filtro, por lo que si se quedan en mosaicos **NULL,** no cuentan como un acceso no autorizado. Tenga en cuenta que la misma garantía se aplica a los filtros de textura que incluyen varios niveles de mip; si los elementos de textura de uno de los mapas mip no están asignados, pero el peso de esos elementos es 0, esos elementos no cuentan como acceso sin asignar.

Cuando se muestrea desde un formato que tiene menos de 4 componentes (como DXGI \_ FORMAT \_ R8 \_ UNORM),   los elementos de textura que se incluyen en los mosaicos NULL tienen como resultado que se informe de un acceso asignado NULL independientemente de los componentes que el sombreador examina realmente en el resultado. Por ejemplo, al leer R8 UNORM y enmascarar el resultado de lectura en el sombreador con .gba/.yzw, no parecería necesario leer la \_ textura. Sin embargo, si la dirección del elemento de textura es un icono asignado a **NULL,** la operación todavía cuenta como un acceso de **asignación NULL.**

El sombreador puede comprobar el estado y llevar a cabo cualquier curso de acción deseado en caso de error. Por ejemplo, un curso de acción puede ser registrar "errores" (por ejemplo, a través de la escritura UAV) o emitir otra lectura fija a un LOD más general que se sabe que se asigna. Es posible que una aplicación también quiera realizar un seguimiento de los accesos correctos para obtener una idea de a qué parte del conjunto asignado de iconos se ha accedido.

Una complicación del registro es que no existe ningún mecanismo para notificar el conjunto exacto de iconos a los que se habría accedido. La aplicación puede realizar sujeciones conservadoras en función de conocer las coordenadas que usó para el acceso, así como de usar la instrucción LOD (por ejemplo, [**tex2Dlod),**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)que devuelve cuál es el cálculo de LOD de hardware.

Otra complicación es que muchos accesos estarán en los mismos iconos, por lo que se producirá una gran cantidad de registro redundante y posiblemente contención en la memoria. Podría ser conveniente si el hardware pudiera tener la opción de no preocuparse de notificar los accesos a los mosaicos si se notificaron en otro lugar antes. Quizás el estado de este seguimiento se podría restablecer desde la API (probablemente en los límites de fotogramas).

## <a name="per-sample-minlod-clamp"></a>Fijación MinLOD por ejemplo

Para ayudar a los sombreadores a evitar áreas de recursos en mosaico mipmapped que se sabe que no están asignados, la mayoría de las instrucciones de sombreador que implican el uso de un muestreador (filtrado) tienen un nuevo modo que permite al sombreador pasar un parámetro de fijación MinLOD float32 adicional a la muestra de textura. Este valor se encuentra en el espacio del número de mapa mipmap de la vista, en lugar del recurso subyacente.

El hardware realiza [**max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(fShaderMinLODClamp,fComputedLOD) en el mismo lugar en el cálculo de LOD donde se produce la fijación MinLOD por recurso, que también es un **máximo**().

Si el resultado de aplicar la fijación de LOD por ejemplo y cualquier otra fijación lod definida en el muestreador es un conjunto vacío, el resultado es el mismo resultado de acceso fuera de límites que la fijación minLOD por recurso: 0 para los componentes en el formato de superficie y el valor predeterminado para los componentes que faltan.

La instrucción LOD (por ejemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que es anterior a la fijación minLOD por ejemplo descrita aquí, devuelve un LOD fija y sin reclamación. El LOD con fijación devuelto por esta instrucción de LOD refleja todas las fijaciones, incluida la fijación por recurso, pero no una fijación por ejemplo. De todos modos, el sombreador controla y conoce la fijación por ejemplo, por lo que el autor del sombreador puede aplicar manualmente esa fijación al valor devuelto de la instrucción LOD si lo desea.

## <a name="minmax-reduction-filtering"></a>Filtrado de reducción mínimo/máximo

Las aplicaciones pueden optar por administrar sus propias estructuras de datos que les informan del aspecto de las asignaciones para un recurso en mosaico. Un ejemplo sería una superficie que contiene un elemento de textura que contiene información de cada icono de un recurso en mosaico. Se puede almacenar el primer LOD que se asigna en una ubicación de mosaico determinada. Mediante un muestreo cuidadosa de esta estructura de datos de forma similar a la que se pretende muestrear el recurso en mosaico, se podría descubrir cuál será el LOD mínimo que está totalmente asignado para una superficie de filtro de textura completa. Para facilitar este proceso, Direct3D 11.2 presenta un nuevo modo sampler de uso general, filtrado mínimo/máximo.

La utilidad de filtrado mínimo/máximo para el seguimiento de LOD puede ser útil para otros propósitos, como, quizás, el filtrado de superficies de profundidad.

El filtrado de reducción mínimo/máximo es un modo en muestreadores que captura el mismo conjunto de elementos de textura que un filtro de textura normal capturaría. Pero en lugar de combinar los valores para generar una respuesta, devuelve el valor min() o max() de los elementos de textura que se capturan, por componente (por ejemplo, el mínimo de todos los valores de R, por separado del mínimo de todos los valores G, y así sucesivamente).

Las operaciones min/max siguen las reglas de precisión aritmética de Direct3D. El orden de las comparaciones no importa.

Durante las operaciones de filtro que no son min/max, a veces el peso de un texel determinado termina siendo 0,0. Un ejemplo es una muestra lineal con coordenadas de textura que se encuentran directamente en un centro de texel; otros 3 elementos texeles (que pueden variar según el hardware) contribuyen al filtro, pero con 0 peso. En el caso de cualquiera de estos elementos de textura que tendrían un peso de 0 en un filtro no mínimo o máximo, si el filtro es mínimo/máximo, estos elementos de textura siguen sin contribuir al resultado (y las ponderaciones no afectan de otro modo a la operación de filtro mínimo/máximo).

La lista completa de modos de filtro se muestra en la enumeración [**\_ FILTER D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) con MINIMUM y MAXIMUM en los valores de enumeración.

La compatibilidad con esta característica depende de la [compatibilidad de nivel 2](tier-2.md) con los recursos en mosaico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 