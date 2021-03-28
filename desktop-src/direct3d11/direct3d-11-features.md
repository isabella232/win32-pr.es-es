---
title: Características de Direct3D 11
description: La guía de programación contiene información sobre cómo usar la canalización programable de Direct3D 11 para crear gráficos 3D en tiempo real para juegos y aplicaciones científicas y de escritorio.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078579"
---
# <a name="direct3d-11-features"></a>Características de Direct3D 11

La guía de programación contiene información sobre cómo usar la canalización programable de Direct3D 11 para crear gráficos 3D en tiempo real para juegos y aplicaciones científicas y de escritorio.

-   [Sombreador de cálculo](#compute-shader)
-   [Vinculación dinámica del sombreador](#dynamic-shader-linking)
-   [Multithreading](#multithreading)
-   [Tesela](#tessellation)
-   [Lista completa de características](#full-listing-of-features)
-   [Características agregadas en versiones anteriores](#features-added-in-previous-releases)
-   [Temas relacionados](#related-topics)

## <a name="compute-shader"></a>Sombreador de cálculo

Un sombreador de cálculo es un sombreador programable diseñado para el procesamiento en paralelo de datos de uso general. En otras palabras, los sombreadores de cálculo permiten usar una GPU como un procesador paralelo de uso general. El sombreador de cálculo es similar a los demás sombreadores de canalización programables (como vértices, píxeles, geometría) en la forma en que tiene acceso a las entradas y salidas. La tecnología del sombreador de cálculo también se conoce como tecnología DirectCompute. Un sombreador de cálculo se integra en Direct3D y es accesible a través de un dispositivo Direct3D. Puede compartir directamente los recursos de memoria con los sombreadores de gráficos mediante el dispositivo Direct3D. Sin embargo, no está conectado directamente a otras fases del sombreador.

Un sombreador de cálculo está diseñado para aplicaciones de mercado masivo que realizan cálculos en tasas interactivas, cuando el costo de la transición entre la API (y su pila de software asociado) y una CPU consume demasiada sobrecarga.

Un sombreador de cálculo tiene su propio conjunto de Estados. Un sombreador de cálculo no tiene necesariamente una asignación forzada de 1-1 a los registros de entrada (por ejemplo, un sombreador de vértices) o a los registros de salida (como hace el sombreador de píxeles). Se admiten algunas características del sombreador de gráficos, pero otras se han quitado para que se puedan agregar nuevas características específicas del sombreador de proceso.

Para admitir las características específicas del sombreador de cálculo, ahora hay disponibles varios tipos de recursos nuevos, como los búferes de lectura/escritura, las texturas y los búferes estructurados.

Vea información [General sobre el sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md) para obtener información adicional.

## <a name="dynamic-shader-linking"></a>Vinculación dinámica del sombreador

Los sistemas de representación deben tener una gran complejidad al administrar los sombreadores, a la vez que proporcionan la oportunidad de optimizar el código del sombreador. Esto se convierte en un desafío aún mayor, ya que los sombreadores deben admitir una variedad de materiales diferentes en una escena representada en varias configuraciones de hardware. Para abordar este reto, los desarrolladores del sombreador suelen estar recurridos a uno de los dos enfoques generales. Han creado sombreadores grandes y de uso general de gran tamaño que se pueden usar en una amplia variedad de elementos de la escena, que componen un rendimiento para la flexibilidad, o crean sombreadores individuales para cada flujo de geometría, tipo de material o combinación de tipos de luz necesarios.

Estos sombreadores grandes de uso general controlan este desafío volviendo a compilar el mismo sombreador con diferentes definiciones de preprocesador, y el último método usa la capacidad del desarrollador de fuerza bruta para lograr el mismo resultado. La explosión de permutación del sombreador suele ser un problema para los desarrolladores que ahora deben administrar miles de permutaciones de sombreador diferentes dentro de su canalización de recursos y juegos.

Direct3D 11 y el modelo de sombreador 5 introducen construcciones de lenguaje orientado a objetos y proporcionan compatibilidad en tiempo de ejecución con la vinculación del sombreador para ayudar a los programadores a los sombreadores.

Consulte [vinculación dinámica](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) para obtener información adicional.

## <a name="multithreading"></a>Subprocesamiento múltiple

Muchas aplicaciones de gráficos están enlazadas a la CPU debido a actividades costosas como el recorrido del gráfico de escenas, la ordenación de objetos y las simulaciones físicas. Dado que los sistemas de varios núcleos están cada vez más disponibles, Direct3D 11 ha mejorado su compatibilidad con multithreading para permitir una interacción eficaz entre varios subprocesos de CPU y las API de gráficos D3D11.

Direct3D 11 permite que la siguiente funcionalidad admita el multithreading:

-   Los objetos simultáneos se crean ahora en subprocesos independientes, ya que las funciones de punto de entrada que crean objetos de subprocesamiento libre permiten que muchos subprocesos creen objetos simultáneamente. Por ejemplo, una aplicación puede ahora compilar un sombreador o cargar una textura en un subproceso mientras se representa en otro.
-   Las listas de comandos se pueden crear en varios subprocesos; una lista de comandos es una secuencia grabada de comandos de gráficos. Con Direct3D 11, puede crear listas de comandos en varios subprocesos de CPU, lo que permite atravesar en paralelo la base de datos de la escena o el procesamiento físico en varios subprocesos. Esto libera el subproceso de representación principal para enviar los búferes de comandos al hardware.

Vea [multithreading](overviews-direct3d-11-render-multi-thread.md) para obtener información adicional.

## <a name="tessellation"></a>Teselación

La teselación se puede usar para representar un modelo único con distintos niveles de detalle. Este enfoque genera un modelo más preciso geométricamente que depende del nivel de detalle necesario para una escena. Use teselación en una escena en la que el nivel de detalle permita un modelo de geometría inferior, lo que reduce la demanda de ancho de banda de memoria consumida durante la representación.

En Direct3D, la teselación se implementa en la GPU para calcular una superficie curva más suave a partir de una revisión de entrada gruesa (menos detallada). Cada cara de revisión (cuádruple o triángulo) se divide en caras triangulares más pequeñas que se aproximan mejor a la superficie deseada.

Para obtener información sobre la implementación de teselación en la canalización de gráficos, consulte [información general sobre teselación](direct3d-11-advanced-stages-tessellation.md).

## <a name="full-listing-of-features"></a>Lista completa de características

Esta es una lista completa de las características de Direct3D 11.

-   Puede ejecutar Direct3D 11 en el [hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md) especificar un [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) al crear un dispositivo.
-   Puede realizar teselación (consulte [información general sobre teselación](direct3d-11-advanced-stages-tessellation.md)) mediante los siguientes tipos de sombreador:

    -   Sombreador de casco
    -   Sombreador de dominios

-   Direct3D 11 admite multithreading (vea [multithreading](overviews-direct3d-11-render-multi-thread.md))

    -   Recursos multiproceso/sombreador/creación de objetos
    -   Creación de listas de visualización multiproceso

-   Direct3D 11 expande los sombreadores con las siguientes características (consulte [modelo de sombreador 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))

    -   Recursos direccionables: texturas, búferes de constantes y muestreadores
    -   Tipos de recursos adicionales, como búferes de lectura/escritura y texturas (vea [nuevos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)).
    -   Subrutinas
    -   Sombreador de cálculo (consulte [información general sobre el sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md)): un sombreador que acelera los cálculos dividiendo el espacio problemático entre varios subprocesos de software o grupos de subprocesos, y compartiendo datos entre los registros del sombreador para reducir de forma significativa la cantidad de datos necesarios para la entrada en un sombreador. Entre los algoritmos que el sombreador de cálculo puede mejorar significativamente se incluyen el procesamiento posterior, la animación, la física y la inteligencia artificial.
    -   Sombreador de geometría (vea [características del sombreador de geometría](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))

        -   Instancing: permite que el sombreador de geometría genere un máximo de 1024 vértices, o cualquier combinación de instancias y vértices hasta 1024 (el máximo de 32 instancias de los vértices 32 cada uno).

    -   Sombreador de píxeles

        -   Cobertura como entrada de PS
        -   Interpolación programable de entradas: el sombreador de píxeles puede evaluar atributos dentro del píxel, en cualquier lugar de la cuadrícula de ejemplo múltiple
        -   El muestreo centroide de los atributos debe obedecer las siguientes reglas:

            -   Si se incluyen todas las muestras de la primitiva, el atributo se evalúa en el centro de píxeles independientemente de si el patrón de ejemplo tiene una ubicación de ejemplo en el centro de píxeles.
            -   De lo contrario, el atributo se evalúa en el primer ejemplo descrito, es decir, el ejemplo con el índice más bajo entre todos los índices de ejemplo. En esta situación, la cobertura de ejemplo se determina después de aplicar la operación AND lógica a la cobertura y el estado de rasterizador de la máscara de ejemplo.
            -   Si no se cubre ningún ejemplo (por ejemplo, en los píxeles de la aplicación auxiliar que se ejecutan fuera de los límites de un primitivo para rellenar las marcas de un píxel de 2x2), el atributo se evalúa de una de las siguientes maneras:

                -   Si el estado del rasterizador de la máscara de ejemplo es un subconjunto de los ejemplos del píxel, el primer ejemplo que está incluido en el estado del rasterizador de la máscara de ejemplo es el punto de evaluación.
                -   De lo contrario, en la condición de máscara de muestra completa, el centro de píxeles es el punto de evaluación.

-   Direct3D 11 expande las texturas (consulte [información general sobre las texturas](overviews-direct3d-11-resources-textures.md)) con las siguientes características

    -   Gather4

        -   Compatibilidad con texturas de varios componentes: especifique un canal desde el que cargar
        -   Compatibilidad con desplazamientos programables

    -   Streaming

        -   Abrazaderas de textura para limitar la precarga de WDDM

    -   16 000 límites de textura
    -   Requerir 8 bits de subtexel y precisión de sub-MIP en el filtrado de texturas
    -   Nuevos formatos de compresión de textura (1 nuevo formato de LDR y 1 nuevo formato HDR)

-   Direct3D 11 admite oDepth conservador: este algoritmo permite a un sombreador de píxeles comparar el valor de profundidad por píxel del sombreador de píxeles con el del rasterizador. El resultado habilita las operaciones de selección de profundidad tempranas y mantiene la capacidad de generar oDepth desde un sombreador de píxeles.
-   Direct3D 11 admite memoria grande

    -   Permitir recursos > 4 GB
    -   Mantener los índices de recursos de 32 bits, pero el recurso es más grande

-   Direct3D 11 admite mejoras en la salida de flujo

    -   Salida de flujo direccionable
    -   Aumentar el número de salidas de Stream a 4
    -   Cambiar todos los búferes de salida de flujo para que sean de varios elementos

-   Direct3D 11 admite el modelo de sombreador 5 (consulte [modelo de sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Double con desnormaciones
    -   Instrucción de conjunto de bits de recuento
    -   Buscar instrucción de primer bit set
    -   Control de transporte/desbordamiento
    -   Instrucciones de inversión de bits para FFTs
    -   Intrínseco de intercambio condicional
    -   Resinfo en búferes
    -   Recíproco de precisión reducida
    -   Instrucciones de conversión de sombreador: FP16 a fp32 y viceversa
    -   Búfer estructurado, que es un nuevo tipo de búfer que contiene elementos estructurados.

-   Direct3D 11 admite la profundidad de solo lectura o las vistas de estarcido

    -   Deshabilita las escrituras en el elemento que es de solo lectura y permite el uso de textura como entrada y para la selección de profundidad.

-   Direct3D 11 admite Draw Indirect: Direct3D 10 implementa DrawAuto, que toma el contenido (generado por la GPU) y lo representa (en la GPU). Direct3D 11 generaliza DrawAuto para que se pueda llamar mediante un sombreador de cálculo mediante DrawInstanced y DrawIndexedInstanced.
-   Direct3D 11 admite características varias

    -   Ventanillas de punto flotante
    -   Fijación de mipmap por recurso
    -   Tendencia de profundidad: este algoritmo actualiza el comportamiento de la tendencia de profundidad mediante el estado de rasterizador. El resultado elimina los escenarios en los que la diferencia calculada podría ser NaN.
    -   Límites de recursos: los índices de recursos siguen siendo necesarios para <= bits de 32, pero los recursos pueden ser mayores de 4 GB.
    -   Precisión de rasterizador
    -   Requisitos de MSAA
    -   Contadores reducidos
    -   Formato de 1 bits y filtro de texto quitados

## <a name="features-added-in-previous-releases"></a>Características agregadas en versiones anteriores

Para obtener la lista de las características agregadas en versiones anteriores, vea los temas siguientes:

-   [Novedades del SDK de Windows 7/Direct3D 11 de agosto de 2009](dx11-whats-new.md)
-   [Novedades de la vista previa técnica de Direct3D 11 de noviembre de 2008](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 