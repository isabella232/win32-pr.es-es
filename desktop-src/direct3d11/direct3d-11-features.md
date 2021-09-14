---
title: Características de Direct3D 11
description: La guía de programación contiene información sobre cómo usar la canalización programable de Direct3D 11 para crear gráficos 3D en tiempo real para juegos y para aplicaciones científicas y de escritorio.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963824"
---
# <a name="direct3d-11-features"></a>Características de Direct3D 11

La guía de programación contiene información sobre cómo usar la canalización programable de Direct3D 11 para crear gráficos 3D en tiempo real para juegos y para aplicaciones científicas y de escritorio.

-   [Sombreador de proceso](#compute-shader)
-   [Vinculación dinámica de sombreador](#dynamic-shader-linking)
-   [Multithreading](#multithreading)
-   [Teselación](#tessellation)
-   [Lista completa de características](#full-listing-of-features)
-   [Características agregadas en versiones anteriores](#features-added-in-previous-releases)
-   [Temas relacionados](#related-topics)

## <a name="compute-shader"></a>Sombreador de proceso

Un sombreador de proceso es un sombreador programable diseñado para el procesamiento paralelo de datos de uso general. En otras palabras, los sombreadores de proceso permiten usar una GPU como procesador paralelo de uso general. El sombreador de proceso es similar al resto de sombreadores de canalización programables (como vértices, píxeles, geometría) de la manera en que accede a las entradas y salidas. La tecnología de sombreador de proceso también se conoce como tecnología DirectCompute. Un sombreador de proceso se integra en Direct3D y es accesible a través de un dispositivo Direct3D. Puede compartir directamente recursos de memoria con sombreadores de gráficos mediante el dispositivo Direct3D. Sin embargo, no está conectado directamente a otras fases del sombreador.

Un sombreador de proceso está diseñado para aplicaciones de mercado masivo que realizan cálculos a velocidades interactivas, cuando el costo de la transición entre la API (y su pila de software asociada) y una CPU consumiría demasiada sobrecarga.

Un sombreador de proceso tiene su propio conjunto de estados. Un sombreador de proceso no tiene necesariamente una asignación forzada de 1 a 1 a los registros de entrada (como hace un sombreador de vértices) o a los registros de salida (como hace el sombreador de píxeles). Se admiten algunas características del sombreador de gráficos, pero otras se han quitado para que se puedan agregar nuevas características específicas del sombreador de proceso.

Para admitir las características específicas del sombreador de proceso, ahora hay disponibles varios tipos de recursos nuevos, como búferes de lectura y escritura, texturas y búferes estructurados.

Consulte [Información general sobre el sombreador de](direct3d-11-advanced-stages-compute-shader.md) proceso para obtener información adicional.

## <a name="dynamic-shader-linking"></a>Vinculación dinámica de sombreador

Los sistemas de representación deben tratar con una complejidad significativa cuando administran sombreadores, a la vez que proporcionan la oportunidad de optimizar el código del sombreador. Esto se convierte en un desafío aún mayor porque los sombreadores deben admitir una variedad de materiales diferentes en una escena representada en varias configuraciones de hardware. Para abordar este desafío, los desarrolladores de sombreadores a menudo han recurrido a uno de los dos enfoques generales. Han creado sombreadores grandes y de uso general completos que pueden usar una amplia variedad de elementos de escena, lo que ofrece cierto rendimiento por flexibilidad, o han creado sombreadores individuales para cada flujo de geometría, tipo de material o combinación de tipos de luz necesarios.

Estos sombreadores grandes de uso general controlan este desafío mediante la recompilación del mismo sombreador con diferentes definiciones de preprocesador y el último método usa la capacidad de desarrollador por fuerza bruta para lograr el mismo resultado. La explosión de permutación del sombreador a menudo ha sido un problema para los desarrolladores que ahora deben administrar miles de permutaciones de sombreador diferentes dentro de su canalización de juegos y recursos.

Direct3D 11 y el modelo de sombreador 5 presentan construcciones de lenguaje orientadas a objetos y proporcionan compatibilidad en tiempo de ejecución con la vinculación de sombreadores para ayudar a los desarrolladores a programar sombreadores.

Consulte [Dynamic Linking (Vinculación](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) dinámica) para obtener información adicional.

## <a name="multithreading"></a>Subprocesamiento múltiple

Muchas aplicaciones gráficas están enlazadas a la CPU debido a actividades costosas, como el recorrido del grafo de escena, la ordenación de objetos y las simulaciones físicas. Dado que los sistemas de varios núcleos están cada vez más disponibles, Direct3D 11 ha mejorado su compatibilidad con multithreading para permitir una interacción eficaz entre varios subprocesos de CPU y las API de gráficos D3D11.

Direct3D 11 permite que la siguiente funcionalidad admita el multithreading:

-   Los objetos simultáneos ahora se crean en subprocesos independientes: al crear funciones de punto de entrada que crean objetos sin subprocesos, muchos subprocesos pueden crear objetos simultáneamente. Por ejemplo, una aplicación ahora puede compilar un sombreador o cargar una textura en un subproceso mientras se representa en otro.
-   Las listas de comandos se pueden crear en varios subprocesos: una lista de comandos es una secuencia grabada de comandos gráficos. Con Direct3D 11, puede crear listas de comandos en varios subprocesos de CPU, lo que permite el recorrido paralelo de la base de datos de escena o el procesamiento físico en varios subprocesos. Esto libera el subproceso de representación principal para enviar búferes de comandos al hardware.

Consulte [MultiThreading para](overviews-direct3d-11-render-multi-thread.md) obtener información adicional.

## <a name="tessellation"></a>Teselación

La teselación se puede usar para representar un único modelo con distintos niveles de detalle. Este enfoque genera un modelo más preciso geométricamente que depende del nivel de detalle necesario para una escena. Use la teselación en una escena en la que el nivel de detalle permite un modelo de geometría inferior, lo que reduce la demanda de ancho de banda de memoria consumido durante la representación.

En Direct3D, la teselación se implementa en la GPU para calcular una superficie curva más suave a partir de una revisión de entrada gruesa (menos detallada). Cada cara de revisión (cuadrándulo o triángulo) se subdivide en caras triangulares más pequeñas que se aproximan mejor a la superficie que desea.

Para obtener información sobre cómo implementar la teselación en la canalización de gráficos, vea [Introducción a la teselación.](direct3d-11-advanced-stages-tessellation.md)

## <a name="full-listing-of-features"></a>Lista completa de características

Esta es una lista completa de las características de Direct3D 11.

-   Puede ejecutar Direct3D 11 en hardware de nivel [inferior](overviews-direct3d-11-devices-downlevel.md) especificando un nivel [de característica](overviews-direct3d-11-devices-downlevel-intro.md) al crear un dispositivo.
-   Puede realizar la teselación (consulte Introducción a [la](direct3d-11-advanced-stages-tessellation.md)teselación) mediante los siguientes tipos de sombreador:

    -   Sombreador de casco
    -   Sombreador de dominios

-   Direct3D 11 admite multithreading (vea [MultiThreading)](overviews-direct3d-11-render-multi-thread.md)

    -   Creación de recursos multiproceso, sombreador o objeto
    -   Creación de una lista de presentación multiproceso

-   Direct3D 11 expande los sombreadores con las siguientes características (vea [Shader Model 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))

    -   Recursos direccionables: texturas, búferes constantes y muestreadores
    -   Tipos de recursos adicionales, como búferes de lectura y escritura y texturas (consulte [Nuevos tipos de recursos).](direct3d-11-advanced-stages-cs-resources.md)
    -   Subrutinas
    -   Sombreador de proceso (consulte Información general del sombreador de [proceso):](direct3d-11-advanced-stages-compute-shader.md)sombreador que acelera los cálculos dividiendo el espacio del problema entre varios subprocesos de software o grupos de subprocesos, y compartiendo datos entre registros de sombreador para reducir significativamente la cantidad de datos necesarios para introducirlos en un sombreador. Entre los algoritmos que el sombreador de proceso puede mejorar significativamente se incluyen el procesamiento posterior, la animación, la física y la inteligencia artificial.
    -   Sombreador de geometría (vea [Características del sombreador de geometría)](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features)

        -   Creación de instancias: permite al sombreador de geometría generar un máximo de 1024 vértices, o cualquier combinación de instancias y vértices de hasta 1024 (máximo de 32 instancias de 32 vértices cada una).

    -   Sombreador de píxeles

        -   Cobertura como entrada de PS
        -   Interpolación programable de entradas: el sombreador de píxeles puede evaluar los atributos dentro del píxel, en cualquier lugar de la cuadrícula de varias muestras.
        -   El muestreo centroide de atributos debe cumplir las reglas siguientes:

            -   Si se tratan todas las muestras de la primitiva, el atributo se evalúa en el centro de píxeles independientemente de si el patrón de muestra tiene una ubicación de muestra en el centro de píxeles.
            -   De lo contrario, el atributo se evalúa en la primera muestra cubierta, es decir, la muestra con el índice más bajo entre todos los índices de ejemplo. En esta situación, la cobertura de ejemplo se determina después de aplicar la operación LÓGICA AND a la cobertura y al estado de rasterizador sample-mask.
            -   Si no se cubre ninguna muestra (por ejemplo, en píxeles del asistente que se ejecutan fuera de los límites de una primitiva para rellenar marcas de dos x 2 píxeles), el atributo se evalúa de una de las maneras siguientes:

                -   Si el estado del rasterizador sample-mask es un subconjunto de las muestras del píxel, la primera muestra que está cubierta por el estado del rasterizador sample-mask es el punto de evaluación.
                -   De lo contrario, en la condición de máscara de muestra completa, el centro de píxeles es el punto de evaluación.

-   Direct3D 11 expande las texturas (consulte Información general sobre [texturas)](overviews-direct3d-11-resources-textures.md)con las siguientes características

    -   Gather4

        -   Compatibilidad con texturas de varios componentes: especifique un canal desde el que cargar
        -   Compatibilidad con desplazamientos programables

    -   Streaming

        -   Fijaciones de textura para limitar la carga previa de WDDM

    -   Límites de textura de 16 000
    -   Requerir 8 bits de precisión de sub-mip y sub-mip en el filtrado de textura
    -   Nuevos formatos de compresión de textura (1 nuevo formato LDR y 1 nuevo formato HDR)

-   Direct3D 11 admite oDepth conservador: este algoritmo permite que un sombreador de píxeles compare el valor de profundidad por píxel del sombreador de píxeles con el del rasterizador. El resultado permite realizar operaciones tempranas de selección de profundidad mientras se mantiene la capacidad de generar oDepth desde un sombreador de píxeles.
-   Direct3D 11 admite memoria grande

    -   Permitir recursos > 4 GB
    -   Mantener índices de recursos de 32 bits, pero recursos mayores

-   Direct3D 11 admite mejoras de salida de flujo

    -   Salida de flujo direccionable
    -   Aumentar el número de salidas de stream a 4
    -   Cambiar todos los búferes de salida de flujo para que sean de varios elementos

-   Direct3D 11 admite el modelo de sombreador 5 (vea [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Dobles con desnormas
    -   Instrucción de conjunto de bits de recuento
    -   Buscar la primera instrucción del conjunto de bits
    -   Control de carry/overflow
    -   Instrucciones de inversión de bits para FFT
    -   Intercambio condicional intrínseco
    -   Resinfo en búferes
    -   Recíproco de precisión reducida
    -   Instrucciones de conversión del sombreador: fp16 a fp32 y viceversa
    -   Búfer estructurado, que es un nuevo tipo de búfer que contiene elementos estructurados.

-   Direct3D 11 admite vistas de galería de símbolos o profundidad de solo lectura

    -   Deshabilita las escrituras en el elemento que es de solo lectura, permite usar textura como entrada y para la selección de profundidad.

-   Direct3D 11 admite el dibujo indirecto: Direct3D 10 implementa DrawAuto, que toma contenido (generado por la GPU) y lo representa (en la GPU). Direct3D 11 generaliza DrawAuto para que un sombreador de proceso pueda llamarlo mediante DrawInstanced y DrawIndexedInstanced.
-   Direct3D 11 admite características diversas

    -   Ventanillas de punto flotante
    -   Fijación de mipmap por recurso
    -   Sesgo de profundidad: este algoritmo actualiza el comportamiento del sesgo de profundidad mediante el estado de rasterizador. El resultado elimina los escenarios en los que el sesgo calculado podría ser NaN.
    -   Límites de recursos: todavía es necesario que los índices de recursos <= 32 bits, pero los recursos pueden ser mayores que 4 GB.
    -   Precisión del rasterizador
    -   Requisitos de MSAA
    -   Contadores reducidos
    -   Formato de 1 bit y filtro de texto quitados

## <a name="features-added-in-previous-releases"></a>Características agregadas en versiones anteriores

Para obtener la lista de las características agregadas en versiones anteriores, consulte los temas siguientes:

-   [Novedades del SDK de agosto de 2009 Windows 7/Direct3D 11](dx11-whats-new.md)
-   [Novedades de la versión preliminar técnica de Noviembre de 2008 de Direct3D 11](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 