---
description: En la página siguiente se proporciona un esquema básico de las diferencias principales entre Direct3D 9 y Direct3D 10. En el siguiente esquema se proporciona información para ayudar a los desarrolladores con la experiencia de Direct3D 9 a explorar y relacionar con Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Consideraciones de Direct3D 9 a Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467ceefe7784a9b408bb36c8bed13217cb6de7c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807166"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Consideraciones de Direct3D 9 a Direct3D 10 (Direct3D 10)

En la página siguiente se proporciona un esquema básico de las diferencias principales entre Direct3D 9 y Direct3D 10. En el siguiente esquema se proporciona información para ayudar a los desarrolladores con la experiencia de Direct3D 9 a explorar y relacionar con Direct3D 10.

Aunque la información de este tema compara Direct3D 9 con Direct3D 10, ya que Direct3D 11 se basa en las mejoras realizadas en Direct3D 10 y 10,1, también necesitará esta información para migrar de Direct3D 9 a Direct3D 11. Para obtener información sobre cómo moverse más allá de Direct3D 10 a Direct3D 11, vea [migrar a Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Información general sobre los principales cambios estructurales en Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Eliminación de la función Fixed](#removal-of-fixed-function)
    -   [Validación del tiempo de creación de objetos de dispositivo](#device-object-creation-time-validation)
-   [Abstracciones/separación del motor](/windows)
    -   [Eliminación directa de dependencias de Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Trucos para resolver rápidamente problemas de compilación de la aplicación](#tricks-for-quickly-resolving-application-build-issues)
    -   [Reemplazar tipos de Direct3D 9](#overriding-direct3d-9-types)
    -   [Resolver problemas de vínculos](#resolving-link-issues)
    -   [Simular Cap de dispositivo](#simulating-device-caps)
-   [Conducción de la API de Direct3D 10](#driving-the-direct3d-10-api)
    -   [Creación de recursos](#resource-creation)
    -   [Vistas](#views)
    -   [Acceso a recursos estáticos y dinámicos](#static-versus-dynamic-resource-access)
    -   [Efectos de Direct3D 10](#direct3d-10-effects)
    -   [HLSL sin efectos](#hlsl-without-effects)
    -   [Compilación del sombreador](#shader-compilation)
    -   [Creación de recursos del sombreador](#creation-of-shader-resources)
    -   [Interfaz de capa de reflexión del sombreador](#shader-reflection-layer-interface)
    -   [Diseños de ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada](/windows)
    -   [Impacto de la eliminación de código inactivo del sombreador](#impact-of-shader-dead-code-removal)
    -   [Ejemplo de estructura de entrada del sombreador de vértices](#vertex-shader-input-structure-example)
    -   [Creación de objetos de estado](#state-object-creation)
-   [Trasladar texturas](#porting-textures)
    -   [Formatos de archivo admitidos](#file-formats-supported)
    -   [Asignar formatos de textura](#mapping-texture-formats)
-   [Trasladar sombreadores](#porting-shaders)
    -   [Los sombreadores de Direct3D 10 se crean en HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Firma y vinculación del sombreador](#shader-signatures-and-linkage)
    -   [Vinculaciones de fases del sombreador HLSL](#hlsl-shader-stage-linkages)
    -   [Búferes de constantes](#constant-buffers)
    -   [Planos de clip de usuario en HLSL en el nivel de característica 9 y versiones posteriores](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Diferencias adicionales de Direct3D 10 que se deben supervisar](#additional-direct3d-10-differences-to-watch-for)
    -   [Enteros como entrada](#integers-as-input)
    -   [Cursores del mouse](#mouse-cursors)
    -   [Asignar textura a píxeles en Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Cambios de comportamiento de recuento de referencias](#reference-counting-behavior-changes)
    -   [Probar el nivel cooperativo](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Diferencias de Direct3D 10,1 adicionales](#additional-direct3d-101-differences)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Información general sobre los principales cambios estructurales en Direct3D 10

-   [Eliminación de la función Fixed](#removal-of-fixed-function)
-   [Validación del tiempo de creación de objetos de dispositivo](#device-object-creation-time-validation)

El proceso de representación mediante el dispositivo Direct3D 10 es estructuralmente similar a Direct3D 9.

-   Establecer un origen de flujo de vértices
-   Establecer el diseño de entrada en Direct3D 10 (establecer la declaración de flujo de vértices en Direct3D 9)
-   Declarar topología primitiva
-   Establecer texturas
-   Establecer objetos de estado
-   Establecer sombreadores
-   Dibujar

La llamada a [**Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) enlaza las operaciones entre sí; el orden de las llamadas antes de la llamada a Draw es arbitrario. Las principales diferencias en el diseño de la API de Direct3D 10 son las siguientes:

-   Eliminación de la función Fixed
-   Eliminación de bits Cap: se garantiza el conjunto de características base de Direct3D 10.
-   Administración más estricta de: acceso a los recursos, estado del dispositivo, constantes del sombreador, vinculación del sombreador (entradas y salidas a los sombreadores) entre fases
-   Los cambios de nombre de punto de entrada de API reflejan el uso de la memoria virtual GPU (MAP () en lugar de Lock ()).
-   Se puede Agregar una capa de depuración al dispositivo en el momento de su creación
-   La topología primitiva es ahora un estado explícito (separado de la llamada a [**Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) )
-   Las constantes de sombreador explícitas se almacenan ahora en búferes de constantes
-   La creación del sombreador se realiza completamente en HLSL. El compilador de HLSL ahora reside en la DLL principal de Direct3D 10.
-   Nueva fase programable: sombreador de geometría
-   Eliminación de BeginScene ()/EndScene ()
-   Funcionalidad común de 2D, enfoque y administración de adaptadores implementada en un nuevo componente: DXGI

### <a name="removal-of-fixed-function"></a>Eliminación de la función Fixed

A veces es sorprendente que incluso en un motor de Direct3D 9 que aprovecha totalmente la canalización programable, queda una serie de áreas que dependen de la canalización de función fija (FF). Las áreas más comunes suelen estar relacionadas con la representación alineada del espacio de pantalla para la interfaz de usuario. Por esta razón, es probable que tenga que crear un sombreador de emulación FF o un conjunto de sombreadores que proporcionen los comportamientos de reemplazo necesarios.

En esta documentación se incluyen notas del producto que contienen orígenes de sombreador de reemplazo para los comportamientos FF más comunes (vea el ejemplo de la UME de la [función fija](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Algunos comportamientos de píxeles de función fija, incluida la prueba alfa, se han pasado en sombreadores.

### <a name="device-object-creation-time-validation"></a>Validación del tiempo de creación de objetos de dispositivo

La canalización de Direct3D 10 se ha rediseñado desde el principio del hardware y el software con una intención principal de reducir la sobrecarga de la CPU (en el momento del dibujo). Para reducir los costos, a todos los tipos de datos del dispositivo se les ha asignado un objeto con métodos de creación explícitos proporcionados por el propio dispositivo. Esto permite la validación de datos estricta en el momento de la creación de objetos en lugar de durante la llamada a Draw, tal y como se hace con Direct3D 9.

## <a name="engine-abstractions--separation"></a>Abstracciones/separación del motor

Las aplicaciones, incluidos los juegos, que desean admitir Direct3D 9 y Direct3D 10 deben tener las capas de representación abstraedas del resto de la base de código. Hay muchas maneras de lograrlo, pero la clave de todos ellos es el diseño de la capa de abstracción para el dispositivo Direct3D de nivel inferior. Todos los sistemas deben comunicarse con el hardware a través de la capa común que se ha diseñado para proporcionar recursos de GPU y administración de tipos de bajo nivel.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Eliminación directa de dependencias de Direct3D 9

Al migrar bases de código grandes y probadas previamente, es importante minimizar la cantidad de cambios de código a los que son absolutamente necesarios para conservar los comportamientos previamente probados en el código. Los procedimientos recomendados incluyen documentar claramente dónde cambian los elementos mediante Comentarios. A menudo resulta útil tener un estándar de comentarios para este trabajo que permite una navegación rápida a través del código base.

A continuación se muestra una lista de ejemplos de comentarios de bloque de inicio o de línea única estándar que se pueden usar para este trabajo.



| Elemento                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 QUITAdo<br/>                     | Se usa para quitar líneas o bloques de código<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 necesita actualización<br/> | Ayuda a agregar notas adicionales al comentario de necesidad de actualización que sugiere qué trabajo o nueva API debe usarse para las visitas posteriores al código para la conversión de comportamiento. El uso intensivo de Assert (**false**) también debe usarse en los casos en que \\ \\ se produce la actualización de Direct3D 10 para asegurarse de no tener conocimientos de ejecutar código errante<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 cambiado<br/>                     | Las áreas en las que se han producido cambios importantes deben conservarse para futuras referencias pero comentarse<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>FIN de Direct3D 10<br/>                                     | Calificador de bloque de código final<br/>                                                                                                                                                                                                                                                                                            |



 

En el caso de varias líneas de código fuente, debe usar también el estilo C/ \* \* comentarios, pero agregue los comentarios de inicio y fin relevantes en torno a estas áreas.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Trucos para resolver rápidamente problemas de compilación de la aplicación

-   [Reemplazar tipos de Direct3D 9](#overriding-direct3d-9-types)
-   [Resolver problemas de vínculos](#resolving-link-issues)
-   [Simular Cap de dispositivo](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Reemplazar tipos de Direct3D 9

Puede ser útil insertar un archivo de encabezado de alto nivel que contenga definiciones de tipos o invalidaciones para los tipos base de Direct3D 9 que ya no son compatibles con los encabezados de Direct3D 10. Esto le ayudará a minimizar la cantidad de cambios en el código y las interfaces en las que hay una asignación directa desde un tipo de Direct3D 9 al tipo de Direct3D 10 recién definido. Este enfoque también es útil para mantener juntos los comportamientos de código en un archivo de código fuente. En este caso, es una buena idea definir tipos con nombre neutros o en general que describen las construcciones comunes que se usan para la representación, pero que aún abarcan las API de Direct3D 9 y Direct3D 10. Por ejemplo:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Otros ejemplos específicos de Direct3D 10 incluyen:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Resolver problemas de vínculos

Es aconsejable desarrollar aplicaciones de Direct3D 10 y Windows Vista con la versión más reciente de Microsoft Visual Studio. Sin embargo, es posible compilar una aplicación de Windows Vista que depende de Direct3D 10 con la versión anterior 2003 de Visual Studio. Direct3D 10 es un componente de la plataforma de Windows Vista que tiene dependencias (como con el SDK de la plataforma Server 2003 SP1) en el siguiente lib: BufferOverflowU. lib es necesario para resolver cualquier \_ problema del enlazador de comprobación de seguridad del búfer.

### <a name="simulating-device-caps"></a>Simular Cap de dispositivo

Muchas aplicaciones contienen áreas de código que dependen de que los datos de los Cap del dispositivo estén disponibles. Para solucionar este riesgo, invalide la enumeración de dispositivos y fuerce los límites de dispositivo a valores razonables. Tenga previsto volver a visitar las áreas en las que hay dependencias en Cap más adelante para la eliminación completa de los TOPEs siempre que sea posible.

## <a name="driving-the-direct3d-10-api"></a>Conducción de la API de Direct3D 10

Esta sección se centra en los cambios de comportamiento causados por la API de Direct3D 10.

-   [Creación de recursos](#resource-creation)
-   [Vistas](#views)
-   [Acceso a recursos estáticos y dinámicos](#static-versus-dynamic-resource-access)
-   [Efectos de Direct3D 10](#direct3d-10-effects)
-   [HLSL sin efectos](#hlsl-without-effects)
-   [Compilación del sombreador](#shader-compilation)
-   [Creación de recursos del sombreador](#creation-of-shader-resources)
-   [Interfaz de capa de reflexión del sombreador](#shader-reflection-layer-interface)
-   [Diseños de ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada](/windows)
-   [Impacto de la eliminación de código inactivo del sombreador](#impact-of-shader-dead-code-removal)
-   [Ejemplo de estructura de entrada del sombreador de vértices](#vertex-shader-input-structure-example)
-   [Creación de objetos de estado](#state-object-creation)

### <a name="resource-creation"></a>Creación de recursos

La API de Direct3D 10 ha diseñado recursos como tipos de búfer genéricos que tienen marcas de enlace específicas según el uso planeado. Se eligió este punto de diseño para facilitar el acceso casi omnipresente de los recursos de la canalización para escenarios como la representación en un búfer de vértices y, a continuación, se dibujan los resultados al instante sin interrumpir la CPU. En el ejemplo siguiente se muestra la asignación de búferes de vértices y del búfer de índice donde puede ver que la descripción del recurso solo difiere en las marcas de enlace del recurso de GPU.

La API de Direct3D 10 ha proporcionado métodos auxiliares de texturas para crear explícitamente recursos de tipo de textura, pero como puede imaginar, son realmente funciones auxiliares.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Cuando el destino es Direct3D 10, es probable que desee asignar más elementos durante el tiempo de creación del recurso que se usa con Direct3D 9. Esto se hará más evidente con la creación de búferes de destino de representación y texturas, donde también debe crear una vista para tener acceso al búfer y configurar el recurso en el dispositivo.

[Tutorial 1: conceptos básicos de Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 y versiones posteriores de Direct3D amplían el formato de archivo DDS para admitir nuevos formatos de DXGI, matrices de texturas y matrices de mapas de cubos. Para obtener más información acerca de la extensión de formato de archivo DDS, consulte la [Guía de programación para DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Vistas

Una vista es una interfaz de datos con tipo específica que se almacena en un búfer de píxeles. Un recurso puede tener varias vistas asignadas a la vez y esta característica se resalta en el ejemplo de representación de un solo paso en el mapa contenido en este SDK.

[Página guía de programadores sobre el acceso a los recursos](d3d10-graphics-programming-guide-resources-access-views.md)

[Ejemplo de mapa](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Acceso a recursos estáticos y dinámicos

Para obtener el mejor rendimiento, las aplicaciones deben particionar el uso de sus datos en función de la naturaleza estática y dinámica de los datos. Direct3D 10 se ha diseñado para aprovechar las ventajas de este enfoque y, por lo tanto, las reglas de acceso para los recursos se han mejorado considerablemente en Direct3D 9. En el caso de los recursos estáticos, debe rellenar idealmente el recurso con sus datos durante el tiempo de creación. Si el motor se ha diseñado en torno al punto de diseño de creación, bloqueo, relleno y desbloqueo de Direct3D 9, puede aplazar el rellenado a partir de la hora de creación mediante un recurso de almacenamiento provisional y el método UpdateSubResource en la interfaz de recursos.

### <a name="direct3d-10-effects"></a>Efectos de Direct3D 10

El uso del sistema de efectos de Direct3D 10 está fuera del ámbito de este artículo. El sistema se ha escrito para sacar el máximo partido de las ventajas arquitectónicas que proporciona Direct3D 10. Vea la sección [efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) para obtener más detalles sobre su uso.

### <a name="hlsl-without-effects"></a>HLSL sin efectos

La canalización del sombreador de Direct3D 10 se puede controlar sin el uso del sistema de efectos de Direct3D 10. Tenga en cuenta que, en esta instancia, todos los búferes de constantes, sombreadores, muestras y enlaces de textura deben ser administrados por la propia aplicación. Vea el vínculo de ejemplo y las siguientes secciones de este documento para obtener más detalles:

[Ejemplo de HLSL sin efectos](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilación del sombreador

El compilador de HLSL de Direct3D 10 aporta mejoras a la definición del lenguaje HLSL y, por tanto, tiene la capacidad de funcionar en dos modos. Para ofrecer compatibilidad total con las funciones intrínsecas de estilo de Direct3D 9 y la semántica, la compilación se debe invocar mediante la marca del modo de compatibilidad que se puede especificar en cada compilación.

La semántica del lenguaje HLSL específica 4,0 y las funciones intrínsecas de Direct3D 10 pueden encontrarse en [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Los principales cambios en la sintaxis de HLSL de Direct3D 9 para sacar el máximo provecho de se encuentran en el área de acceso a textura. La nueva sintaxis es el único formulario admitido por el compilador fuera del modo de compatibilidad.

> [!Note]  
> Los tiempos de ejecución de Direct3D 10, 10,1 y 11 que se ejecutan en Windows Vista y versiones posteriores proporcionan las API de tipo de compilador de Direct3D 10 ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) y [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)). Las API de tipo de compilador de Direct3D 10 tienen la misma funcionalidad que el compilador de HLSL que se incluye en el SDK de DirectX (diciembre 2006). Este compilador de HLSL no admite los perfiles de Direct3D 10,1 (vs \_ 4 \_ 1, PS \_ 4 1 \_ , GS \_ 4 \_ 1, FX \_ 4 \_ 1) y le falta una serie de optimizaciones y mejoras. Puede obtener un compilador de HLSL que admita los perfiles de Direct3D 10,1 desde la última versión heredada del [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)). Para obtener información sobre el SDK de DirectX heredado, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md). Puede obtener el último compilador de línea de comandos de HLSL Fxc.exe y las API de [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) desde el Windows SDK.

 

### <a name="creation-of-shader-resources"></a>Creación de recursos del sombreador

La creación de instancias de sombreador compiladas fuera del sistema de efectos de Direct3D 10 se realiza de forma muy similar a Direct3D 9, sin embargo, en Direct3D 10, es importante mantener la firma de entrada del sombreador para su uso posterior. La firma se devuelve de forma predeterminada como parte del BLOB del sombreador, pero se puede extraer para reducir los requisitos de memoria si es necesario. Para obtener más información, vea [usar sombreadores en Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Interfaz de capa de reflexión del sombreador

La capa de reflexión del sombreador es la interfaz por la que se puede obtener información sobre los requisitos del sombreador. Esto es especialmente útil cuando se crean vinculaciones de ensamblado de entrada (vea más abajo), donde puede ser necesario atravesar los requisitos de entrada del sombreador para asegurarse de que se proporciona la estructura de entrada correcta al sombreador. Puede crear una instancia de la interfaz de nivel de reflexión al mismo tiempo que la creación de una instancia de un sombreador compilado.

La capa de reflexión del sombreador reemplaza los métodos D3DX9 que proporcionan una funcionalidad similar. Por ejemplo, [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) se reemplaza por el método [**GetDesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) .

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Diseños de ensamblador de entrada: sombreador de vértices/vinculación de flujo de entrada

El ensamblador de entrada (IA) reemplaza a la declaración de secuencia de vértices de estilo de Direct3D 9 y su estructura de descripción es muy similar en el formulario. La principal diferencia que el IA aporta es que el objeto de diseño del IA creado debe asignarse directamente a un formato específico de la firma de entrada del sombreador. El objeto de asignación creado para vincular el flujo de entrada con el sombreador se puede usar en cualquier número de sombreadores en los que la firma de entrada del sombreador coincida con la del sombreador utilizado para crear el diseño de entrada.

Para impulsar mejor la canalización con datos estáticos, debe tener en cuenta las permutaciones del formato de flujo de entrada a posibles firmas de entrada del sombreador y crear las instancias del objeto de diseño de IA tan pronto como sea posible y reutilizarlas siempre que sea posible.

### <a name="impact-of-shader-dead-code-removal"></a>Impacto de la eliminación de código inactivo del sombreador

En la siguiente sección se detallan una diferencia significativa entre Direct3D 9 y Direct3D 10 que es probable que requiera un cuidadoso control en el código del motor. Los sombreadores que contienen expresiones condicionales a menudo tienen algunas rutas de acceso de código que se han quitado como parte del proceso de compilación. En Direct3D 9, se pueden quitar dos tipos de entradas (marcadas para su eliminación) cuando no se usan: entradas de firma (como en el ejemplo siguiente) y entradas constantes. Si el final del búfer de constantes contiene entradas no utilizadas, la declaración de tamaño del sombreador reflejará el tamaño del búfer de constantes sin las entradas no utilizadas al final. Ambos tipos de entradas permanecen en las firmas o en los búferes de constantes Direct3D 10 con una excepción especial en el caso de las entradas constantes sin usar al final de un búfer de constantes. Esto puede tener un impacto en el motor al administrar sombreadores grandes y crear diseños de entrada. Los elementos que se quitan mediante optimizaciones de código muerto en el compilador todavía se deben declarar en la estructura de entrada. En el siguiente ejemplo se muestra esto:

### <a name="vertex-shader-input-structure-example"></a>Ejemplo de estructura de entrada del sombreador de vértices


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* La eliminación de código no muerto de Direct3D 9 quitaría la declaración en el sombreador debido a la eliminación de código inactivo condicional


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



También podría hacer que sea más obvio que la constante es una constante de tiempo de compilación con la siguiente declaración:


```
#define LIGHT_MAPPED false
```



En el ejemplo anterior, en Direct3D 9, el elemento UV2 se quitaría debido a las optimizaciones de código inactivo en el compilador. En Direct3D 10, el código muerto todavía se quitará, pero el diseño del ensamblador de entrada del sombreador requiere que exista la definición de los datos de entrada. La capa de reflexión del sombreador proporciona los medios para controlar esta situación de forma genérica, por lo que puede atravesar los requisitos de entrada del sombreador y asegurarse de proporcionar una descripción completa del flujo de entrada a la asignación de firma del sombreador.

A continuación se muestra una función de ejemplo para detectar la existencia de un índice o nombre semántico en una firma de función:


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

Al trasladar el código del motor, puede ser útil usar inicialmente un conjunto predeterminado de objetos de estado y deshabilitar todos los valores de estado de representación/estado de textura de Direct3D 9. Esto provocará artefactos de representación, pero es la forma más rápida de poner todo en marcha. Posteriormente, puede construir un sistema de administración de objetos de estado que puede usar una clave compuesta para permitir la reutilización máxima del número de objetos de estado que se usan.

## <a name="porting-textures"></a>Trasladar texturas

### <a name="file-formats-supported"></a>Formatos de archivo admitidos

Las funciones **D3DXxxCreateXXX** y **D3DXxxSaveXXX** que crean o guardan una textura de o en un archivo de gráficos (por ejemplo, [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) admiten un conjunto diferente de formatos de archivo en Direct3D 10 que en Direct3D 9:



| Formato de archivo | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| . ppm        | x          |             |
| .dib        | x          |             |
| . HDR        | x          |             |
| . PFM        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Para obtener más información, compare las enumeraciones de formato de archivo D3DXIMAGE de Direct3D 9 con las enumeraciones de [**\_**](../direct3d9/d3dximage-fileformat.md) formato de archivo de imagen de D3DX10 para Direct3D 10. [**\_ \_ \_**](d3dx10-image-file-format.md)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8. Para el procesamiento de archivos de textura, se recomienda usar [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Asignar formatos de textura

En la tabla siguiente se muestra la asignación de formatos de textura de Direct3D 9 a Direct3D 10. Cualquier contenido en los formatos que no esté disponible en DXGI tendrá que ser convertido por rutinas de utilidad.



| Formato de Direct3D 9                   | Formato de Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ desconocido                     | formato de DXGI \_ \_ desconocido                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | Formato \_ dxgi \_ B8G8R8A8 \_ UNORM & \_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | Formato \_ dxgi \_ B8G8R8X8 \_ UNORM & \_ formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | Formato de DXGI \_ \_ B5G6R5 \_ UNORM ²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | Formato de DXGI \_ \_ B5G5R5A1 \_ UNORM ²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | Formato de DXGI \_ \_ B4G4R4A4 \_ UNORM ³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | Formato de DXGI \_ \_ a8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | Formato de DXGI \_ \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | Formato \_ dxgi \_ R8G8B8A8 \_ UNORM & \_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | Formato de DXGI \_ \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | Formato de DXGI \_ \_ R8 \_ UNORM Nota: use. r swizzle en el sombreador para duplicar el color rojo en otros componentes para obtener el comportamiento de D3D9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | Formato de DXGI \_ \_ R8G8 \_ UNORM Nota: Use swizzle. rrrg en el sombreador para duplicar rojo y desplace el color verde a los componentes alfa para obtener el comportamiento de D3D9.                                                                                                            |
| D3DFMT \_ A4L4                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | Formato de DXGI \_ \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | Formato de DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ format \_ G8R8 \_ G8B8 \_ UNORM (en DX9 los datos se escalaron verticalmente con 255.0 f, pero esto se puede controlar en el código del sombreador).                                                                                                                                   |
| D3DFMT \_ YUY2                        | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ format \_ R8G8 \_ B8G8 \_ UNORM (en DX9 los datos se escalaron verticalmente con 255.0 f, pero esto se puede controlar en el código del sombreador).                                                                                                                                   |
| D3DFMT \_ DXT1                        | Formato \_ dxgi \_ BC1 \_ UNORM & \_ formato dxgi \_ BC1 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ format \_ BC1 \_ UNORM & formato de dxgi \_ \_ BC1 \_ UNORM \_ sRGB Note: DXT1 y DXT2 son los mismos desde una perspectiva de API/hardware... solo la diferencia fue "alfa premultiplicada", que puede ser rastreada por una aplicación y no necesita un formato independiente. |
| D3DFMT \_ DXT3                        | Formato \_ dxgi \_ BC2 \_ UNORM & \_ formato dxgi \_ BC2 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ format \_ BC2 \_ UNORM & formato de dxgi \_ \_ BC2 \_ UNORM \_ sRGB Note: DXT3 y DXT4 son los mismos desde una perspectiva de API/hardware... solo la diferencia fue "alfa premultiplicada", que puede ser rastreada por una aplicación y no necesita un formato independiente. |
| D3DFMT \_ DXT5                        | Formato \_ dxgi \_ BC3 \_ UNORM & \_ formato dxgi \_ BC3 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ bloqueable | Formato de DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | Formato de DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ bloqueable              | Formato de DXGI \_ \_ D32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI \_ format \_ R16 \_ UNORM Nota: use. r swizzle en Shader para duplicar de rojo en otros componentes para obtener el comportamiento de D3D9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | Formato de DXGI \_ \_ R16 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | Formato de DXGI \_ \_ R32 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | No disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | Formato de DXGI \_ \_ R16 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | Formato de DXGI \_ \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | Formato de DXGI \_ \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | Formato de DXGI \_ \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | Formato de DXGI \_ \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | Formato de DXGI \_ \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | Formato de DXGI \_ \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | Formato de DXGI \_ \_ R32G32B32 \_ float                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | Formato de DXGI \_ \_ R8G8B8A8 \_ uint Nota: el sombreador obtiene valores uint, pero si se necesitan flotantes de estilo de Direct3D 9 (0,0 f, 1,0 f... 255. f), UINT solo se puede convertir a float32 en el sombreador.                                                               |
| D3DDECLTYPE \_ SHORT2                 | Formato de DXGI \_ \_ R16G16 \_ Sint Nota: el sombreador obtiene valores de Sint, pero si se necesitan flotantes de estilo de Direct3D 9, el valor de Sint solo se puede convertir a float32 en el sombreador.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | Formato de DXGI \_ \_ R16G16B16A16 \_ Sint Nota: el sombreador obtiene valores de Sint, pero si se necesitan flotantes de estilo de Direct3D 9, el valor de Sint solo se puede convertir a float32 en el sombreador.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | Formato de DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | Formato de DXGI \_ \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | No disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | Formato de DXGI \_ \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | Formato de DXGI \_ \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | Formato de DXGI \_ \_ las texturas BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | Formato de DXGI \_ \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹ DXGI 1,1, que se incluye en el tiempo de ejecución de Direct3D 11, incluye formatos BGRA. Sin embargo, la compatibilidad con estos formatos es opcional para los dispositivos de Direct3D 10 y 10,1 con los controladores que se implementan en el modelo de controladores de pantalla (WDDM) de Windows Vista (WDDM 1,0). Considere la posibilidad de usar el formato de DXGI \_ \_ R8G8B8A8 \_ UNORM en su lugar. Como alternativa, puede crear el dispositivo con [**D3D10 \_ Create \_ Device \_ BGRA \_ support**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) para asegurarse de que solo se admiten equipos con el tiempo de ejecución de Direct3D 11,0 y un controlador WDDM 1,1 o superior instalado.

² DXGI 1,0 Defined formatos 5:6:5 y 5:5:5:1, pero el tiempo de ejecución de Direct3D 10. x o Direct3D 11,0 no los admitía. Opcionalmente, estos formatos se admiten con DXGI 1,2 en el tiempo de ejecución de DirectX 11,1, que es necesario para los adaptadores de vídeo de nivel de característica 11,1 y los controladores WDDM 1,2 (Display Driver Model a partir de Windows 8) y ya se admiten en los niveles de características de 10level9.

³ DXGI 1,2 presentó el formato 4:4:4:4. Opcionalmente, este formato se admite en el tiempo de ejecución de DirectX 11,1, que es necesario para los adaptadores de vídeo 11,1 de nivel de característica y los controladores WDDM 1,2, y ya se admiten en los niveles de características de 10level9.

En el caso de los formatos sin comprimir, DXGI ha limitado la compatibilidad con patrones de formato de píxeles arbitrarios; todos los formatos sin comprimir deben ser del tipo RGBA. Esto puede requerir permutación de los formatos de píxel de los recursos existentes, lo que se recomienda para calcular como un paso de preprocesamiento sin conexión siempre que sea posible.

## <a name="porting-shaders"></a>Trasladar sombreadores

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Los sombreadores de Direct3D 10 se crean en HLSL

Direct3D 10 limita el uso del lenguaje de ensamblado a solo con fines de depuración, por lo que cualquier sombreador de ensamblado escrito a mano que se use en Direct3D 9 deberá convertirse a HLSL.

### <a name="shader-signatures-and-linkage"></a>Firma y vinculación del sombreador

Analizamos los requisitos para la vinculación de ensamblados de entrada a las firmas de entrada del sombreador de vértices anteriormente en este documento (consulte más arriba). Tenga en cuenta que el tiempo de ejecución de Direct3D 10 también ha restringido los requisitos para la vinculación de fase a fase entre los sombreadores. Este cambio afectará a los orígenes del sombreador en los que es posible que el enlace entre fases no se haya descrito completamente en Direct3D 9. Por ejemplo:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Vinculación VS-PS interrumpida: aunque es posible que el sombreador de píxeles no esté interesado en la matriz completa, la vinculación debe especificar el float4x3 completo.

Tenga en cuenta que la semántica de vinculación entre fases debe coincidir exactamente, sin embargo, las entradas de las fases de destino pueden ser un prefijo de los valores que se van a generar. En el ejemplo anterior, el sombreador de píxeles podría tener Position y texcoord1 como las únicas entradas, pero no podía tener la posición y texcoord2 como las únicas entradas debido a las restricciones de ordenación.

### <a name="hlsl-shader-stage-linkages"></a>Vinculaciones de fases del sombreador HLSL

La vinculación entre los sombreadores puede producirse en cualquiera de los siguientes puntos de la canalización:

-   Ensamblador de entrada a sombreador de vértices
-   Sombreador de vértices para sombreador de píxeles
-   Sombreador de vértices para sombreador de geometría
-   Sombreador de vértices para transmitir la salida
-   Sombreador de geometría a sombreador de píxeles
-   Sombreador de geometría que se va a transmitir

### <a name="constant-buffers"></a>Búferes de constantes

Para facilitar la migración de contenido de Direct3D 9, un enfoque inicial de la administración constante fuera del sistema de efectos podría implicar la creación de un búfer de constante único que contenga todas las constantes necesarias. Es importante que el rendimiento ordene las constantes en búferes por la frecuencia de actualización esperada. Esta organización reducirá al mínimo la cantidad de conjuntos de constantes redundantes.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Planos de clip de usuario en HLSL en el nivel de característica 9 y versiones posteriores

A partir de Windows 8, puede usar el atributo de función **clipplanes** en una [declaración de función](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) HLSL en lugar de la [VP \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para que el sombreador funcione en el [nivel de característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x, así como en el \_ nivel de característica 10 y versiones posteriores. Para obtener más información, consulte [planos de clips de usuario en hardware de nivel de característica 9](../direct3dhlsl/user-clip-planes-on-10level9.md).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Diferencias adicionales de Direct3D 10 que se deben supervisar

### <a name="integers-as-input"></a>Enteros como entrada

En Direct3D 9, no había compatibilidad real con el hardware para tipos de datos enteros; sin embargo, el hardware de Direct3D 10 admite tipos enteros explícitos. Si tiene datos de punto flotante en el búfer de vértices, debe tener una entrada float. De lo contrario, un tipo entero será la representación del patrón de bits del valor de punto flotante. No se permite un tipo entero para una entrada de sombreador de píxeles a menos que el valor se marque para ninguna interpolación (vea [modificadores de interpolación](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursores del mouse

En versiones anteriores de Windows, las rutinas de cursor de mouse GDI estándar no funcionaban correctamente en todos los dispositivos exclusivos de pantalla completa. Se han agregado las API [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)y [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) para controlar estos casos. Dado que la versión de Windows Vista de GDI es totalmente compatible con las superficies de [DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) , no hay necesidad de esta API de cursor de mouse especializada, por lo que no hay ningún equivalente de Direct3D 10. En su lugar, las aplicaciones de Direct3D 10 deben usar las [rutinas de cursor de mouse GDI](../menurc/cursors.md) estándar para los cursores del mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Asignar textura a píxeles en Direct3D 10

En Direct3D 9, los centros de textura y los centros de píxeles estaban separados por una media unidad (consulte [asignación directa de textura a píxeles (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). En Direct3D 10, los centros de textura ya están en unidades de medio, por lo que no es necesario desplazar las coordenadas de vértices.

La representación de cuádruples de pantalla completa es más directa con Direct3D 10. Las cuádruples de pantalla completa se deben definir en clipspace (-1, 1) y simplemente pasar a través del sombreador de vértices sin cambios. De este modo, no es necesario volver a cargar el búfer de vértices cada vez que cambia la resolución de pantalla y no hay ningún trabajo adicional en el sombreador de píxeles para manipular las coordenadas de textura.

### <a name="reference-counting-behavior-changes"></a>Cambios de comportamiento de recuento de referencias

A diferencia de las versiones anteriores de Direct3D, las distintas funciones de conjunto no contendrán una referencia a los objetos de dispositivos. Esto significa que la aplicación debe asegurarse de que contiene una referencia en el objeto, siempre y cuando se desee enlazar ese objeto a la canalización. Cuando el recuento de referencias del objeto desciende a cero, el objeto se desenlazará de la canalización a medida que se destruya. Este estilo de retención de referencia también se conoce como una retención de referencia débil, por lo que cada ubicación de enlace del objeto de dispositivo contiene una referencia débil a la interfaz/objeto. A menos que se mencione explícitamente, se debe asumir este comportamiento para todos los métodos set. Cada vez que la destrucción de un objeto hace que un punto de enlace se establezca en **null** , la capa de depuración emitirá una advertencia. Tenga en cuenta que las llamadas a métodos Get de dispositivo, como [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) , aumentarán el recuento de referencias de los objetos que se devuelven.

### <a name="test-cooperative-level"></a>Probar el nivel cooperativo

La funcionalidad de la API [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) de Direct3D 9 es análoga a la configuración de la [prueba de DXGI \_ \_ presente](../direct3ddxgi/dxgi-present.md) cuando se llama a [**present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Una función similar al método [**IDirect3DDevice9:: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) de Direct3D 9 no está disponible en Direct3D 10 y 10,1. Para copiar superficies de recursos, use [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). En el caso de las operaciones de cambio de tamaño, se representa en una textura mediante el filtrado de textura. Para convertir superficies de MSAA en superficies que no son de MSAA, use [**ID3D10Device:: ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Diferencias de Direct3D 10,1 adicionales

Windows Vista con Service Pack 1 (SP1) incluía una actualización secundaria de Direct3D 10 y Direct3D 10,1, que exponía las siguientes características de hardware adicionales:

-   Sombreadores por ejemplo de MSAA
-   Lectura de profundidad de MSAA
-   Modos de mezcla independientes por destino de representación
-   Matrices de mapas de cubos
-   Representar en formatos de compresión de bloques (BC)

La actualización de Direct3D 10,1 agregó compatibilidad con las siguientes interfaces nuevas, que se derivan de las interfaces existentes:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

La actualización de Direct3D 10,1 también incluye las siguientes estructuras adicionales:

-   [**\_DESC1 de \_ mezcla de destino de representación D3D10 \_ \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**\_Vista de recursos del sombreador de D3D10 \_ \_ \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

La API de Direct3D 10,1 incluye un nuevo concepto denominado nivel de característica. Este concepto significa que puede usar la API de Direct3D 10,1 para impulsar el hardware de Direct3D 10,0 ([**nivel de característica de D3D10 \_ \_ \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) o Direct3D 10,1 ([**nivel de característica de D3D10 \_ \_ \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)). Dado que la API de Direct3D 10,1 se deriva de las interfaces de Direct3D 10, las aplicaciones pueden crear un dispositivo Direct3D 10,1 y usarlo como un dispositivo Direct3D 10,0, excepto cuando se necesitan nuevas características específicas de 10,1 (siempre que el nivel de características de **D3D10 de \_ nivel de característica \_ \_ 10 \_ 1** esté presente y admita estas características).

> [!Note]  
> Los dispositivos de Direct3D 10,1 pueden usar los perfiles de sombreador de HLSL de 10,0 existentes (vs \_ 4 \_ 0, PS 4 0 \_ \_ , GS \_ 4 \_ 0) y los nuevos perfiles de 10,1 (vs \_ 4 \_ 1, PS 4 1 \_ \_ , GS \_ 4 \_ 1) con otras funciones y instrucciones de HLSL.

 

Windows 7 contenía una actualización secundaria de la API de Direct3D 10,1 que se incluye en el tiempo de ejecución de Direct3D 11. Esta actualización agrega compatibilidad con los siguientes niveles de características:

-   [**Nivel de característica de D3D10 \_ \_ \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nivel de característica de D3D10 \_ \_ \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**Nivel de característica de D3D10 \_ \_ \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 también agregó compatibilidad con Direct3D 10,1 para la [plataforma de rasterización avanzada de Windows (warp)](../direct3darticles/directx-warp.md). Puede especificar un controlador de WARP con el [**\_ tipo de \_ controlador \_ D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Para obtener más información sobre Direct3D 10,1, vea [características de direct3d 10,1](d3d10-graphics-programming-guide-10-1.md) y la enumeración Level1 de la [**\_ característica \_ D3D10**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
