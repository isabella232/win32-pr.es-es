---
title: Modelo de volteo, rectángulos sucios, áreas desplazadas
description: DXGI 1.2 admite una nueva cadena de intercambio de modelos de volteo, rectángulos sucios y áreas desplazadas. Explicamos las ventajas de usar la nueva cadena de intercambio de modelos de volteo y de optimizar la presentación mediante la especificación de rectángulos sucios y áreas desplazadas.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574065"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Modelo de volteo, rectángulos sucios, áreas desplazadas

DXGI 1.2 admite una nueva cadena de intercambio de modelos de volteo, rectángulos sucios y áreas desplazadas. Explicamos las ventajas de usar la nueva cadena de intercambio de modelos de volteo y de optimizar la presentación mediante la especificación de rectángulos sucios y áreas desplazadas.

## <a name="dxgi-flip-model-presentation"></a>Presentación del modelo de volteo DXGI

DXGI 1.2 agrega compatibilidad con el modelo de presentación de volteo para las API de Direct3D 10 y versiones posteriores. En Windows 7, Direct3D 9EX [](../direct3darticles/direct3d-9ex-improvements.md) adoptó por primera vez la presentación del modelo de volteo para evitar copiar innecesariamente el búfer de cadena de intercambio. Con el modelo de volteo, los búferes de reserva se voltea entre el tiempo de ejecución y Administrador de ventanas de escritorio (DWM), por lo que DWM siempre se compone directamente desde el búfer de reserva en lugar de copiar el contenido del búfer de reserva.

Las API de DXGI 1.2 incluyen una interfaz de cadena de intercambio DXGI revisada, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). Puede usar varios métodos de interfaz [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) para crear el objeto **IDXGISwapChain1** adecuado que se usará con un identificador [**HWND,**](../winprog/windows-data-types.md) un objeto [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) [DirectComposition](../directcomp/directcomposition-portal.md)o el [**Windows. UI. Marco xaml.**](/uwp/api/Windows.UI.Xaml?view=winrt-19041)

