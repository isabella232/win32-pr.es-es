---
description: En la página siguiente se proporciona un esquema básico de las diferencias clave entre Direct3D 9 y Direct3D 10. El esquema siguiente proporciona información para ayudar a los desarrolladores con la experiencia de Direct3D 9 a explorar y relacionarse con Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Consideraciones de Direct3D 9 a Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6c2dac7da24184bb5cc6a78f8e7d391c7d0f8b7000107915ba5a606188dcf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120015"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Consideraciones de Direct3D 9 a Direct3D 10 (Direct3D 10)

En la página siguiente se proporciona un esquema básico de las diferencias clave entre Direct3D 9 y Direct3D 10. El esquema siguiente proporciona información para ayudar a los desarrolladores con la experiencia de Direct3D 9 a explorar y relacionarse con Direct3D 10.

Aunque la información de este tema compara Direct3D 9 con Direct3D 10, ya que Direct3D 11 se basa en las mejoras realizadas en Direct3D 10 y 10.1, también necesita esta información para migrar de Direct3D 9 a Direct3D 11. Para obtener información sobre cómo pasar de Direct3D 10 a Direct3D 11, consulte [Migración a Direct3D 11.](../direct3d11/d3d11-programming-guide-migrating.md)

-   [Introducción a los principales cambios estructurales en Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Eliminación de la función fija](#removal-of-fixed-function)
    -   [Validación de la hora de creación de objetos de dispositivo](#device-object-creation-time-validation)
-   [Abstracciones/separación del motor](/windows)
    -   [Eliminación directa de dependencias de Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Trucos para resolver rápidamente problemas de compilación de aplicaciones](#tricks-for-quickly-resolving-application-build-issues)
    -   [Invalidar tipos de Direct3D 9](#overriding-direct3d-9-types)
    -   [Resolución de problemas de vínculo](#resolving-link-issues)
    -   [Simulación de CAP de dispositivo](#simulating-device-caps)
-   [Conducción de la API de Direct3D 10](#driving-the-direct3d-10-api)
    -   [Creación de recursos](#resource-creation)
    -   [Vistas](#views)
    -   [Acceso a recursos estático frente a dinámico](#static-versus-dynamic-resource-access)
    -   [Efectos de Direct3D 10](#direct3d-10-effects)
    -   [HLSL sin efectos](#hlsl-without-effects)
    -   [Compilación del sombreador](#shader-compilation)
    -   [Creación de recursos de sombreador](#creation-of-shader-resources)
    -   [Interfaz de capa de reflexión de sombreador](#shader-reflection-layer-interface)
    -   [Diseños del ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada](/windows)
    -   [Impacto de la eliminación de código no generado del sombreador](#impact-of-shader-dead-code-removal)
    -   [Ejemplo de estructura de entrada del sombreador de vértices](#vertex-shader-input-structure-example)
    -   [Creación de objetos de estado](#state-object-creation)
-   [Porte de texturas](#porting-textures)
    -   [Formatos de archivo admitidos](#file-formats-supported)
    -   [Asignar formatos de textura](#mapping-texture-formats)
-   [Porte de sombreadores](#porting-shaders)
    -   [Los sombreadores de Direct3D 10 se han creado en HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Firmas de sombreador y vinculación](#shader-signatures-and-linkage)
    -   [Vinculaciones de la fase de sombreador HLSL](#hlsl-shader-stage-linkages)
    -   [Búferes constantes](#constant-buffers)
    -   [Planos de recorte de usuario en HLSL en el nivel de característica 9 y superior](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Diferencias adicionales de Direct3D 10 para observar](#additional-direct3d-10-differences-to-watch-for)
    -   [Enteros como entrada](#integers-as-input)
    -   [Cursores del mouse](#mouse-cursors)
    -   [Asignación de elementos de textura a píxeles en Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Cambios de comportamiento de recuento de referencias](#reference-counting-behavior-changes)
    -   [Prueba del nivel de cooperativa](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Diferencias adicionales de Direct3D 10.1](#additional-direct3d-101-differences)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Introducción a los principales cambios estructurales en Direct3D 10

-   [Eliminación de la función fija](#removal-of-fixed-function)
-   [Validación de la hora de creación de objetos de dispositivo](#device-object-creation-time-validation)

El proceso de representación mediante el dispositivo Direct3D 10 es estructuralmente similar a Direct3D 9.

-   Establecer un origen de flujo de vértices
-   Establecer el diseño de entrada en Direct3D 10 (establecer la declaración de flujo de vértices en Direct3D 9)
-   Declarar topología primitiva
-   Establecer texturas
-   Establecer objetos de estado
-   Establecer sombreadores
-   Dibujar

La [**llamada a Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) une las operaciones; el orden de las llamadas antes de la llamada a Draw es arbitrario. Las principales diferencias en el diseño de la API de Direct3D 10 son las siguientes:

-   Eliminación de la función fija
-   Eliminación de bits CAPS: se garantiza el conjunto de características base de Direct3D 10
-   Administración más estricta de: acceso a recursos, estado del dispositivo, constantes de sombreador, vinculación de sombreador (entradas y salidas a sombreadores) entre fases
-   Los cambios en el nombre del punto de entrada de la API reflejan el uso de memoria de GPU virtual (Map() en lugar de Lock()).
-   Se puede agregar una capa de depuración al dispositivo en el momento de la creación
-   La topología primitiva es ahora un estado explícito (separado de la [**llamada a Draw)**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw)
-   Las constantes de sombreador explícitas ahora se almacenan en búferes constantes
-   La creación de sombreadores se realiza completamente en HLSL. El compilador HLSL reside ahora en el archivo DLL principal de Direct3D 10.
-   Nueva fase programable: sombreador de geometría
-   Eliminación de BeginScene()/EndScene()
-   Funcionalidad 2D común, de enfoque y administración de adaptadores implementada en un nuevo componente: DXGI

### <a name="removal-of-fixed-function"></a>Eliminación de la función fija

A veces resulta sorprendente que incluso en un motor de Direct3D 9 que aprovecha por completo la canalización programable, sigue hando una serie de áreas que dependen de la canalización de función fija (FF). Las áreas más comunes suelen estar relacionadas con la representación alineada del espacio de pantalla para la interfaz de usuario. Por este motivo, es probable que tenga que crear un sombreador de emulación ff o un conjunto de sombreadores que proporcionen los comportamientos de reemplazo necesarios.

Esta documentación contiene un documento técnico que contiene orígenes de sombreador de reemplazo para los comportamientos de FF más comunes (vea [Ejemplo de EMU de función fija).](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) Algunos comportamientos de píxeles de función fija, incluida la prueba alfa, se han movido a sombreadores.

### <a name="device-object-creation-time-validation"></a>Validación de la hora de creación de objetos de dispositivo

La canalización de Direct3D 10 se ha rediseñado desde el primer momento en hardware y software con la intención principal de reducir la sobrecarga de CPU (en tiempo de dibujo). Para reducir los costos, se ha asignado un objeto a todos los tipos de datos de dispositivo con métodos de creación explícitos proporcionados por el propio dispositivo. Esto permite una validación de datos estricta en el momento de la creación del objeto en lugar de durante la llamada a Draw, como suele hacer con Direct3D 9.

## <a name="engine-abstractions--separation"></a>Abstracciones/separación del motor

Las aplicaciones, incluidos los juegos, que desean admitir Direct3D 9 y Direct3D 10 deben tener abstraer las capas de representación del resto de la base de código. Hay muchas maneras de lograrlo, pero la clave para todas ellas es el diseño de la capa de abstracción para el dispositivo Direct3D de nivel inferior. Todos los sistemas deben comunicarse con el hardware a través de la capa común que está diseñada para proporcionar administración de recursos de GPU y tipos de bajo nivel.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Eliminación directa de dependencias de Direct3D 9

Al portear bases de código grandes probadas previamente, es importante minimizar la cantidad de cambios de código en aquellos que son absolutamente necesarios para conservar los comportamientos probados previamente en el código. Los procedimientos recomendados incluyen documentar claramente dónde cambian los elementos mediante comentarios. A menudo resulta útil tener un estándar de comentarios para este trabajo que permite la navegación rápida a través de la base de código.

A continuación se muestra una lista de ejemplo de comentarios de bloque de inicio o una sola línea estándar que podrían usarse para este trabajo.



| Elemento                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 REMOVED<br/>                     | Use esta opción donde se quitan las líneas o bloques de código<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 NEEDS UPDATE<br/> | Ayuda a agregar notas adicionales al comentario NEED UPDATE que sugiere qué trabajo o nueva API se debe usar para visitas posteriores al código para la conversión de comportamiento. También se debe usar un uso pesado de assert(**false**) cuando se produce \\ direct3D 10 NEEDS UPDATE para asegurarse de que no se ejecuta código \\ errante sin saberlo.<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 HA CAMBIADO<br/>                     | Las áreas en las que se han producido cambios importantes deben conservarse para futuras referencias, pero comentadas<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 END<br/>                                     | Calificador de bloque de código final<br/>                                                                                                                                                                                                                                                                                            |



 

En el caso de varias líneas de origen, también debe usar los comentarios de estilo //de C, pero agregar los comentarios iniciales y finales \* \* pertinentes en torno a estas áreas.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Trucos para resolver rápidamente problemas de compilación de aplicaciones

-   [Invalidar tipos de Direct3D 9](#overriding-direct3d-9-types)
-   [Resolución de problemas de vínculo](#resolving-link-issues)
-   [Simulación de CAP de dispositivo](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Invalidar tipos de Direct3D 9

Puede ser útil insertar un archivo de encabezado de alto nivel que contenga definiciones de tipo o invalidaciones para tipos base de Direct3D 9 que ya no son compatibles con los encabezados de Direct3D 10. Esto le ayudará a minimizar la cantidad de cambios en el código y las interfaces en las que hay una asignación directa de un tipo Direct3D 9 al tipo direct3D 10 recién definido. Este enfoque también es útil para mantener los comportamientos de código juntos en un archivo de código fuente. En este caso, es una buena idea definir tipos neutrales de versión o con nombre general que describan construcciones comunes usadas para la representación, pero que abarcan las API de Direct3D 9 y Direct3D 10. Por ejemplo:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Otros ejemplos específicos de Direct3D 10 de esto incluyen:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Resolución de problemas de vínculo

Es aconsejable desarrollar aplicaciones direct3D 10 y Windows Vista con la versión más reciente de Microsoft Visual Studio. Sin embargo, es posible compilar una aplicación Windows Vista que depende de Direct3D 10 mediante la versión 2003 anterior de Visual Studio. Direct3D 10 es un componente de la plataforma Windows Vista que tiene dependencias (como con el SDK de la plataforma Server 2003 SP1) en la siguiente biblioteca: BufferOverflowU.lib es necesario para resolver los problemas del vinculador de comprobación de seguridad del \_ búfer.

### <a name="simulating-device-caps"></a>Simulación de CAP de dispositivo

Muchas aplicaciones contienen áreas de código que dependen de que los datos caps del dispositivo estén disponibles. Para evitarlo, invalide la enumeración de dispositivos y forza los CAPS de dispositivo a valores razonables. Planee volver a visitar áreas en las que haya dependencias en CAPS más adelante para la eliminación completa de CAPS siempre que sea posible.

## <a name="driving-the-direct3d-10-api"></a>Conducción de la API de Direct3D 10

Esta sección se centra en los cambios de comportamiento causados por la API de Direct3D 10.

-   [Creación de recursos](#resource-creation)
-   [Vistas](#views)
-   [Acceso a recursos estático frente a dinámico](#static-versus-dynamic-resource-access)
-   [Efectos de Direct3D 10](#direct3d-10-effects)
-   [HLSL sin efectos](#hlsl-without-effects)
-   [Compilación del sombreador](#shader-compilation)
-   [Creación de recursos de sombreador](#creation-of-shader-resources)
-   [Interfaz de capa de reflexión de sombreador](#shader-reflection-layer-interface)
-   [Diseños del ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada](/windows)
-   [Impacto de la eliminación de código no generado del sombreador](#impact-of-shader-dead-code-removal)
-   [Ejemplo de estructura de entrada del sombreador de vértices](#vertex-shader-input-structure-example)
-   [Creación de objetos de estado](#state-object-creation)

### <a name="resource-creation"></a>Creación de recursos

La API de Direct3D 10 ha diseñado recursos como tipos de búfer genéricos que tienen marcas de enlace específicas según el uso planeado. Este punto de diseño se ha elegido para facilitar el acceso casi ubicuo de los recursos de la canalización para escenarios como la representación en un búfer de vértices y, a continuación, dibujar al instante los resultados sin interrumpir la CPU. En el ejemplo siguiente se muestra la asignación de búferes de vértices y búfer de índice, donde puede ver que la descripción del recurso solo difiere en las marcas de enlace de recursos de GPU.

La API de Direct3D 10 ha proporcionado métodos auxiliares de textura para crear explícitamente recursos de tipo de textura, pero como puede imaginar, se trata realmente de funciones auxiliares.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Al tener como destino Direct3D 10, es probable que quiera asignar más elementos durante el tiempo de creación de recursos de los que está acostumbrado con Direct3D 9. Esto se hará más evidente con la creación de búferes de destino de representación y texturas donde también debe crear una vista para acceder al búfer y establecer el recurso en el dispositivo.

[Tutorial 1: Conceptos básicos de Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 y versiones posteriores de Direct3D amplían el formato de archivo DDS para admitir nuevos formatos DXGI, matrices de textura y matrices de mapa de cubo. Para obtener más información sobre la extensión de formato de archivo DDS, vea la [Guía de programación para DDS.](../direct3ddds/dx-graphics-dds-pguide.md)

 

### <a name="views"></a>Vistas

Una vista es una interfaz específicamente con tipo para los datos almacenados en un búfer de píxeles. Un recurso puede tener varias vistas asignadas a la vez y esta característica se resalta en el ejemplo Single Pass Render to Cubemap contenido en este SDK.

[Página guía de programadores en Acceso a recursos](d3d10-graphics-programming-guide-resources-access-views.md)

[Ejemplo de CubeMap](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Acceso a recursos estático frente a dinámico

Para obtener el mejor rendimiento, las aplicaciones deben dividir su uso de datos en términos de la naturaleza estática frente a dinámica de los datos. Direct3D 10 se ha diseñado para aprovechar este enfoque y, como tal, las reglas de acceso de los recursos se han ajustado considerablemente con respecto a Direct3D 9. En el caso de los recursos estáticos, lo ideal es rellenar el recurso con sus datos durante el tiempo de creación. Si el motor se ha diseñado en torno al punto de diseño Crear, Bloquear, Rellenar y Desbloquear de Direct3D 9, puede aplazar el rellenado de la hora de creación mediante un recurso de almacenamiento provisional y el método UpdateSubResource en la interfaz de recursos.

### <a name="direct3d-10-effects"></a>Efectos de Direct3D 10

El uso del sistema de efectos de Direct3D 10 está fuera del ámbito de este artículo. El sistema se ha escrito para aprovechar al máximo las ventajas arquitectónicas que proporciona Direct3D 10. Consulte la [sección Efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) para obtener más detalles sobre su uso.

### <a name="hlsl-without-effects"></a>HLSL sin efectos

La canalización del sombreador de Direct3D 10 se puede dirigir sin el uso del sistema de efectos de Direct3D 10. Tenga en cuenta que, en esta instancia, la propia aplicación debe administrar todo el búfer constante, el sombreador, el muestreador y el enlace de textura. Consulte el vínculo de ejemplo y las secciones siguientes de este documento para obtener más detalles:

[Ejemplo hlsl sin efectos](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilación del sombreador

El compilador HLSL de Direct3D 10 aporta mejoras a la definición del lenguaje HLSL y, por tanto, tiene la capacidad de funcionar en dos modos. Para obtener compatibilidad completa con funciones intrínsecas y semánticas de estilo Direct3D 9, se debe invocar la compilación mediante la marca COMPATIBILITY MODE, que se puede especificar en función de la compilación.

Las funciones intrínsecas y semántica del lenguaje HLSL específicas del modelo de sombreador 4.0 para Direct3D 10 se pueden encontrar en [HLSL.](../direct3dhlsl/dx-graphics-hlsl.md) Los cambios importantes en la sintaxis de HLSL de Direct3D 9 que se van a tener en cuenta se encuentran en el área de acceso de textura. La nueva sintaxis es la única forma admitida por el compilador fuera del modo de compatibilidad.

> [!Note]  
> Las API de tipo compilador de Direct3D 10 [**(D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) y [**D3D10CompileEffectFromMemory)**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)las proporcionan los entornos de ejecución 10, 10.1 y 11 de Direct3D que se ejecutan en Windows Vista y versiones posteriores. Las API de tipo compilador de Direct3D 10 tienen la misma funcionalidad que el compilador HLSL que se incluye en el SDK de DirectX (diciembre de 2006). Este compilador HLSL no admite los perfiles de Direct3D 10.1 (frente \_ a 4 \_ 1, ps \_ 4 \_ 1, gs \_ \_ 4 1, fx \_ 4 \_ 1) y falta una serie de optimizaciones y mejoras. Puede obtener un compilador HLSL que admita los perfiles de Direct3D 10.1 de la versión más reciente del [SDK de DirectX heredado.](/previous-versions/windows/apps/hh452744(v=win.10)) Para obtener información sobre el SDK de DirectX heredado, consulte [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md). Puede obtener la versión más reciente de HLSL Fxc.exe de línea de comandos y las API [de D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) desde el SDK Windows.

 

### <a name="creation-of-shader-resources"></a>Creación de recursos de sombreador

La creación de instancias de sombreador compiladas fuera del sistema de efectos de Direct3D 10 se realiza de forma muy similar a Direct3D 9, pero en Direct3D 10, es importante mantener la firma de entrada del sombreador para su uso posterior. La firma se devuelve de forma predeterminada como parte del blob del sombreador, pero se puede extraer para reducir los requisitos de memoria si es necesario. Para obtener más información, [vea Usar sombreadores en Direct3D 10.](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)

### <a name="shader-reflection-layer-interface"></a>Interfaz de capa de reflexión de sombreador

La capa de reflexión del sombreador es la interfaz por la que se puede obtener información sobre los requisitos del sombreador. Esto es especialmente útil al crear vinculaciones de ensamblados de entrada (consulte a continuación), donde es posible que tenga que recorrer los requisitos de entrada del sombreador para asegurarse de que está suministrando la estructura de entrada correcta al sombreador. Puede crear una instancia de la interfaz de capa de reflexión al mismo tiempo que crear una instancia de un sombreador compilado.

La capa de reflexión del sombreador reemplaza a los métodos D3DX9 que proporcionan una funcionalidad similar. Por [**ejemplo, IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) se reemplaza por el [**método GetDesc.**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc)

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Diseños del ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada

El ensamblador de entrada (IA) reemplaza la declaración de flujo de vértices de estilo Direct3D 9 y su estructura de descripción es muy similar en el formato. La principal diferencia que aporta el IA es que el objeto de diseño de IA creado debe asignarse directamente a un formato específico de firma de entrada del sombreador. El objeto de asignación creado para vincular el flujo de entrada al sombreador se puede usar en cualquier número de sombreadores donde la firma de entrada del sombreador coincida con la del sombreador utilizado para crear el diseño de entrada.

Para impulsar mejor la canalización con datos estáticos, debe tener en cuenta las permutaciones del formato de flujo de entrada a posibles firmas de entrada del sombreador y crear las instancias de objeto de diseño de IA lo antes posible y reutilizarlas siempre que sea posible.

### <a name="impact-of-shader-dead-code-removal"></a>Impacto de la eliminación de código no generado del sombreador

En la sección siguiente se detalla una diferencia significativa entre Direct3D 9 y Direct3D 10 que es probable que requiera un control preciso en el código del motor. Los sombreadores que contienen expresiones condicionales a menudo quitan determinadas rutas de acceso de código como parte del proceso de compilación. En Direct3D 9, se pueden quitar dos tipos de entradas (marcadas para su eliminación) cuando no se usan: entradas de firma (como en el ejemplo siguiente) y entradas constantes. Si el final del búfer constante contiene entradas no utilizadas, la declaración de tamaño en el sombreador reflejará el tamaño del búfer constante sin las entradas sin usar al final. Ambos tipos de entradas permanecen en firmas o búferes constantes direct3D 10 con una excepción especial en el caso de entradas constantes no utilizadas al final de un búfer constante. Esto puede afectar al motor al controlar sombreadores grandes y crear diseños de entrada. Los elementos que se quitan mediante optimizaciones de código no encontrado en el compilador todavía deben declararse en la estructura de entrada. En el siguiente ejemplo se muestra esto:

### <a name="vertex-shader-input-structure-example"></a>Ejemplo de estructura de entrada del sombreador de vértices


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* La eliminación de código no encontrado de Direct3D 9 quitaría la declaración en el sombreador debido a la eliminación condicional de código no encontrado


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



O bien, podría hacer aún más evidente que la constante es una constante de tiempo de compilación con la siguiente declaración:


```
#define LIGHT_MAPPED false
```



En el ejemplo anterior, en Direct3D 9, el elemento uv2 se quitaría debido a las optimizaciones de código no generado en el compilador. En Direct3D 10, se seguirá quitando el código fallido, pero el diseño del ensamblador de entrada del sombreador requiere que exista la definición de los datos de entrada. La capa de reflexión del sombreador proporciona los medios para controlar esta situación de forma genérica, por lo que puede recorrer los requisitos de entrada del sombreador y asegurarse de proporcionar una descripción completa de la asignación de la firma de flujo de entrada al sombreador.

Esta es una función de ejemplo para detectar la existencia de un nombre o índice semánticos en una firma de función:


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>Creación de objetos de estado

Al portear código del motor, puede ayudar a usar inicialmente un conjunto predeterminado de objetos de estado y deshabilitar toda la configuración de estado de representación o estado de textura del dispositivo Direct3D 9. Esto provocará artefactos de representación, pero es la manera más rápida de empezar a funcionar. Más adelante puede construir un sistema de administración de objetos de estado que puede usar una clave compuesta para habilitar la reutilización máxima del número de objetos de estado que se usan.

## <a name="porting-textures"></a>Porte de texturas

### <a name="file-formats-supported"></a>Formatos de archivo admitidos

Las funciones **D3DXxxCreateXXX** y **D3DXxxSaveXXX** que crean o guardan una textura desde o en un archivo de gráficos (por ejemplo, [**D3DX10CreateTextureFromFile)**](d3dx10createtexturefromfile.md)admiten un conjunto diferente de formatos de archivo en Direct3D 10 que en Direct3D 9:



| Formato de archivo | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| .ppm        | x          |             |
| .dib        | x          |             |
| .hdr        | x          |             |
| .pfm        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Para obtener más información, compare las enumeraciones FILEFORMAT de Direct3D 9 [**D3DXIMAGE \_**](../direct3d9/d3dximage-fileformat.md) con las enumeraciones [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md) para Direct3D 10.

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8. Para el procesamiento de archivos de textura, se recomienda usar [DirectXTex.](https://github.com/Microsoft/DirectXTex)

 

### <a name="mapping-texture-formats"></a>Asignar formatos de textura

En la tabla siguiente se muestra la asignación de formatos de textura de Direct3D 9 a Direct3D 10. Cualquier contenido en formatos que no estén disponibles en DXGI deberá convertirse mediante rutinas de utilidad.



| Formato de Direct3D 9                   | Formato Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                     | FORMATO DXGI \_ \_ DESCONOCIDO                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | FORMATO \_ DXGI \_ B8G8R8A8 \_ UNORM & DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | FORMATO \_ DXGI \_ B8G8R8X8 \_ UNORM & DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | FORMATO DXGI \_ \_ B5G6R5 \_ UNORMNTES                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORMNTES                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | FORMATO DXGI \_ \_ B4G4R4A4 \_ UNORMNTES                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | DXGI \_ FORMAT \_ A8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | FORMATO DXGI \_ \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM & DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | DXGI \_ FORMAT \_ R8 UNORM Nota: Use .r swzzle en el sombreador para duplicar el rojo a otros componentes para \_ obtener el comportamiento D3D9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ FORMAT \_ R8G8 UNORM Nota: Use sw dragle .rrrg en el sombreador para duplicar el color rojo y moverse de color verde a los componentes alfa para obtener el comportamiento \_ D3D9.                                                                                                            |
| D3DFMT \_ A4L4                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ FORMAT G8R8 G8B8 UNORM (en DX9, los datos se escalaron verticalmente en \_ \_ 255,0f, pero esto se puede controlar en el código del \_ sombreador).                                                                                                                                   |
| D3DFMT \_ YUY2                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ FORMAT R8G8 B8G8 UNORM (en DX9, los datos se escalaron verticalmente en \_ \_ 255,0f, pero esto se puede controlar en el código del \_ sombreador).                                                                                                                                   |
| D3DFMT \_ DXT1                        | DXGI \_ FORMAT \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ FORMAT \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB Nota: DXT1 y DXT2 son los mismos desde una perspectiva de API/hardware... la única diferencia era "alfa premultiplicado", que una aplicación puede realizar un seguimiento y no necesita un formato independiente. |
| D3DFMT \_ DXT3                        | FORMATO DXGI \_ \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ FORMAT \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB Nota: DXT3 y DXT4 son los mismos desde una perspectiva de API/hardware... la única diferencia era "alfa premultiplicado", que una aplicación puede realizar un seguimiento y no necesita un formato independiente. |
| D3DFMT \_ DXT5                        | DXGI \_ FORMAT \_ BC3 \_ UNORM & DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ LOCKABLE | DXGI \_ FORMAT \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | DXGI \_ FORMAT \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ LOCKABLE              | DXGI \_ FORMAT \_ D32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI \_ FORMAT \_ R16 UNORM Nota: Use .r swzzle en el sombreador para duplicar el rojo a otros componentes para obtener el comportamiento \_ D3D9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI \_ FORMAT \_ R16 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI \_ FORMAT \_ R32 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI \_ FORMAT \_ R16 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI FORMAT R8G8B8A8 UINT Nota: El sombreador obtiene valores UINT, pero si se necesitan flotantes enteros de estilo \_ \_ \_ Direct3D 9 (0,0f, 1,0f... 255.f), UINT solo se puede convertir a float32 en el sombreador.                                                               |
| D3DDECLTYPE \_ SHORT2                 | DXGI \_ FORMAT R16G16 SINT Nota: El sombreador obtiene valores SINT, pero si se necesitan flotantes enteros de estilo \_ \_ Direct3D 9, SINT solo se puede convertir a float32 en el sombreador.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI \_ FORMAT \_ R16G16B16A16 SINT Nota: El sombreador obtiene valores SINT, pero si se necesitan flotantes enteros de estilo \_ Direct3D 9, SINT solo se puede convertir a float32 en el sombreador.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | DXGI \_ FORMAT \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | DXGI \_ FORMAT \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹DXGI 1.1, que se incluye en el entorno de ejecución de Direct3D 11, incluye formatos BGRA. Sin embargo, la compatibilidad con estos formatos es opcional para dispositivos Direct3D 10 y 10.1 con controladores que se implementan en Windows Display Driver Model (WDDM) para Windows Vista (WDDM 1.0). Considere la posibilidad de usar DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM en su lugar. Como alternativa, puede crear el dispositivo con [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) para asegurarse de que solo admite equipos con el entorno de ejecución de Direct3D 11.0 y un controlador WDDM 1.1 o superior instalado.

TivoDXGI 1.0 definió los formatos 5:6:5 y 5:5:5:1, pero no eran compatibles con el runtime de Direct3D 10.x o Direct3D 11.0. Estos formatos se admiten opcionalmente con DXGI 1.2 en el entorno de ejecución de DirectX 11.1, que es necesario para los adaptadores de vídeo de nivel de característica 11.1 y los controladores WDDM 1.2 (modelo de controlador de pantalla a partir de Windows 8) y ya se admiten en niveles de características de 10level9.

TivosGI 1.2 introdujeron el formato 4:4:4:4. Este formato se admite opcionalmente en el entorno de ejecución de DirectX 11.1, que es necesario para los adaptadores de vídeo de nivel de característica 11.1 y los controladores WDDM 1.2 y ya se admite en niveles de características de 10level9.

En el caso de los formatos sin comprimir, DXGI ha limitado la compatibilidad con patrones de formato de píxel arbitrario; todos los formatos sin comprimir deben ser de tipo RGBA. Esto puede requerir la aplicación de formatos de píxeles de recursos existentes, que se recomienda calcular como un paso de pre-proceso sin conexión siempre que sea posible.

## <a name="porting-shaders"></a>Porte de sombreadores

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Los sombreadores de Direct3D 10 se han creado en HLSL

Direct3D 10 limita el uso del lenguaje de ensamblado al de depuración únicamente, por lo que cualquier sombreador de ensamblado escrito a mano que se use en Direct3D 9 tendrá que convertirse a HLSL.

### <a name="shader-signatures-and-linkage"></a>Firmas de sombreador y vinculación

Se han analizado los requisitos para la vinculación del ensamblado de entrada con las firmas de entrada del sombreador de vértices anteriormente en este documento (consulte más arriba). Tenga en cuenta que el entorno de ejecución de Direct3D 10 también ha mejorado los requisitos de vinculación de fase a fase entre sombreadores. Este cambio afectará a los orígenes del sombreador en los que es posible que el enlace entre fases no se haya descrito por completo en Direct3D 9. Por ejemplo:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* VS roto - PS Linkage : aunque el sombreador de píxeles no esté interesado en la matriz completa, la vinculación debe especificar el float4x3 completo.

Tenga en cuenta que la semántica de vinculación entre fases debe coincidir exactamente, pero las entradas de las fases de destino pueden ser un prefijo de los valores que se están generando. En el ejemplo anterior, el sombreador de píxeles podría tener position y texcoord1 como las únicas entradas, pero no pudo tener la posición y texcoord2 como las únicas entradas debido a las restricciones de ordenación.

### <a name="hlsl-shader-stage-linkages"></a>Vinculaciones de la fase de sombreador HLSL

La vinculación entre sombreadores puede producirse en cualquiera de los puntos siguientes de la canalización:

-   Ensamblador de entrada al sombreador de vértices
-   Sombreador de vértices a sombreador de píxeles
-   Sombreador de vértices a sombreador de geometría
-   Sombreador de vértices para transmitir salida
-   Sombreador de geometría a sombreador de píxeles
-   Sombreador de geometría para transmitir

### <a name="constant-buffers"></a>Búferes constantes

Para facilitar la porción de contenido de Direct3D 9, un enfoque inicial para la administración constante fuera del sistema de efectos podría implicar la creación de un búfer constante único que contenga todas las constantes necesarias. Es importante que el rendimiento ordene las constantes en búferes según la frecuencia esperada de actualización. Esta organización reducirá al mínimo la cantidad de conjuntos de constantes redundantes.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Planos de recorte de usuario en HLSL en el nivel de característica 9 y superior

A partir de Windows 8, puede usar el atributo de función [](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) **clipplanes** en una declaración de función HLSL en lugar de [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para que el sombreador funcione en el nivel [de](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) característica 9 x, así como en el nivel de característica \_ 10 y superior. Para obtener más información, consulte [Planos de recorte de usuario en hardware de nivel de característica 9.](../direct3dhlsl/user-clip-planes-on-10level9.md)

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Diferencias adicionales de Direct3D 10 para observar

### <a name="integers-as-input"></a>Enteros como entrada

En Direct3D 9, no había compatibilidad de hardware real con tipos de datos enteros, pero el hardware de Direct3D 10 admite tipos enteros explícitos. Si tiene datos de punto flotante en el búfer de vértices, debe tener una entrada float. De lo contrario, un tipo entero será la representación del patrón de bits del valor de punto flotante. No se permite un tipo entero para una entrada de sombreador de píxeles a menos que el valor esté marcado para ninguna interpolación (vea [Modificadores de interpolación](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursores del mouse

En versiones anteriores de Windows, las rutinas estándar de cursor del mouse GDI no funcionaba correctamente en todos los dispositivos exclusivos de pantalla completa. Las [**API SetCursorProperties,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties) [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)y [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) se agregaron para controlar estos casos. Puesto Windows versión de GDI de Vista entiende completamente las superficies [DXGI,](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) no es necesario esta API de cursor de mouse especializada, por lo que no hay ningún equivalente de Direct3D 10. En su lugar, las aplicaciones de Direct3D 10 deben usar las rutinas estándar de [cursor de mouse GDI](../menurc/cursors.md) para los cursores del mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Asignación de elementos de textura a píxeles en Direct3D 10

En Direct3D 9, los centros de texel y los centros de píxeles estaban separados por una media unidad (vea Asignación directa de elementos de textura a píxeles [(Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). En Direct3D 10, los centros de texel ya están a medias unidades, por lo que no es necesario desplazar las coordenadas de vértice en absoluto.

La representación de quads de pantalla completa es más directa con Direct3D 10. Los quads de pantalla completa se deben definir en el espacio de recorte (-1,1) y simplemente pasar a través del sombreador de vértices sin cambios. De este modo, no es necesario volver a cargar el búfer de vértices cada vez que cambia la resolución de la pantalla y no hay ningún trabajo adicional en el sombreador de píxeles para manipular las coordenadas de textura.

### <a name="reference-counting-behavior-changes"></a>Cambios de comportamiento de recuento de referencias

A diferencia de las versiones anteriores de Direct3D, las distintas funciones Set no contendrán una referencia a los objetos de los dispositivos. Esto significa que la aplicación debe asegurarse de que contiene una referencia en el objeto mientras quiera que ese objeto esté enlazado a la canalización. Cuando el recuento de referencias del objeto cae a cero, el objeto se desenlazó de la canalización a medida que se destruya. Este estilo de retención de referencia también se conoce como retención de referencia débil, por lo que cada ubicación de enlace en el objeto Device contiene una referencia débil al objeto interface/. A menos que se indique explícitamente lo contrario, este comportamiento debe asumirse para todos los métodos Set. Cada vez que la destrucción de un objeto hace que un punto de enlace se establezca en **NULL,** la capa de depuración emitirá una advertencia. Tenga en cuenta que las llamadas a métodos Get del [**dispositivo, como OMGetRenderTargets,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) aumentarán el recuento de referencias de los objetos que se devuelven.

### <a name="test-cooperative-level"></a>Prueba del nivel de cooperativa

La funcionalidad de [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) de la API de Direct3D 9 es análoga a la configuración de [DXGI \_ PRESENT \_ TEST](../direct3ddxgi/dxgi-present.md) al llamar a [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Una función similar al método [**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) de Direct3D 9 no está disponible en Direct3D 10 y 10.1. Para copiar superficies de recursos, use [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Para cambiar el tamaño de las operaciones, represente en una textura mediante el filtrado de textura. Para convertir superficies de MSAA en superficies que no son de MSAA, use [**ID3D10Device::ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Diferencias adicionales de Direct3D 10.1

Windows Vista con Service Pack 1 (SP1) incluía una actualización secundaria de Direct3D 10 y Direct3D 10.1, que exponía las siguientes características de hardware adicionales:

-   Sombreadores de MSAA por ejemplo
-   Lectura de profundidad de MSAA
-   Modos de combinación independientes por destino de representación
-   Matrices de mapa de cubos
-   Representación en formatos comprimidos en bloques (BC)

La actualización 10.1 de Direct3D agregó compatibilidad con las siguientes interfaces nuevas, que se derivan de las interfaces existentes:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

La actualización de Direct3D 10.1 también incluía las siguientes estructuras adicionales:

-   [**D3D10 \_ RENDER \_ TARGET \_ BLEND \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**VISTA DESC1 DEL RECURSO \_ \_ DEL SOMBREADOR \_ \_ D3D10**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

La API de Direct3D 10.1 incluye un nuevo concepto denominado nivel de característica. Este concepto significa que puede usar la API de Direct3D 10.1 para impulsar el hardware Direct3D 10.0 ([**D3D10 \_ FEATURE \_ LEVEL \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) o Direct3D 10.1 ([**D3D10 \_ FEATURE LEVEL \_ \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)). Dado que la API de Direct3D 10.1 se deriva de las interfaces de Direct3D 10, las aplicaciones pueden crear un dispositivo Direct3D 10.1 y, a continuación, usarlo como un dispositivo Direct3D 10.0, excepto cuando se necesitan nuevas características específicas de 10.1 (siempre que el nivel de característica **D3D10 \_ FEATURE \_ LEVEL \_ \_ 10 1** esté presente y admita estas características).

> [!Note]  
> Los dispositivos Direct3D 10.1 pueden usar los perfiles de sombreador HLSL existentes (frente a \_ 4 \_ 0, ps 4 0, gs 4 0) y los nuevos perfiles \_ \_ \_ \_ 10.1 (frente a \_ 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 1) \_ con instrucciones y funcionalidades adicionales de HLSL.

 

Windows 7 contenía una actualización secundaria de la API de Direct3D 10.1 que se incluye en el entorno de ejecución de Direct3D 11. Esta actualización agrega compatibilidad con los siguientes niveles de características:

-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 también agregó compatibilidad con Direct3D 10.1 para Windows [Advanced Rasterization Platform (WARP).](../direct3darticles/directx-warp.md) Puede especificar un controlador WARP mediante [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Para obtener más información sobre Direct3D 10.1, vea Características de [Direct3D 10.1](d3d10-graphics-programming-guide-10-1.md) y la [**enumeración D3D10 \_ FEATURE \_ LEVEL1.**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
