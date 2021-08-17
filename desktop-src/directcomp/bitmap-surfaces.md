---
title: Objetos de mapa de bits
description: En este tema se describen los tipos de contenido de mapa de bits que admite DirectComposition.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc36253511c060b264039f27975c694272c1c916ad0067c1955fd02f00553d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089055"
---
# <a name="bitmap-objects"></a>Objetos de mapa de bits

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition es un motor de composición de mapa de bits. Permite a los desarrolladores de aplicaciones combinar varios mapas de bits y manipularlos de varias maneras para lograr efectos visuales y animaciones interesantes en una interfaz de usuario de la aplicación. En este tema se describen los tipos de contenido de mapa de bits que admite DirectComposition.

-   [Contenido de mapa de bits](#bitmap-content)
    -   [Mapas de bits de memoria de vídeo](#video-memory-bitmaps)
    -   [Mapas de bits de ventana](#window-bitmaps)
    -   [Asociación de contenido de mapa de bits con un objeto visual](#associating-bitmap-content-with-a-visual)
    -   [Canal alfa](#alpha-channel)
-   [Temas relacionados](#related-topics)

## <a name="bitmap-content"></a>Contenido de mapa de bits

Las aplicaciones proporcionan a DirectComposition el contenido del mapa de bits para crear y animar mediante la creación de objetos visuales y, a continuación, el establecimiento de la [propiedad Content](basic-concepts.md) de esos objetos. DirectComposition no ofrece ningún servicio de rasterización. Una aplicación debe usar alguna otra biblioteca de rasterización basada en software o acelerada por hardware, como [Direct2D](../direct2d/direct2d-portal.md) o [Direct3D,](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para rellenar los mapas de bits que se van a componer. Después de la composición, DirectComposition pasa contenido de mapa de bits compuesto [a Administrador de ventanas de escritorio (DWM) para](/windows/desktop/dwm/dwm-overview) representarlo en la pantalla.

**Tipos admitidos de contenido de mapa de bits** Microsoft DirectComposition admite los siguientes tipos de mapas de bits:

-   [Mapas de bits de memoria de vídeo](#video-memory-bitmaps)
-   [Mapas de bits de ventana](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Mapas de bits de memoria de vídeo

Un mapa de bits de memoria de vídeo se rasteriza en hardware mediante métodos de Microsoft DirectX (incluido el modelo de interoperabilidad DX a GDI). Está respaldo de superficies compartidas entre procesos que son visibles para la aplicación que realiza la llamada y para DirectComposition. Un mapa de bits de memoria de vídeo no está sujeto a desgarros porque la aplicación solo puede leer desde las superficies de las que directComposition se textura.

### <a name="video-content"></a>Contenido de vídeo

Las aplicaciones pueden usar DirectComposition para crear fotogramas de vídeo que usan cadenas de intercambio sin ventanas de DirectX que están enlazadas a una superficie de DirectComposition. Conceptualmente, DirectComposition trata el contenido de vídeo como una secuencia de mapas de bits. DirectComposition no proporciona un medio para presentar fotogramas de vídeo.

DirectComposition admite cadenas de intercambio sin ventanas de DirectX, es decir, cadenas de intercambio que no están enlazadas a una ventana determinada, y permite que dos aplicaciones diferentes compartan cadenas de intercambio sin ventanas a través de los límites del proceso. Compartir cadenas de intercambio sin ventanas permite escenarios de vídeo en los que la cadena de intercambio se crea en un proceso y se usa con DirectComposition en un segundo proceso. Las cadenas de intercambio sin ventanas se crean mediante el método [**IDXGIFactory2::CreateSwapChainForCompositionSurface.**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)

Para obtener más información sobre las cadenas de intercambio de DirectX, vea [Información general de DXGI.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

### <a name="stereo-content"></a>Contenido estéreo

Conceptualmente, una cadena de intercambio estéreo consta de superficies de Microsoft Infraestructura de gráficos de DirectX (DXGI) que representan los canales izquierdo y derecho para contenido 3D estéreo. Cuando se usa una cadena de intercambio estéreo como recurso de mapa de bits para un objeto visual, DirectComposition se compone en estéreo. Se considera que todo el contenido no estéreo (contenido mono) tiene contenido de canal izquierdo y derecho idéntico. es decir, se usa el mismo contenido de mapa de bits para ambos canales. DirectComposition compone todo el contenido izquierdo y todo el contenido correcto por separado. Si el dispositivo de pantalla no es compatible con estéreo, DirectComposition trata el canal estéreo izquierdo o derecho (según la aplicación) como contenido mono y crea usando solo los datos para el recurso de mapa de bits.

DirectComposition no admite la creación o manipulación de contenido estéreo y no puede promover una cadena de intercambio mono a un par estéreo. Una aplicación debe realizar estas tareas antes de presentar contenido estéreo de DirectX a DirectComposition. Además, una aplicación debe proporcionar los desplazamientos del canal izquierdo y derecho para la percepción de la profundidad; DirectComposition no puede ajustar los desplazamientos del canal izquierdo y derecho para modificar la profundidad percibida del contenido estéreo de DirectX.

El contenido estéreo de DirectX se compone y se conserva en DWM cuando hay hardware compatible con estéreo disponible.

### <a name="window-bitmaps"></a>Mapas de bits de ventana

Un "mapa de bits de ventana" no es un mapa de bits real, pero es un marcador de posición que DirectComposition reemplaza en tiempo real por rasterizaciones de ventanas de nivel superior o secundarias en capas. Un mapa de bits de ventana es similar a una miniatura DWM, salvo que una miniatura puede contener contribuciones de muchas ventanas, como las ventanas que no son secundarias en propiedad, mientras que un mapa de bits de la ventana DirectComposition siempre es una representación de una sola ventana y sus elementos secundarios.

Dado que DirectComposition tiene acceso a las superficies de redireccionamiento de todas las ventanas y todos los árboles visuales, puede reutilizar el contenido de una ventana en varios árboles visuales. La ventana debe estar superada porque una ventana sin capas no tiene una superficie de redireccionamiento dedicada y, por lo tanto, su rasterización no siempre está disponible para DirectComposition.

Para usar un mapa de bits de ventana, una aplicación asocia un objeto visual a un identificador de ventana (HWND). Después, DirectComposition vuelve a componer el objeto visual cada vez que cambia el contenido de la ventana, incluso cuando el contenido cambia como resultado de cambios en los árboles visuales asociados a la ventana. En otras palabras, como las miniaturas dwm, los mapas de bits de ventana de DirectComposition son "en directo".

### <a name="associating-bitmap-content-with-a-visual"></a>Asociación de contenido de mapa de bits con un objeto visual

Para los tres tipos de mapas de bits, una aplicación puede asociar el mismo mapa de bits con varios objetos visuales, lo que significa que se puede usar una sola asignación de memoria para mostrar el mismo contenido varias veces.

### <a name="alpha-channel"></a>Canal alfa

Todos los mapas de bits tienen un formato de 32 bits por píxel (BPP), que incluye ocho bits para la transparencia por píxel. Sin embargo, una aplicación puede especificar cómo DirectComposition debe consumir el canal alfa. En concreto, DirectComposition puede respetar el canal alfa o puede omitir alfa por completo, en cuyo caso el mapa de bits se considera totalmente opaco.

Un modo alfa adicional omite el canal alfa, pero trata los valores rojo, verde y azul como valores alfa por canal en lugar de la interpretación normal de esos canales como intensidades de color. Este modo es útil para la representación de ClearType, que requiere información de cobertura de subpíxeles. Para usar el modo alfa por canal, una aplicación [](/windows/desktop/DirectWrite/direct-write-portal) debe usar primero [Direct2D](../direct2d/direct2d-portal.md) y DirectWrite escribir datos de cobertura de subpíxeles en un mapa de bits. A continuación, la aplicación debe establecer el modo alfa correcto y especificar un color de texto cuando asocie el mapa de bits a un objeto visual. DirectComposition combina el color del texto con los datos de cobertura, lo que produce una combinación ClearType en el fondo.

En situaciones en las que el algoritmo ClearType no es aplicable, como si el mapa de bits no está alineado en píxeles y en el eje, o si necesita dibujarse en una superficie intermedia, DirectComposition puede usar los datos de cobertura de subpíxeles del mapa de bits para generar una rasterización de escala de grises en su lugar, de forma automática y sin costo adicional.

Para obtener más información, vea la descripción del parámetro *alphaMode* de la función [**IDCompositionDevice::CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) o [**IDCompositionDevice::CreateVirtualSurface.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 