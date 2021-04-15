---
title: Objetos Bitmap
description: En este tema se describen los tipos de contenido de mapa de bits que DirectComposition admite.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c390778fef1ee7ad96c90a8b7706fa635f3615ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421343"
---
# <a name="bitmap-objects"></a>Objetos Bitmap

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition es un motor de composición de mapas de bits. Permite a los desarrolladores de aplicaciones combinar varios mapas de bits y manipularlos de varias maneras para lograr animaciones y efectos visuales interesantes en una interfaz de usuario de la aplicación. En este tema se describen los tipos de contenido de mapa de bits que DirectComposition admite.

-   [Contenido de mapa de bits](#bitmap-content)
    -   [Mapas de bits de memoria de vídeo](#video-memory-bitmaps)
    -   [Mapas de bits de ventana](#window-bitmaps)
    -   [Asociar el contenido del mapa de bits a un visual](#associating-bitmap-content-with-a-visual)
    -   [Canal alfa](#alpha-channel)
-   [Temas relacionados](#related-topics)

## <a name="bitmap-content"></a>Contenido de mapa de bits

Las aplicaciones proporcionan DirectComposition con el contenido del mapa de bits para componer y animar creando objetos visuales y estableciendo después la [propiedad de contenido](basic-concepts.md) de esos objetos. DirectComposition no ofrece ningún servicio de rasterización. Una aplicación debe usar otra biblioteca de rasterización basada en software o con aceleración de hardware, como [Direct2D](../direct2d/direct2d-portal.md) o [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) , para rellenar los mapas de bits que se van a componer. Después de redactar, DirectComposition pasa el contenido del mapa de bits compuesto a [Administrador de ventanas de escritorio (DWM)](/windows/desktop/dwm/dwm-overview) para su representación en la pantalla.

**Tipos de contenido**   de mapa de bits admitidos Microsoft DirectComposition admite los siguientes tipos de mapas de bits:

-   [Mapas de bits de memoria de vídeo](#video-memory-bitmaps)
-   [Mapas de bits de ventana](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Mapas de bits de memoria de vídeo

Un mapa de bits de memoria de vídeo se rasteriza en hardware mediante el uso de los métodos de Microsoft DirectX (incluido el modelo de interoperabilidad DX-to-GDI). Está respaldado por superficies compartidas entre procesos que son visibles para la aplicación que realiza la llamada y DirectComposition. Un mapa de bits de memoria de vídeo no está sujeto a un desgarro, ya que la aplicación solo puede leer de las superficies de las que DirectComposition las texturas.

### <a name="video-content"></a>Contenido de vídeo

Las aplicaciones pueden usar DirectComposition para crear fotogramas de vídeo que usen cadenas de intercambio sin ventanas de DirectX enlazadas a una superficie de DirectComposition. Conceptualmente, DirectComposition trata el contenido de vídeo como una secuencia de mapas de bits. DirectComposition no proporciona un medio para presentar fotogramas de vídeo.

DirectComposition admite cadenas de intercambio sin ventanas de DirectX, es decir, cadenas de intercambio que no están enlazadas a una ventana determinada, y permite que dos aplicaciones diferentes compartan cadenas de intercambio sin ventanas en los límites del proceso. Compartir cadenas de intercambio sin ventanas permite escenarios de vídeo en los que la cadena de intercambio se crea en un proceso y se usa con DirectComposition en un segundo proceso. Las cadenas de intercambio sin ventanas se crean mediante el método [**IDXGIFactory2:: CreateSwapChainForCompositionSurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

Para obtener más información sobre las cadenas de intercambio de DirectX, consulte [información general sobre DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Contenido estéreo

Conceptualmente, una cadena de intercambio estéreo consta de las superficies de infraestructura de gráficos de Microsoft DirectX (DXGI) que representan los canales izquierdo y derecho para contenido 3D estéreo. Cuando se usa una cadena de intercambio estéreo como recurso de mapa de bits para un visual, DirectComposition se compone en estéreo. Se considera que todo el contenido no estéreo (contenido mono) tiene el mismo contenido de canal izquierdo y derecho. es decir, se usa el mismo contenido de mapa de bits para ambos canales. DirectComposition compone todo el contenido de la izquierda y todo el contenido adecuado por separado. Si el dispositivo de pantalla no es compatible con estéreo, DirectComposition trata el canal estéreo izquierdo o derecho (en función de la aplicación) como contenido mono y se compone solo con los datos del recurso de mapa de bits.

DirectComposition no admite la creación o manipulación de contenido estéreo y no puede promover una cadena de intercambio mono a un par estéreo. Una aplicación debe realizar estas tareas antes de presentar el contenido estéreo de DirectX a DirectComposition. Además, una aplicación debe proporcionar los desplazamientos de canal izquierdo y derecho para la percepción de profundidad. DirectComposition no puede ajustar los desplazamientos de canal izquierdo y derecho para modificar la profundidad percibida del contenido estéreo de DirectX.

El contenido estéreo de DirectX se compone y se conserva en DWM cuando está disponible hardware compatible con estéreo.

### <a name="window-bitmaps"></a>Mapas de bits de ventana

Un "mapa de bits de ventana" no es un mapa de bits real, sino que es un marcador de posición que DirectComposition reemplaza en tiempo real con rasterizaciones de ventanas secundarias o de nivel superior superpuestas. Un mapa de bits de ventana es similar a una miniatura de DWM, excepto en que una miniatura puede contener las contribuciones de muchas ventanas, como las ventanas que no son secundarias, mientras que un mapa de bits de la ventana de DirectComposition siempre es una representación de solo una ventana y sus elementos secundarios.

Dado que DirectComposition tiene acceso a las superficies de redirección de todas las ventanas y de todos los árboles visuales, puede volver a usar el contenido de una ventana en varios árboles visuales. La ventana debe estar en capas porque una ventana sin capas no tiene una superficie de redirección dedicada y, por lo tanto, su rasterización no siempre está disponible para DirectComposition.

Para usar un mapa de bits de ventana, una aplicación asocia un visual a un identificador de ventana (HWND). Después, DirectComposition vuelve a crear el objeto visual cada vez que cambia el contenido de la ventana, incluso cuando cambia el contenido como resultado de los cambios en los árboles visuales asociados a la ventana. En otras palabras, al igual que las miniaturas de DWM, los mapas de bits de la ventana DirectComposition son "activos".

### <a name="associating-bitmap-content-with-a-visual"></a>Asociar el contenido del mapa de bits a un visual

En el caso de los tres tipos de mapas de bits, una aplicación puede asociar el mismo mapa de bits con varios objetos visuales, lo que significa que se puede usar una única asignación de memoria para mostrar el mismo contenido varias veces.

### <a name="alpha-channel"></a>Canal alfa

Todos los mapas de bits tienen un formato de 32 bits por píxel (BPP), que incluye ocho bits para la transparencia por píxel. Sin embargo, una aplicación puede especificar cómo debe consumir DirectComposition el canal alfa. En concreto, DirectComposition puede respetar el canal alfa o puede omitir alfa por completo, en cuyo caso se considera que el mapa de bits es totalmente opaco.

Un modo alfa adicional omite el canal alfa, pero trata los valores rojo, verde y azul como valores alfa por canal en lugar de la interpretación normal de esos canales como intensidades de color. Este modo es útil para la representación de ClearType, que requiere información de cobertura de subpíxeles. Para usar el modo alfa por canal, una aplicación debe usar primero [Direct2D](../direct2d/direct2d-portal.md) y [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para escribir datos de cobertura de subpíxeles en un mapa de bits. A continuación, la aplicación debe establecer el modo alfa correcto y especificar un color de texto cuando asocie el mapa de bits con un valor visual. DirectComposition combina el color del texto con los datos de cobertura, lo que produce la combinación de ClearType en el fondo.

En situaciones en las que el algoritmo ClearType no es aplicable, como si el mapa de bits no está alineado por píxeles y está alineado con el eje, o si es necesario dibujarlo en una superficie intermedia, DirectComposition puede usar los datos de cobertura de subpíxeles del mapa de bits para generar una rasterización de escala de grises en su lugar, de forma automática y sin costo adicional.

Para obtener más información, vea la descripción del parámetro *alphaMode* de la función [**IDCompositionDevice:: CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) o [**IDCompositionDevice:: CreateVirtualSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 