Seleccione el modelo de presentación de volteo especificando el valor de enumeración [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en el miembro **SwapEffect** de la estructura [**DXGI SWAP CHAIN \_ \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) y estableciendo el miembro **BufferCount** de **DXGI SWAP CHAIN \_ \_ \_ DESC1** en un mínimo de 2. Para obtener más información sobre cómo usar el modelo de volteo DXGI, vea [Modelo de volteo DXGI](dxgi-flip-model.md). Debido a la presentación más fluida del modelo de presentación de volteo y a otras nuevas funcionalidades, se recomienda usar el modelo de presentación de volteo para todas las aplicaciones nuevas que escriba con Direct3D 10 y las API posteriores.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Usar rectángulos sucios y el rectángulo de desplazamiento en la presentación de la cadena de intercambio

Al usar rectángulos desfasados y el rectángulo de desplazamiento en la presentación de la cadena de intercambio, se ahorra en el uso del ancho de banda de memoria y el uso relacionado de la potencia del sistema porque la cantidad de datos de píxeles que el sistema operativo necesita para dibujar el siguiente marco presentado se reduce si el sistema operativo no necesita dibujar todo el marco. En el caso de las aplicaciones que a menudo se muestran a través de Conexión a Escritorio remoto y otras tecnologías de acceso remoto, el ahorro es especialmente apreciable en la calidad de la presentación, ya que estas tecnologías usan rectángulos sucios y metadatos de desplazamiento.

Solo puede usar el desplazamiento con cadenas de intercambio DXGI que se ejecutan en el modelo de presentación de volteo. Puede usar rectángulos sucios con cadenas de intercambio DXGI que se ejecutan tanto en el modelo de volteo como en el modelo bitblt (establecido con [**DXGI \_ SWAP EFFECT \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).

En este escenario e ilustración se muestra la funcionalidad de usar rectángulos y desplazamientos sucios. Aquí, una aplicación desplazable contiene texto y vídeo de animación. La aplicación usa rectángulos sucios para actualizar simplemente el vídeo de animación y la nueva línea de la ventana, en lugar de actualizar toda la ventana. El rectángulo de desplazamiento permite al sistema operativo copiar y traducir el contenido representado previamente en el nuevo marco y representar solo la nueva línea en el nuevo marco.

La aplicación realiza la presentación mediante una llamada [**al método IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) En esta llamada, la aplicación pasa un puntero a una estructura [**DXGI \_ PRESENT \_ PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) que incluye rectángulos desfasados y el número de rectángulos desfasados, el rectángulo de desplazamiento y el desplazamiento de desplazamiento asociado, o bien rectángulos desfasados y el rectángulo de desplazamiento. Nuestra aplicación pasa dos rectángulos desfasados y el rectángulo de desplazamiento. El rectángulo de desplazamiento es el área del marco anterior que el sistema operativo debe copiar en el marco actual antes de representar el marco actual. La aplicación especifica el vídeo de animación y la nueva línea como rectángulos desfasados, y el sistema operativo los representa en el marco actual.

![ilustración de rectángulos de desplazamiento y rectángulos sucios superpuestos](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

El rectángulo discontinuo muestra el rectángulo de desplazamiento en el marco actual. El miembro **pScrollRect** de DXGI PRESENT PARAMETERS especifica el rectángulo [**\_ de \_ desplazamiento.**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) La flecha muestra el desplazamiento de desplazamiento. El desplazamiento de desplazamiento lo especifica el **miembro pScrollOffset** de **DXGI \_ PRESENT \_ PARAMETERS**. Los rectángulos rellenos muestran rectángulos sucios que la aplicación actualizó con nuevo contenido. Los rectángulos rellenos se especifican mediante los **miembros DirtyRectsCount** y **pDirtyRects** de **DXGI \_ PRESENT \_ PARAMETERS**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Ejemplo de cadena de intercambio de modelo de volteo de 2 búferes con rectángulos sucios y rectángulo de desplazamiento

En la siguiente ilustración y secuencia se muestra un ejemplo de una operación de presentación del modelo de volteo DXGI que usa rectángulos sucios y un rectángulo de desplazamiento. En este ejemplo se usa el número mínimo de búferes para la presentación del modelo de volteo, que es un recuento de búferes de dos, un búfer frontal que contiene el contenido para mostrar de la aplicación y un búfer de reserva que contiene el marco actual que la aplicación quiere representar.

1.  Como se muestra en el búfer frontal al principio del marco, la aplicación desplazable muestra inicialmente un fotograma con texto y vídeo de animación.
2.  Para representar el siguiente fotograma, la aplicación representa en el búfer de reserva los rectángulos sucios que actualizan el vídeo de animación y la nueva línea de la ventana.
3.  Cuando la aplicación llama a [**IDXGISwapChain1::P resent1,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)especifica los rectángulos desfasados y el rectángulo de desplazamiento y el desplazamiento. A continuación, el tiempo de ejecución copia el rectángulo de desplazamiento del marco anterior menos los rectángulos sucios actualizados en el búfer de reserva actual.
4.  Por último, el tiempo de ejecución intercambia los búferes front y back.

![ejemplo de cadena de intercambio de modelos de volteo con rectángulos de desplazamiento y desgaje](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Seguimiento de rectángulos sucios y rectángulos de desplazamiento en varios fotogramas

Al usar rectángulos sucios en la aplicación, debe realizar un seguimiento de los rectángulos sucios para admitir la representación incremental. Cuando la aplicación llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rectángulos sucios, debe asegurarse de que todos los píxeles dentro de los rectángulos sucios están actualizados. Si no va a volver a representar completamente el área completa del rectángulo desnuciado o si no puede saber con certeza las áreas que están protegidas, debe copiar algunos datos del búfer de reserva totalmente coherente anterior en el búfer de reserva obsoleto actual antes de empezar la representación.

El tiempo de ejecución solo copia las diferencias entre las áreas actualizadas del marco anterior y las áreas actualizadas del marco actual en el búfer de reserva actual. Si estas áreas se cruzan, el tiempo de ejecución solo copia la diferencia entre ellas. Como puede ver en el diagrama y la secuencia siguientes, debe copiar la intersección entre el rectángulo sucio del marco 1 y el rectángulo sucio del marco 2 al rectángulo sucio del marco 2.

1.  Presentar rectángulo desa obsceno en el marco 1.
2.  Copie la intersección entre el rectángulo sucio del marco 1 y el rectángulo sucio del marco 2 en el rectángulo sucio del marco 2.
3.  Presentar rectángulo desa obsceno en el marco 2.

![desplazamiento de seguimiento y rectángulos sucios en varios fotogramas](images/track-dirty-rects-scroll-rects.png)

Para generalizar, para una cadena de intercambio con N búferes, el área que el tiempo de ejecución copia del último fotograma al marco actual en el marco actual es:

![ecuación para calcular el área que copia el tiempo de ejecución](images/runtime-copy-equation.png)

donde buffer indica el índice de búfer en una cadena de intercambio, empezando por el índice de búfer actual en cero.

Puede realizar un seguimiento de las intersecciones entre el marco anterior y los rectángulos des dirty del marco actual manteniendo una copia de los rectángulos des dirty del marco anterior o re-rendering the new frame's dirty rectangles with the appropriate content from the previous frame.

Del mismo modo, en los casos en los que la cadena de intercambio tiene más de 2 búferes de reserva, debe asegurarse de que las áreas superpuestas entre los rectángulos sucios del búfer actual y los rectángulos sucios de todos los fotogramas anteriores se copian o se representan de nuevo.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Seguimiento de una intersección única entre dos rectángulos sucios

En el caso más sencillo, cuando se actualiza un único rectángulo desdobado por fotograma, los rectángulos sucios entre dos marcos pueden formar una intersección. Para averiguar si el rectángulo sucio del marco anterior y el rectángulo sucio del marco actual se superponen, debe comprobar si el rectángulo sucio del marco anterior forma una intersección con el rectángulo sucio del marco actual. Puede llamar a la función [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) de GDI para determinar si dos estructuras [**RECT**](/previous-versions//dd162897(v=vs.85)) que representan los dos rectángulos sucios se intersecan.

En este fragmento de código, una llamada a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) devuelve la intersección de dos rectángulos sucios en otro [**RECT**](/previous-versions//dd162897(v=vs.85)) denominado dirtyRectCopy. Después de que el fragmento de código determine que los dos rectángulos sucios se cruzan, llama al método [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar la región de intersección en el marco actual.

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

Si usa este fragmento de código en la aplicación, la aplicación estará lista para llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para actualizar el marco actual con el rectángulo sucio actual.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Seguimiento de intersecciones entre N rectángulos sucios

Si especifica varios rectángulos sucios, que pueden incluir un rectángulo desalineado para la línea de desplazamiento recién revelada, por fotograma, debe comprobar y realizar un seguimiento de las superposiciones que puedan producirse entre todos los rectángulos sucios del marco anterior y todos los rectángulos sucios del marco actual. Para calcular las intersecciones entre los rectángulos sucios del marco anterior y los rectángulos sucios del marco actual, puede agrupar los rectángulos sucios en regiones.

En este fragmento de código, llamamos a la función [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) de GDI para convertir cada rectángulo sucio en una región rectangular y, a continuación, llamamos a la función [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) de GDI para combinar todas las regiones rectangulares desaversas en un grupo.

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

Ahora puede usar la función [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) de GDI para determinar la intersección entre la región desaseñada del marco anterior y la región desaseñada del marco actual. Después de obtener la región en intersección, llame a la función [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) de GDI para obtener cada rectángulo individual de la región que forma intersección y, a continuación, llame al método [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar cada rectángulo que forma una intersección en el búfer de reserva actual. El siguiente fragmento de código muestra cómo usar estas funciones GDI y Direct3D.

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Cadena de intercambio del modelo bitblt con rectángulos sucios

Puede usar rectángulos sucios con cadenas de intercambio DXGI que se ejecutan en el modelo bitblt (establecido con [**DXGI \_ SWAP EFFECT \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). Las cadenas de intercambio de modelos de Bitblt que usan más de un búfer también deben realizar un seguimiento de los rectángulos desdoblados superpuestos entre fotogramas de la misma manera que se describe en Seguimiento de rectángulos desgaje y rectángulos de desplazamiento entre varios fotogramas para las [cadenas](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) de intercambio de modelos de volteo. Las cadenas de intercambio del modelo bitblt con un solo búfer no necesitan realizar un seguimiento de los rectángulos sucios superpuestos porque todo el búfer se vuelve a dibujar en cada fotograma.

## <a name="related-topics"></a>Temas relacionados

[Mejoras de DXGI 1.2](dxgi-1-2-improvements.md)
