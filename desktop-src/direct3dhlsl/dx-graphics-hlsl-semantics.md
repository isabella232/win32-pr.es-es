---
title: Semántica
description: Una semántica es una cadena adjunta a una entrada o salida del sombreador que transmite información sobre el uso previsto de un parámetro.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- BINORMAL, semántica (DirectX HLSL)
- BLENDINDICES, semántica (HLSL de DirectX)
- BLENDWEIGHT, semántica (HlSL de DirectX)
- COLOR, semántica (HLSL de DirectX)
- HL, semántica (HLSL de DirectX)
- POSITIONT, semántica (HLSL de DirectX)
- PSIZE, semántica (HLSL de DirectX)
- TANGENTE, semántica (HLSL de DirectX)
- TESSFACTOR, semántica (HLSL de DirectX)
- TEXCOORD, semántica (HLSL de DirectX)
- VFACE, semántica (HLSL de DirectX)
- VPOS, semántica (HLSL de DirectX)
- System-Value semántica
- Semántica de valores del sistema
- ClipDistance, semántica (DirectX HLSL)
- Cobertura, semántica (HLSL de DirectX)
- CullDistance, semántica (HLSL de DirectX)
- Profundidad, semántica (HLSL de DirectX)
- InstanceID, semántica (HLSL de DirectX)
- IsFrontFace, semántica (HLSL de DirectX)
- Posición, semántica (HLSL de DirectX)
- PrimitiveID, semántica (HLSL de DirectX)
- RenderTargetArrayIndex, semántica (HLSL de DirectX)
- Destino, semántica (HLSL de DirectX)
- SampleIndex, semántica (HLSL de DirectX)
- VertexID, semántica (HLSL de DirectX)
- ViewportArrayIndex, semántica (HLSL de DirectX)
- SV_ClipDistance, semántica (HLSL de DirectX)
- SV_CullDistance, semántica (HLSL de DirectX)
- SV_Depth, semántica (HLSL de DirectX)
- SV_DepthGreaterEqual, semántica (HLSL de DirectX)
- SV_DepthLessEqual, semántica (HLSL de DirectX)
- SV_IsFrontFace, semántica (HLSL de DirectX)
- SV_Position, semántica (HLSL de DirectX)
- SV_RenderTargetArrayIndex, semántica (HLSL de DirectX)
- SV_Target, semántica (HLSL de DirectX)
- SV_ViewportArrayIndex, semántica (HLSL de DirectX)
- SV_InstanceID, semántica (HLSL de DirectX)
- SV_PrimitiveID, semántica (HLSL de DirectX)
- SV_VertexID, semántica (HLSL de DirectX)
- SV_Coverage, semántica (HLSL de DirectX)
- SV_SampleIndex, semántica (HLSL de DirectX)
- SV_InnerCoverage, setcs (DirectX HLSL)
- SV_StencilRef, semántica (HLSL de DirectX)
- SV_GroupID, semántica (HLSL de DirectX)
- SV_GroupThreadID, semántica (HLSL de DirectX)
- SV_DispatchThreadID semántica (HLSL de DirectX)
- SV_GroupIndex, semántica (HLSL de DirectX)
- SV_OutputControlPointID, semántica (HLSL de DirectX)
- SV_TessFactor, semántica (HLSL de DirectX)
- SV_InsideTessFactor, semántica (HLSL de DirectX)
- SV_DomainLocation, semántica (HLSL de DirectX)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8979b4e4842a4c84317b456802ed8f1beefea35
ms.sourcegitcommit: 1d3c59a7066a75facc0565027251cad1ca1dd9c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2021
ms.locfileid: "107594170"
---
# <a name="semantics"></a>Semántica

