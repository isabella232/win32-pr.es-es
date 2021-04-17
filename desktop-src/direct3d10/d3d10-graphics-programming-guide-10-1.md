---
description: Características de Direct3D 10,1
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Características de Direct3D 10,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705293"
---
# <a name="direct3d-101-features"></a>Características de Direct3D 10,1

Direct3D 10,1 extiende el conjunto de características de Direct3D 10,0 con las siguientes características nuevas:

-   Modos de mezcla: modos de mezcla independientes por destino de representación mediante la nueva interfaz de estado de Blend (consulte la [**interfaz ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). Las operaciones de fusión de origen dual están restringidas para representar la ranura de destino 0; no puede escribir en otras salidas ni tener destinos de representación enlazados a ranuras distintas de la ranura 0.
-   Comportamiento de selección de valor: las caras de área cero se seleccionan automáticamente; Esto solo afecta a la representación de tramas de alambres.
-   Reglas de punto flotante: usa las mismas reglas IEEE-754 para el punto flotante, excepto que las operaciones de punto flotante de 32 bits se han apretado para producir un resultado dentro de 0,5 de unidad (0,5 ULP) del resultado infinitamente preciso. Esto se aplica a la suma, resta y multiplicación. (precisión en 0,5 ULP para multiplicar, 1,0 ULP para recíproco).
-   Formatos: la precisión de la combinación de float16 ha aumentado a 0,5 ULP. La combinación también es necesaria para los formatos UNORM16/SNORM16/SNORM8.
-   Suavizado de contorno de muestreo múltiple: el multimuestreo se ha mejorado para generalizar la transparencia basada en la cobertura y hacer que el muestreo múltiple funcione de forma más eficaz con la representación de varias pasadas. Para lograr esto, toda la semántica de varios ejemplos se define como si el sombreador de píxeles siempre se ejecuta una vez por ejemplo (frecuencia de muestreo), calculando un color independiente por muestra. Si un sombreador de píxeles no usa ningún atributo por muestra, calculará el mismo valor para cada muestra incluida en un píxel. En ese caso, es equivalente al hardware que ejecuta el sombreador una vez por píxel (frecuencia de píxeles), replicando el resultado en todos los ejemplos incluidos. Naturalmente, la ejecución a una frecuencia de píxeles siempre produce los mismos resultados que la ejecución del mismo sombreador en la frecuencia de muestreo, cuando los atributos se muestrean a una frecuencia de píxeles. La estadística de canalización PSInvocations se incrementa a la frecuencia de ejemplo, a menos que el sombreador se ejecute con una frecuencia de píxeles.
-   Ancho de banda de la fase de canalización: aumento de la cantidad de datos que se pueden pasar entre fases del sombreador: 

    | Recurso                        | Límites                    |
    |---------------------------------|---------------------------|
    | Registros entre fases del sombreador | 32 (32 bits x 4-componente) |
    | Registros de entrada del sombreador de vértices   | 32                        |
    | Ranuras de entrada del ensamblador de entrada     | 32                        |

    

     

-   Reglas de rasterización: las reglas de rasterización han cambiado en lo que respecta a las líneas; además, se ha agregado una nueva funcionalidad.
    -   MultisampleEnable solo afecta a la rasterización de líneas (los puntos y triángulos no se ven afectados) y se utiliza para elegir un algoritmo de dibujo de líneas. Esto significa que ya no se admiten algunas rasterizaciones Multimuestra de Direct3D 10.
    -   Nueva ejecución del sombreador de píxeles de frecuencia de muestra con rasterización primitiva.
-   Resources-CopyResource se habilita en dos escenarios nuevos:
    -   Ahora se pueden usar las superficies de MSAA de color y de profundidad/Galería de símbolos con CopyResource como origen o destino.
    -   Conversión de formato mientras se copia entre determinados recursos con tipo y preestructurados de 32/64/128 bits y representaciones comprimidas de los mismos anchos de bits.
-   Muestreo de textura: \_ las instrucciones de ejemplo c y \_ c \_ LZ se definen para que funcionen con Texture2DArrays y TextureCubeArrays, use el miembro Location (el componente alfa) para especificar un índice de matriz.
-   Views-TextureCube y el nuevo TextureCubeArray (vea [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) no son recursos reales, sino que son vistas nuevas en un recurso Texture2DArray. Cree una vista de recursos a partir de un recurso de Texture2DArray con una marca de uso nueva (D3D10 de \_ recursos \_ varios \_ TEXTURECUBE), use la nueva interfaz de [**interfaz de ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) para enlazar una vista de textura de cubo a la canalización.

Las nuevas características requieren un tipo de dispositivo 10,1 (vea la [**interfaz ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) que se puede crear mediante una llamada a [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1), o bien puede crear el dispositivo y la cadena de intercambio al mismo tiempo mediante una llamada a [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1).

En Windows Vista Service Pack 1, los archivos dll de Direct3D 10,0 y Direct3D 10,1 existen en paralelo en el sistema. Para obtener acceso a las características 10,1, realice una de las siguientes acciones:

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Obtener acceso a las características 10,1 en vista Gold y Vista Service Pack 1

Los desarrolladores que deseen admitir vista Gold y SP1 tendrán que tener en cuenta la falta de las nuevas extensiones de API de 10,1 en vista Gold. Tanto DXUT como D3DX10 proporcionarán funciones útiles para crear el dispositivo adecuado, en función de los archivos dll disponibles en el sistema y el hardware disponible (10,0 o 10,1). El dispositivo 10,1 hereda del dispositivo 10,0 y se puede recuperar mediante QueryInterface (). Se recomienda que cada aplicación realice un seguimiento del tipo de dispositivo y mantenga un puntero al dispositivo 10,1 (si está disponible) para evitar llamadas QueryInterface frecuentes cuando se desee la funcionalidad de 10,1. Del mismo modo, donde 10,1 vistas de recursos y objetos de estado están asociados a la clase personalizada de una aplicación, se recomienda que la aplicación realice un seguimiento de si el objeto es un tipo 10,0 o 10,1 para evitar llamadas de QueryInterface () redundantes. D3DX10 incluye un conjunto de funciones de utilidad para simplificar este proceso (vea [**D3DX10CreateDevice**](d3dx10createdevice.md) y [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Acceso exclusivo a las características 10,1 en vista Service Pack 1

Algunos desarrolladores pueden optar por requerir Vista Service Pack 1, que se distribuirá en general a los usuarios finales e incluye una serie de mejoras fuera de Direct3D 10,1. Estos desarrolladores pueden usar los encabezados y las bibliotecas de Direct3D 10,1 exclusivamente, tomando una dependencia de los archivos dll de Direct3D 10,1 que admiten el hardware 10,0 y 10,1 (algunas llamadas pueden producir un error, sin embargo, en los dispositivos de 10,0 donde no se admite la nueva funcionalidad).

Algunas notas adicionales:

-   Las API expuestas en el D3DX10.dll aceptarán ambos dispositivos 10,0 y 10,1 y aprovecharán la funcionalidad de 10,1 cuando estén disponibles.
-   D3D10SDKLayers.dll admite un dispositivo 10,1 y puede generar el Spew de depuración adecuado para las características de 10,1.
-   D3D10Ref.dll implementa un dispositivo de software 10,0 y 10,1.
-   D3DX10 y FXC admiten el modelo de sombreador actualizado 10,1 con los siguientes destinos: vs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1 y FX \_ 4 \_ 1, que se pueden enlazar a un dispositivo 10,1. Un dispositivo 10,1 admite sombreadores de modelo de sombreador 4,0 y 4,1.
-   El marco de efecto de Direct3D 10,0 admite los dispositivos 10,0 y 10,1, sin embargo, cualquier técnica que incluya sombreadores modelo de sombreador 4,1 o las nuevas características de 10,1 deben usar un dispositivo 10,1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



