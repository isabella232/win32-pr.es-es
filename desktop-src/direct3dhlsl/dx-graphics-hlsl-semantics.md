---
title: Semántica
description: Una semántica es una cadena adjunta a una entrada o salida del sombreador que transmite información sobre el uso previsto de un parámetro.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- Binormalización, semántica (DirectX HLSL)
- BLENDINDICES, semántica (DirectX HLSL)
- BLENDWEIGHT, semántica (DirectX HLSL)
- COLOR, semántica (DirectX HLSL)
- NIEBLA, semántica (DirectX HLSL)
- POSITIONt, semántica (DirectX HLSL)
- PSIZE, semántica (DirectX HLSL)
- TANGENTE, semántica (DirectX HLSL)
- TESSFACTOR, semántica (DirectX HLSL)
- TEXCOORD, semántica (DirectX HLSL)
- VFACE, semántica (DirectX HLSL)
- VPOS, semántica (DirectX HLSL)
- Semántica de System-Value
- Semántica de valores del sistema
- ClipDistance, semántica (DirectX HLSL)
- Cobertura, semántica (DirectX HLSL)
- CullDistance, semántica (DirectX HLSL)
- Profundidad, semántica (DirectX HLSL)
- InstanceID, semántica (DirectX HLSL)
- IsFrontFace, semántica (DirectX HLSL)
- Posición, semántica (DirectX HLSL)
- PrimitiveID, semántica (DirectX HLSL)
- RenderTargetArrayIndex, semántica (DirectX HLSL)
- Destino, semántica (DirectX HLSL)
- SampleIndex, semántica (DirectX HLSL)
- VertexID, semántica (DirectX HLSL)
- ViewportArrayIndex, semántica (DirectX HLSL)
- SV_ClipDistance, semántica (DirectX HLSL)
- SV_CullDistance, semántica (DirectX HLSL)
- SV_Depth, semántica (DirectX HLSL)
- SV_DepthGreaterEqual, semántica (DirectX HLSL)
- SV_DepthLessEqual, semántica (DirectX HLSL)
- SV_IsFrontFace, semántica (DirectX HLSL)
- SV_Position, semántica (DirectX HLSL)
- SV_RenderTargetArrayIndex, semántica (DirectX HLSL)
- SV_Target, semántica (DirectX HLSL)
- SV_ViewportArrayIndex, semántica (DirectX HLSL)
- SV_InstanceID, semántica (DirectX HLSL)
- SV_PrimitiveID, semántica (DirectX HLSL)
- SV_VertexID, semántica (DirectX HLSL)
- SV_Coverage, semántica (DirectX HLSL)
- SV_SampleIndex, semántica (DirectX HLSL)
- SV_InnerCoverage, semanitcs (DirectX HLSL)
- SV_StencilRef, semántica (DirectX HLSL)
- SV_GroupID, semántica (DirectX HLSL)
- SV_GroupThreadID, semántica (DirectX HLSL)
- Semántica de SV_DispatchThreadID (DirectX HLSL)
- SV_GroupIndex, semántica (DirectX HLSL)
- SV_OutputControlPointID, semántica (DirectX HLSL)
- SV_TessFactor, semántica (DirectX HLSL)
- SV_InsideTessFactor, semántica (DirectX HLSL)
- SV_DomainLocation, semántica (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 510f718608363c547c8333279826cc8bac141358
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279861"
---
# <a name="semantics"></a>Semántica

Una semántica es una cadena adjunta a una entrada o salida del sombreador que transmite información sobre el uso previsto de un parámetro. Se requieren semánticas en todas las variables pasadas entre las fases del sombreador. Aquí se muestra la sintaxis para agregar una semántica a una variable de sombreador ([Sintaxis de variables (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

En general, los datos pasados entre las fases de canalización son completamente genéricos y el sistema no los interpreta de forma exclusiva; se permite la semántica arbitraria, que no tiene ningún significado especial. Los parámetros (en Direct3D 10 y versiones posteriores) que contienen esta semántica especial se conocen como [semántica de valores del sistema](#system-value-semantics).

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Semántica admitida en Direct3D 9 y Direct3D 10 y versiones posteriores

En Direct3D 9 y Direct3D 10 y versiones posteriores se admiten los siguientes tipos de semántica.

- [Semántica del sombreador de vértices](#vertex-shader-semantics)
- [Semántica del sombreador de píxeles](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Semántica del sombreador de vértices

Esta semántica tiene un significado cuando se adjunta a un parámetro de sombreador de vértices. Estas semánticas se admiten en Direct3D 9 y Direct3D 10 y versiones posteriores.

| Entrada | Descripción | Tipo |
|-|-|-|
| Binormal \[ n\] | Binormalización | float4 |
| BLENDINDICES \[ n\] | Índices de Blend | uint |
| BLENDWEIGHT \[ n\] | Pesos de Blend | FLOAT |
| COLOR \[ n\] | Color difuso y especular | float4 |
| NORMAL \[ n\] | Vector normal | float4 |
| POSICIÓN \[ n\] | Posición del vértice en el espacio de objeto. | float4 |
| POSICIÓN | Posición del vértice transformada. | float4 |
| PSIZE \[ n\] | Tamaño del punto | FLOAT |
| TANGENTE \[ n\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordenadas de textura | float4 |
| Output | Descripción | Tipo |
| COLOR \[ n\] | Color difuso o especular | float4 |
| LUZ | Niebla de vértices | FLOAT |
| POSICIÓN \[ n\] | Posición de un vértice en el espacio homogéneo. Calcula la posición en el espacio de pantalla dividiendo (x, y, z) por w. Cada sombreador de vértices debe escribir un parámetro con esta semántica. | float4 |
| PSIZE | Tamaño del punto | FLOAT |
| TESSFACTOR \[ n\] | Factor de teselación | FLOAT |

`n` es un entero opcional entre 0 y el número de recursos admitidos. Por ejemplo, POSITION0, TEXCOORD1, etc.

### <a name="pixel-shader-semantics"></a>Semántica del sombreador de píxeles

Estas semánticas tienen significado cuando se asocian a un parámetro de entrada del sombreador de píxeles. Estas semánticas se admiten en Direct3D 9 y Direct3D 10 y versiones posteriores.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Entrada</th>
<th>Descripción</th>
<th>Tipo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COLOR [n]</td>
<td>Color difuso o especular.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD [n]</td>
<td>Coordenadas de textura</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Escalar de punto flotante que indica un primitivo con conexión inversa. Un valor negativo se enfrenta hacia atrás, mientras que un valor positivo se enfrenta a la cámara.
<blockquote>
[!Note]<br />
Esta semántica está disponible en el <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador de Direct3D 9 3,0</a>. En Direct3D 10 y versiones posteriores, use <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> en su lugar.
</blockquote>
<br/></td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>La ubicación de píxel (x, y) en el espacio de pantalla. Para convertir un sombreador de Direct3D 9 (que usa esta semántica) en un sombreador de Direct3D 10 y versiones posteriores, consulte <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS y Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Output</td>
<td>Descripción</td>
<td>Tipo</td>
</tr>
<tr class="even">
<td>COLOR [n]</td>
<td>Color de salida</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>PROFUNDIDAD [n]</td>
<td>Profundidad de salida</td>
<td>FLOAT</td>
</tr>
</tbody>
</table>

`n` es un entero opcional entre 0 y el número de recursos admitidos. Por ejemplo, PSIZE0, COLOR1, etc.

La semántica del COLOR solo es válida en el modo de compatibilidad del sombreador (es decir, cuando el sombreador se crea con el \_ sombreador D3D10 \_ Habilitar la compatibilidad con \_ versiones anteriores \_ ).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>La semántica solo es compatible con Direct3D 10 y versiones más recientes.

Los siguientes tipos de semántica se han incorporado recientemente para Direct3D 10 y no están disponibles para Direct3D 9.

- [Semántica de valores del sistema](#system-value-semantics)

### <a name="system-value-semantics"></a>Semántica de System-Value

La semántica de valores del sistema es nueva en Direct3D 10. Todos los valores del sistema comienzan con un \_ prefijo VP, un ejemplo común es \_ la posición de la VP, que se interpreta mediante la fase de rasterizador. Los valores del sistema son válidos en otras partes de la canalización. Por ejemplo, \_ la posición de SV se puede especificar como una entrada para un sombreador de vértices, así como una salida. Los sombreadores de píxeles solo pueden escribir en parámetros con la profundidad de SV \_ y la \_ semántica de valor de sistema de destino de SV.

Otros valores del sistema (VP \_ VertexID, VP \_ INSTANCEID, VP \_ IsFrontFace) solo se pueden escribir en el primer sombreador activo de la canalización que puede interpretar el valor concreto; después de que la función de sombreador debe pasar los valores a las fases posteriores.

SV \_ PrimitiveID es una excepción a esta regla de que solo se va a introducir en el primer sombreador activo de la canalización que puede interpretar el valor concreto; el hardware puede proporcionar el mismo valor de identificador que la entrada para la fase del sombreador de casco, la fase del sombreador de dominio y, después de esa fase, la primera fase habilitada: Geometry-Shader Stage

Si la teselación está habilitada, la fase del sombreador de casco y el sombreador de dominio están presentes. En el caso de una revisión determinada, el mismo PrimitiveID se aplica a la invocación del sombreador de casco de la revisión y a todas las invocaciones de sombreador de dominio teselado. El mismo PrimitiveID también se propaga a la siguiente fase activa; fase de sombreador de geometría o de sombreador de píxeles si está habilitada.

Si el sombreador de geometría escribe la VP \_ PrimitiveID y porque puede generar cero o una o más primitivas por invocación, el sombreador debe programar su propia opción de \_ valor de VP PrimitiveID para cada primitiva de salida si un sombreador de píxeles subsiguiente escribe la VP \_ PrimtiveID.

Como otro ejemplo, \_ la fase del sombreador de vértices no puede interpretar la VP PrimitiveID porque un vértice puede ser miembro de varios tipos primitivos.

Estas semánticas se han agregado a Direct3D 10; no están disponibles en Direct3D 9.

Semántica de valor del sistema para la fase de rasterizador.

| Semántica System-Value | Descripción | Tipo |
|-|-|-|
| VP \_ ClipDistance \[ n\] | Datos de la distancia del clip. \_Los valores de ClipDistance de SV se supone que son una distancia con signo float32 a un plano. La configuración primitiva solo invoca la rasterización en píxeles cuyas distancias de plano interpolado son >= 0. Se pueden implementar varios planos de clips simultáneamente, declarando varios componentes de uno o varios elementos de vértice como ClipDistance de la VP \_ . Los valores de distancia de recorte y selección combinados son los componentes de recuento de recortes o de distancia de selección de recorte de D3D en \# \_ \_ \_ \_ \_ la mayoría de \# \_ registros de número de distancia de \_ selección o recorte \_ \_ de D3D \_ \_ . Está disponible para todos los sombreadores que se van a leer o escribir, excepto el sombreador de vértices que puede escribir el valor, pero no como entrada.<br/> El atributo **clipplanes** funciona como la VP \_ ClipDistance, pero funciona en todo el [nivel de características](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) de hardware 9 \_ x y versiones posteriores. Para obtener más información, consulte [planos de clips de usuario en hardware de nivel de característica 9](./user-clip-planes-on-10level9.md).<br/> | FLOAT |
| VP \_ CullDistance \[ n\] | Datos de distancia de selección. Cuando los componentes de los elementos de vértice se proporcionan en esta etiqueta, se supone que cada uno de estos valores es una distancia con signo float32 a un plano. Las primitivas se descartarán por completo si la distancia del plano de todos los vértices de la primitiva es < 0. Se pueden usar varios planos de selección simultáneamente, declarando varios componentes de uno o varios elementos de vértice como CullDistance de la VP \_ . Los valores de distancia de recorte y selección combinados son los componentes de recuento de recortes o de distancia de selección de recorte de D3D en \# \_ \_ \_ \_ \_ la mayoría de \# \_ registros de número de distancia de \_ selección o recorte \_ \_ de D3D \_ \_ . Está disponible para todos los sombreadores que se van a leer o escribir, excepto el sombreador de vértices que puede escribir el valor, pero no como entrada.<br/> | FLOAT |
| Cobertura de SV \_ | Máscara que se puede especificar en la entrada, la salida o ambos de un sombreador de píxeles. <br/> En el caso de \_ la cobertura de SV en un sombreador de píxeles, la salida se admite en PS \_ 4 \_ 1 o superior. <br/> Para \_ la cobertura de SV en un sombreador de píxeles, la entrada requiere PS \_ 5 \_ 0 o superior. <br/> | uint |
| Profundidad de la VP \_ | Datos de búfer de profundidad. Se puede escribir en el sombreador de píxeles. | FLOAT |
| VP \_ DepthGreaterEqual | En un sombreador de píxeles, permite la profundidad de salida, siempre que sea mayor o igual que el valor determinado por el rasterizador. Permite ajustar la profundidad sin deshabilitar la Z temprana. | FLOAT |
| VP \_ DepthLessEqual | En un sombreador de píxeles, permite la profundidad de salida, siempre que sea menor o igual que el valor determinado por el rasterizador. Permite ajustar la profundidad sin deshabilitar la Z temprana. | FLOAT |
| [VP \_ DispatchThreadID](sv-dispatchthreadid.md) | Define el desplazamiento global de subprocesos dentro de la llamada de envío, por dimensión del grupo. Disponible como entrada para el sombreador de cálculo. (solo lectura) | uint3 |
| [VP \_ DomainLocation](sv-domainlocation.md) | Define la ubicación en el casco del punto de dominio actual que se está evaluando. Está disponible como entrada para el sombreador de dominios. (solo lectura) | float2 \| 3 |
| [ID. de \_ la SV](sv-groupid.md) | Define el desplazamiento de grupo dentro de una llamada de envío, por dimensión de la llamada de envío. Está disponible como entrada para el sombreador de cálculo. (solo lectura) | uint3 |
| [VP \_ GroupIndex](sv-groupindex.md) | Proporciona un índice plano para un subproceso determinado dentro de un grupo determinado. Está disponible como entrada para el sombreador de cálculo. (solo lectura) | uint |
| [VP \_ GroupThreadID](sv-groupthreadid.md) | Define el desplazamiento del subproceso dentro del grupo, por dimensión del grupo. Está disponible como entrada para el sombreador de cálculo. (solo lectura) | uint3 |
| [VP \_ GSInstanceID](sv-gsinstanceid.md) | Define la instancia del sombreador de geometría. Está disponible como entrada para el sombreador de geometría. La instancia de es necesaria, ya que se puede invocar un sombreador de geometría hasta 32 veces en la misma primitiva de geometría. | uint |
| VP \_ InnerCoverage | Representa la información de rasterización conservadora desestimada (es decir, si se garantiza que un píxel está totalmente incluido). El sombreador de píxeles puede leer o escribir. | |
| [VP \_ InsideTessFactor](sv-insidetessfactor.md) | Define la cantidad de teselación dentro de una superficie de revisión. Disponible en el sombreador de casco para escritura y disponible en el sombreador de dominios para la lectura. | Float \| float \[ 2\] |
| InstanceID de SV \_ | Identificador por instancia generado automáticamente por el Runtime (vea [usar valores System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Está disponible para todos los sombreadores. | |
| VP \_ IsFrontFace | Especifica si un triángulo está delante. En el caso de las líneas y los puntos, IsFrontFace tiene el valor true. La excepción son las líneas que se dibujan fuera de los triángulos (modo reticular), que establece IsFrontFace de la misma forma que la rasterización del triángulo en modo sólido. Se puede escribir en el sombreador de geometría y el sombreador de píxeles lo lee. | bool |
| [VP \_ OutputControlPointID](sv-outputcontrolpointid.md) | Define el índice del identificador de punto de control en el que se opera mediante una invocación del punto de entrada principal del sombreador de casco. Solo puede ser leído por el sombreador de casco. | uint |
| Posición de la VP \_ | Cuando \_ la posición de VP se declara para la entrada a un sombreador, puede tener uno de los dos modos de interpolación especificados: linearNoPerspective o linearNoPerspectiveCentroid, donde el último hace que se proporcionen valores xyzw con ajuste de centroide cuando el suavizado de contorno de muestreo múltiple. Cuando se usa en un sombreador, \_ la posición VP describe la ubicación de los píxeles. Está disponible en todos los sombreadores para obtener el centro de píxeles con un desplazamiento de 0,5. | float4 |
| VP \_ PrimitiveID | Identificador por primitivo generado automáticamente por el tiempo de ejecución (vea [usar valores System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Los sombreadores de píxeles o de píxeles pueden escribir en ellos y leer los sombreadores de geometría, píxel, casco o dominio. | uint |
| VP \_ RenderTargetArrayIndex | Índice de matriz de destino de representación. Se aplica a la salida del sombreador de geometría e indica el segmento de la matriz de destino de representación al que el sombreador de píxeles va a dibujar el primitivo. \_La VP RenderTargetArrayIndex solo es válida si el destino de representación es un recurso de matriz. Esta semántica se aplica solo a los primitivos; Si un primitivo tiene más de un vértice, se usa el valor del vértice inicial. Este valor también indica qué segmento de matriz de una vista de profundidad o galería de símbolos se usa para fines de lectura y escritura.<br/> Se puede escribir desde el sombreador de geometría y leerlo por el sombreador de píxeles.<br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) es `true` , se \_ aplica la VP RenderTargetArrayIndex a cualquier sombreador que alimenta el rasterizador. | uint |
| VP \_ SampleIndex | Datos de índice de frecuencia de ejemplo. Solo se puede leer o escribir en el sombreador de píxeles. | uint |
| VP \_ StencilRef | Representa el valor de referencia de la galería de símbolos del sombreador de píxeles actual. Solo se puede escribir en el sombreador de píxeles. | uint |
| \_Destino VP \[ n \] , donde 0 <= n <= 7 | Valor de salida que se almacenará en un destino de representación. El índice indica cuál de los 8 destinos de representación enlazados posiblemente en la que se va a escribir. El valor está disponible para todos los sombreadores. | Float \[ 2 \| 3 \| 4\] |
| [VP \_ TessFactor](sv-tessfactor.md) | Define la cantidad de teselación en cada borde de una revisión. Está disponible para escribir en el sombreador de casco y leer en el sombreador de dominios. | Float \[ 2 \| 3 \| 4\] |
| VP \_ VertexID | Identificador por vértice generado automáticamente por el tiempo de ejecución (vea [usar valores System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Solo está disponible como entrada para el sombreador de vértices. | uint |
| VP \_ ViewportArrayIndex | Índice de la matriz de ventanilla. Se aplica a la salida del sombreador de geometría e indica la ventanilla que se va a utilizar para la primitiva que se está escribiendo actualmente. Puede ser leído por el sombreador de píxeles. El primitivo se transformará y se recortará en la ventanilla especificada por el índice antes de pasarlo al rasterizador. Esta semántica se aplica solo a los primitivos; Si un primitivo tiene más de un vértice, se usa el valor del vértice inicial. <br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) es `true` , se \_ aplica la VP ViewportArrayIndex a cualquier sombreador que alimenta el rasterizador. | uint |
| VP \_ ShadingRate | Define, a través de [los valores](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)de velocidad de sombreado, el número de píxeles escritos por una invocación del sombreador de píxeles para dispositivos de nivel 2 o superior de [velocidad de sombreado variable](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Se puede leer desde el sombreador de píxeles. Se puede escribir desde un sombreador de vértices o de geometría. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitaciones al escribir la profundidad de la VP \_ :

- Cuando el muestreo múltiple (MultisampleEnable es **true** en [**D3D10 de \_ rasterización de tramas \_**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)) y escribe un valor de profundidad (mediante un sombreador de píxeles), el valor único escrito también se utiliza en la [prueba de profundidad](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md), por lo que la capacidad de representar bordes primitivos con una resolución mayor se pierde cuando se produce un muestreo múltiple.
- Cuando se usa el control de flujo dinámico, es imposible determinar en tiempo de compilación si se garantiza que un sombreador que escribe la \_ profundidad de la VP en algunas rutas de acceso escribe la \_ profundidad de la VP en cada ejecución. Si no se escribe \_ la profundidad de la VP cuando se declara, se produce un comportamiento indefinido (que puede incluir o no descartar el píxel).
- Cualquier valor float32 incluido +/-INF y NaN se puede escribir en la profundidad de la VP \_ .
- Escribir la profundidad de la VP \_ sigue siendo válida cuando se realiza la mezcla de colores de origen doble.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migración de Direct3D 9 a Direct3D 10 y versiones posteriores

Se deben tener en cuenta los siguientes problemas al migrar código de Direct3D 9 a Direct3D 10 y versiones posteriores:

### <a name="mapping-to-direct3d-9-semantics"></a>Asignación a la semántica de Direct3D 9

Algunas de las semánticas de Direct3D 10 y versiones posteriores se asignan directamente a la semántica de Direct3D 9.

| Semántica de Direct3D 10 | Semántica equivalente en Direct3D 9 |
|-|-|
| Profundidad de la VP \_ | DEPTH |
| Posición de la VP \_ | POSITION |
| Destino de la VP \_ | COLOR |

> [!] Nota para los desarrolladores de Direct3D 9: en el caso de los destinos de Direct3D 9, la semántica del sombreador debe estar asignada a una semántica de Direct3D 9 válida. Para la compatibilidad con versiones anteriores POSITION0 (y sus nombres de variante) se trata como una \_ posición de la VP, el color se trata como el destino de la VP \_ .

- [Asignación a la semántica de Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Posición de la VP de Direct3D 9 VPOS y Direct3D 10 \_](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Planos de clip de usuario en HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Posición de la VP de Direct3D 9 VPOS y Direct3D 10 \_

La posición D3D10 semántica de la VP \_ proporciona una funcionalidad similar a la semántica del modelo de sombreador de Direct3D 9 VPOS. Por ejemplo, en Direct3D 9 se usa la siguiente sintaxis para un sombreador de píxeles mediante coordenadas de espacio de pantalla:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

Se agregó VPOS para la compatibilidad con el modelo de sombreador 3, para especificar las coordenadas del espacio de pantalla, ya que la semántica de la posición estaba pensada para las coordenadas del espacio de objeto.

En Direct3D 10 y versiones posteriores, la \_ semántica de posición de la VP (cuando se usa en el contexto de un sombreador de píxeles) especifica las coordenadas del espacio de pantalla (desplazamiento por 0,5). Por lo tanto, el sombreador de Direct3D 9 sería aproximadamente equivalente (sin tener en cuenta el desplazamiento 0,5) a lo siguiente:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Al migrar de Direct3D 9 a Direct3D 10 y versiones posteriores, tendrá que tener en cuenta esto al traducir los sombreadores.

### <a name="user-clip-planes-in-hlsl"></a>Planos de clip de usuario en HLSL

A partir de Windows 8, puede usar el atributo de función **clipplanes** en una [declaración de función](dx-graphics-hlsl-function-syntax.md) HLSL en lugar de la VP \_ ClipDistance para que el sombreador funcione en el [nivel de característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x, así como en el nivel de \_ característica 10 y versiones posteriores. Para obtener más información, consulte [planos de clips de usuario en hardware de nivel de característica 9](./user-clip-planes-on-10level9.md).

## <a name="related-topics"></a>Temas relacionados

* [Sintaxis del lenguaje](dx-graphics-hlsl-language-syntax.md)
* [Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)