Una semántica es una cadena adjunta a una entrada o salida del sombreador que transmite información sobre el uso previsto de un parámetro. La semántica es necesaria en todas las variables que se pasan entre las fases del sombreador. La sintaxis para agregar una semántica a una variable de sombreador se muestra aquí ( Sintaxis de variable[(DirectX HLSL).](dx-graphics-hlsl-variable-syntax.md)

En general, los datos pasados entre fases de canalización son completamente genéricos y el sistema no interpreta de forma única; Se permite la semántica arbitraria que no tiene ningún significado especial. Los parámetros (en Direct3D 10 y versiones posteriores) que contienen esta semántica especial se conocen como semántica de valor [del sistema](#system-value-semantics).

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Semántica admitida en Direct3D 9 y Direct3D 10 y versiones posteriores

Los siguientes tipos de semántica se admiten en Direct3D 9 y Direct3D 10 y versiones posteriores.

- [Semántica del sombreador de vértices](#vertex-shader-semantics)
- [Semántica del sombreador de píxeles](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Semántica del sombreador de vértices

Esta semántica tiene significado cuando se adjunta a un parámetro de sombreador de vértices. Esta semántica se admite tanto en Direct3D 9 como en Direct3D 10 y versiones posteriores.

| Entrada | Descripción | Tipo |
|-|-|-|
| BINORMAL \[ n\] | Binormal | float4 |
| BLENDINDICES \[ n\] | Índices de Blend | uint |
| BLENDWEIGHT \[ n\] | Pesos de blend | FLOAT |
| COLOR \[ n\] | Color difuso y especular | float4 |
| NORMAL \[ n\] | Vector normal | float4 |
| POSITION \[ n\] | Posición del vértice en el espacio del objeto. | float4 |
| POSITIONT | Posición del vértice transformado. | float4 |
| PSIZE \[ n\] | Tamaño del punto | FLOAT |
| TANGENT \[ n\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordenadas de textura | float4 |

| Output | Descripción | Tipo |
|-|-|-|
| COLOR \[ n\] | Color difuso o especular | float4 |
| Niebla | Vértice de vértice | FLOAT |
| POSITION \[ n\] | Posición de un vértice en un espacio homogéneo. Calcule la posición en el espacio de pantalla dividiendo (x,y,z) por w. Cada sombreador de vértices debe escribir un parámetro con esta semántica. | float4 |
| PSIZE | Tamaño del punto | FLOAT |
| TESSFACTOR \[ n\] | Factor de teselación | FLOAT |

`n` es un entero opcional entre 0 y el número de recursos admitidos. Por ejemplo, POSITION0, TEXCOORD1, etc.

### <a name="pixel-shader-semantics"></a>Semántica del sombreador de píxeles

Esta semántica tiene significado cuando se adjunta a un parámetro de entrada de sombreador de píxeles. Esta semántica se admite en Direct3D 9 y Direct3D 10 y versiones posteriores.

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
<td>COLOR[n]</td>
<td>Color difuso o especular.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD[n]</td>
<td>Coordenadas de textura</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Escalar de punto flotante que indica una primitiva orientada hacia atrás. Un valor negativo se enfrenta hacia atrás, mientras que un valor positivo se enfrenta a la cámara.
<blockquote>
[!Note]<br />
Esta semántica está disponible en <a href="dx-graphics-hlsl-sm3.md">Direct3D 9 Shader Model 3.0</a>. Para Direct3D 10 y versiones posteriores, use <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> en su lugar.
</blockquote>
<br/></td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>Ubicación de píxeles (x,y) en el espacio de pantalla. Para convertir un sombreador de Direct3D 9 (que usa esta semántica) en un sombreador Direct3D 10 y versiones posteriores, vea <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS y Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
</tbody>
</table>

<table>
<th>Output</th>
<th>Descripción</th>
<th>Tipo</th>
</tr>
<td>COLOR[n]</td>
<td>Color de salida</td>
<td>float4</td>
</tr>
<td>DEPTH[n]</td>
<td>Profundidad de salida</td>
<td>FLOAT</td>
</tr>
</table>

`n` es un entero opcional entre 0 y el número de recursos admitidos. Por ejemplo, PSIZE0, COLOR1, etc.

La semántica color solo es válida en el modo de compatibilidad del sombreador (es decir, cuando el sombreador se crea mediante D3D10 \_ SHADER \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Semántica admitida solo para Direct3D 10 y versiones más recientes.

Los siguientes tipos de semántica se han introducido recientemente para Direct3D 10 y no están disponibles para Direct3D 9.

- [Semántica de valores del sistema](#system-value-semantics)

### <a name="system-value-semantics"></a>System-Value semántica

La semántica de valores del sistema es nueva en Direct3D 10. Todos los valores del sistema comienzan con un prefijo SV, un ejemplo común es SV POSITION, que se \_ interpreta mediante la fase \_ rasterizadora. Los valores del sistema son válidos en otras partes de la canalización. Por ejemplo, la posición sv se puede especificar como una \_ entrada para un sombreador de vértices, así como una salida. Los sombreadores de píxeles solo pueden escribir en parámetros con la semántica de valores del sistema SV Depth y \_ SV \_ Target.

Otros valores del sistema (SV \_ VertexID, SV \_ InstanceID, SV IsFrontFace) solo se pueden introducir en el primer sombreador activo de la canalización que pueda interpretar el valor concreto; después, la función de sombreador debe pasar los valores a las fases \_ posteriores.

SV PrimitiveID es una excepción a esta regla de solo ser entrada en el primer sombreador activo de la canalización que puede interpretar el valor concreto; el hardware puede proporcionar el mismo valor de identificador que la entrada a la fase del sombreador de casco, la fase del sombreador de dominios y, después, la fase que sea la primera habilitada: la fase del sombreador de geometría o la fase de sombreador de \_ píxeles.

Si la teselación está habilitada, la fase de sombreador de casco y la fase de sombreador de dominio están presentes. Para una revisión determinada, el mismo PrimitiveID se aplica a la invocación del sombreador de casco de la revisión y a todas las invocaciones de sombreador de dominios teselados. El mismo PrimitiveID también se propaga a la siguiente fase activa; fase de sombreador de geometría o de sombreador de píxeles si está habilitada.

Si el sombreador de geometría introduce SV PrimitiveID y, dado que puede generar cero o uno o más primitivos por invocación, el sombreador debe programar su propia elección de valor primitiveID de SV para cada primitiva de salida si un sombreador de píxeles posterior introduce \_ \_ SV \_ PrimtiveID.

Como otro ejemplo, SV PrimitiveID no se puede interpretar mediante la fase del sombreador de vértices porque un vértice puede \_ ser miembro de varias primitivas.

Esta semántica se ha agregado a Direct3D 10; no están disponibles en Direct3D 9.

Semántica de valores del sistema para la fase de rasterizador.

| System-Value semántica | Descripción | Tipo |
|-|-|-|
| SV \_ ClipDistance \[ n\] | Recortar datos de distancia. Se supone que los valores de SV \_ ClipDistance son una distancia con firma float32 a un plano. La configuración primitiva solo invoca la rasterización en píxeles para los que las distancias del plano interpolado se >= 0. Se pueden implementar varios planos de recorte simultáneamente, declarando varios componentes de uno o varios elementos de vértice como SV \_ ClipDistance. Los valores combinados clip y cull distance son como máximo componentes D3D CLIP O CULL DISTANCE COUNT en los registros \# \_ \_ \_ D3D CLIP O \_ \_ \# \_ \_ \_ CULL \_ DISTANCE ELEMENT COUNT \_ como \_ máximo. Disponible para todos los sombreadores en los que se va a leer o escribir, excepto el sombreador de vértices que puede escribir el valor pero no tomarlo como entrada.<br/> El **atributo clipplanes** funciona como SV ClipDistance, pero funciona en todas las características \_ de hardware de nivel 9 x y [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) \_ superior. Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](./user-clip-planes-on-10level9.md)<br/> | FLOAT |
| SV \_ CullDistance \[ n\] | Datos de distancia de Cull. Cuando a los componentes de los elementos de vértice se les da esta etiqueta, se supone que estos valores son una distancia con firma float32 a un plano. Las primitivas se descartarán completamente si las distancias del plano de todos los vértices de la primitiva se < 0. Se pueden usar varios planos cull simultáneamente, declarando varios componentes de uno o varios elementos de vértice como SV \_ CullDistance. Los valores combinados clip y cull distance son como máximo componentes D3D CLIP O CULL DISTANCE COUNT en como máximo los registros \# \_ \_ \_ D3D CLIP O \_ \_ \# \_ \_ \_ CULL \_ DISTANCE \_ ELEMENT \_ COUNT. Disponible para todos los sombreadores en los que se va a leer o escribir, excepto el sombreador de vértices que puede escribir el valor pero no tomarlo como entrada.<br/> | FLOAT |
| Cobertura \_ sv | Máscara que se puede especificar en la entrada, salida o ambos de un sombreador de píxeles. <br/> Para la cobertura \_ SV en un sombreador de píxeles, OUTPUT se admite en ps \_ 4 \_ 1 o superior. <br/> Para la cobertura \_ SV en un sombreador de píxeles, INPUT requiere ps \_ 5 \_ 0 o superior. <br/> | uint |
| Profundidad \_ sv | Datos de búfer de profundidad. Se puede escribir mediante sombreador de píxeles. | FLOAT |
| SV \_ DepthGreaterEqual | En un sombreador de píxeles, permite la profundidad de salida, siempre que sea mayor o igual que el valor determinado por el rasterizador. Permite ajustar la profundidad sin deshabilitar la Z inicial. | FLOAT |
| SV \_ DepthLessEqual | En un sombreador de píxeles, permite la profundidad de salida, siempre que sea menor o igual que el valor determinado por el rasterizador. Permite ajustar la profundidad sin deshabilitar la Z inicial. | FLOAT |
| [SV \_ DispatchThreadID](sv-dispatchthreadid.md) | Define el desplazamiento del subproceso global dentro de la llamada a Dispatch, por dimensión del grupo. Disponible como entrada para el sombreador de proceso. (solo lectura) | uint3 |
| [SV \_ DomainLocation](sv-domainlocation.md) | Define la ubicación en el casco del punto de dominio actual que se está evaluando. Disponible como entrada para el sombreador de dominio. (solo lectura) | float2 \| 3 |
| [SV \_ GroupID](sv-groupid.md) | Define el desplazamiento de grupo dentro de una llamada a Dispatch, por dimensión de la llamada de distribución. Disponible como entrada para el sombreador de proceso. (solo lectura) | uint3 |
| [SV \_ GroupIndex](sv-groupindex.md) | Proporciona un índice plano para un subproceso determinado dentro de un grupo determinado. Disponible como entrada para el sombreador de proceso. (solo lectura) | uint |
| [SV \_ GroupThreadID](sv-groupthreadid.md) | Define el desplazamiento del subproceso dentro del grupo, por dimensión del grupo. Disponible como entrada para el sombreador de proceso. (solo lectura) | uint3 |
| [SV \_ GSInstanceID](sv-gsinstanceid.md) | Define la instancia del sombreador de geometría. Disponible como entrada para el sombreador de geometría. La instancia es necesaria, ya que un sombreador de geometría se puede invocar hasta 32 veces en la misma primitiva de geometría. | uint |
| SV \_ InnerCoverage | Representa información de rasterización conservadora infravalora (es decir, si se garantiza que un píxel esté totalmente cubierto). El sombreador de píxeles puede leerlo o escribirlo. | |
| [SV \_ InsideTessFactor](sv-insidetessfactor.md) | Define la cantidad de teselación dentro de una superficie de revisión. Disponible en el sombreador de casco para escritura y disponible en el sombreador de dominio para lectura. | float \| float \[ 2\] |
| SV \_ InstanceID | Identificador por instancia generado automáticamente por el tiempo de ejecución (consulte Uso de [System-Generated valores (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponible para todos los sombreadores. | |
| SV \_ IsFrontFace | Especifica si un triángulo está orientado al frente. Para líneas y puntos, IsFrontFace tiene el valor true. La excepción son las líneas extraídas de triángulos (modo wireframe), que establece IsFrontFace de la misma manera que la rasterización del triángulo en modo sólido. El sombreador de geometría puede escribir en y leerlo el sombreador de píxeles. | bool |
| [SV \_ OutputControlPointID](sv-outputcontrolpointid.md) | Define el índice del identificador de punto de control en el que opera una invocación del punto de entrada principal del sombreador de casco. Solo lo puede leer el sombreador de casco. | uint |
| Sv Position (Posición \_ sv) | Cuando se declara sv position para la entrada a un sombreador, puede tener uno de los dos modos de \_ interpolación especificados: linearNoPerspective o linearNoPerspectiveCentroid, donde el último hace que se proporcionan valores xyzw con ajuste de centroide al suavizar contornos de múltiples muestras. Cuando se usa en un sombreador, SV \_ Position describe la ubicación de píxeles. Disponible en todos los sombreadores para obtener el centro de píxeles con un desplazamiento de 0,5. | float4 |
| SV \_ PrimitiveID | Identificador por primitivo generado automáticamente por el tiempo de ejecución (consulte Uso de [System-Generated valores (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Los sombreadores de geometría o píxeles pueden escribir en y leer en los sombreadores geometry, pixel, hull o domain. | uint |
| SV \_ RenderTargetArrayIndex | Índice de matriz de destino de representación. Se aplica a la salida del sombreador de geometría e indica el segmento de matriz de destino de representación al que el sombreador de píxeles dibujará la primitiva. SV \_ RenderTargetArrayIndex solo es válido si el destino de representación es un recurso de matriz. Esta semántica solo se aplica a las primitivas; Si una primitiva tiene más de un vértice, se usa el valor del vértice inicial. Este valor también indica qué segmento de matriz de una vista de profundidad o galería de símbolos se usa con fines de lectura y escritura.<br/> Se puede escribir desde el sombreador de geometría y leerlo el sombreador de píxeles.<br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) es `true` , SV RenderTargetArrayIndex se aplica a cualquier sombreador que alimenta el \_ rasterizador. | uint |
| SV \_ SampleIndex | Datos de índice de frecuencia de ejemplo. Disponible solo para leer o escribir en el sombreador de píxeles. | uint |
| \_StencilRef de SV | Representa el valor de referencia de la galería de símbolos del sombreador de píxeles actual. Solo lo puede escribir el sombreador de píxeles. | uint |
| Destino \_ SV n , donde \[ \] 0 <= n <= 7 | Valor de salida que se almacenará en un destino de representación. El índice indica en cuál de los 8 destinos de representación posiblemente enlazados se va a escribir. El valor está disponible para todos los sombreadores. | float \[ 2 \| 3 \| 4\] |
| [SV \_ TessFactor](sv-tessfactor.md) | Define la cantidad de teselación en cada borde de una revisión. Disponible para escribir en el sombreador de casco y leer en el sombreador de dominio. | float \[ 2 \| 3 \| 4\] |
| SV \_ VertexID | Identificador por vértice generado automáticamente por el tiempo de ejecución (consulte [Uso de System-Generated valores (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponible solo como entrada para el sombreador de vértices. | uint |
| SV \_ ViewportArrayIndex | Índice de matriz de ventanilla. Se aplica a la salida del sombreador de geometría e indica qué ventanilla se va a usar para la primitiva que se escribe actualmente. El sombreador de píxeles puede leerlo. La primitiva se transformará y recortará en la ventanilla especificada por el índice antes de pasarla al rasterizador. Esta semántica solo se aplica a los primitivos; si una primitiva tiene más de un vértice, se usa el valor del vértice inicial. <br/> Si [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) es , sv ViewportArrayIndex se aplica a cualquier sombreador que alimenta el `true` \_ rasterizador. | uint |
| SV \_ ShadingRate | Define, a través de valores de velocidad de [sombreado,](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)el número de píxeles escritos por una invocación de sombreador de píxeles para dispositivos de nivel [2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o superior. Se puede leer desde el sombreador de píxeles. Se puede escribir desde un sombreador de vértices o geometría. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitaciones al escribir profundidad \_ sv:

- Cuando multimuestreo (MultisampleEnable es **TRUE** en [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)y se escribe un valor de profundidad (mediante un sombreador de píxeles), el valor único escrito también se usa en la prueba de [profundidad,](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)por lo que la capacidad de representar bordes primitivos a una resolución más alta se pierde cuando se multimuestreo.
- Al usar el control de flujo dinámico, es imposible determinar en tiempo de compilación si se garantizará que un sombreador que escribe profundidad SV en algunas rutas de acceso escriba profundidad SV en \_ \_ cada ejecución. Si no se escribe profundidad SV cuando se declara, se produce un comportamiento no definido (que puede incluir o no \_ el descarte del píxel).
- Cualquier valor float32, incluidos +/-INF y NaN, se puede escribir en profundidad \_ SV.
- Escribir profundidad \_ SV sigue siendo válido al realizar la combinación de colores de origen dual.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migración de Direct3D 9 a Direct3D 10 y versiones posteriores

Se deben tener en cuenta los siguientes problemas al migrar código de Direct3D 9 a Direct3D 10 y versiones posteriores:

### <a name="mapping-to-direct3d-9-semantics"></a>Asignación a la semántica de Direct3D 9

Algunas de las semánticas de Direct3D 10 y versiones posteriores se asignan directamente a la semántica de Direct3D 9.

| Semántica de Direct3D 10 | Semántica equivalente de Direct3D 9 |
|-|-|
| Profundidad \_ sv | DEPTH |
| Posición \_ sv | POSITION |
| Destino \_ sv | COLOR |

> [!] Nota para los desarrolladores de Direct3D 9: Para los destinos de Direct3D 9, la semántica del sombreador debe asignarse a una semántica válida de Direct3D 9. Para la compatibilidad con versiones anteriores, POSITION0 (y sus nombres variantes) se trata como SV \_ Position, COLOR se trata como SV \_ TARGET.

- [Asignación a la semántica de Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Posición de VPOS de Direct3D 9 y Direct3D 10 \_ SV](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Planos de recorte de usuario en HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Posición de VPOS de Direct3D 9 y Direct3D 10 \_ SV

La posición SV semántica D3D10 proporciona una funcionalidad similar a la semántica de VPOS 3 del modelo \_ de sombreador 3 de Direct3D 9. Por ejemplo, en Direct3D 9 se usa la sintaxis siguiente para un sombreador de píxeles mediante coordenadas de espacio de pantalla:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS se agregó para la compatibilidad con el modelo de sombreador 3, para especificar coordenadas de espacio de pantalla, ya que la semántica POSITION estaba pensada para coordenadas de espacio de objetos.

En Direct3D 10 y versiones posteriores, la semántica de la posición SV (cuando se usa en el contexto de un sombreador de píxeles) especifica las coordenadas del espacio de pantalla (desplazamiento por \_ 0,5). Por lo tanto, el sombreador de Direct3D 9 sería aproximadamente equivalente (sin tener en cuenta el desplazamiento 0,5) a lo siguiente:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Al migrar de Direct3D 9 a Direct3D 10 y versiones posteriores, debe tener esto en cuenta al traducir los sombreadores.

### <a name="user-clip-planes-in-hlsl"></a>Planos de recorte de usuario en HLSL

A partir de Windows 8, puede usar el atributo de función [](dx-graphics-hlsl-function-syntax.md) **clipplanes** en una declaración de función HLSL en lugar de SV ClipDistance para que el sombreador funcione en el nivel de característica 9 x, así como en el nivel de característica \_ [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 y \_ superior. Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](./user-clip-planes-on-10level9.md)

## <a name="related-topics"></a>Temas relacionados

* [Sintaxis del lenguaje](dx-graphics-hlsl-language-syntax.md)
* [Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
