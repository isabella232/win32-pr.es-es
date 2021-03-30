---
title: Voltear modelo, rectángulos modificados, áreas desplazadas
description: DXGI 1,2 admite una nueva cadena de intercambio de modelo Flip, rectángulos modificados y áreas desplazadas. Se explican las ventajas de usar la nueva cadena de intercambio de modelo flip y de la presentación de optimización mediante la especificación de rectángulos modificados y áreas desplazadas.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104552376"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Voltear modelo, rectángulos modificados, áreas desplazadas

DXGI 1,2 admite una nueva cadena de intercambio de modelo Flip, rectángulos modificados y áreas desplazadas. Se explican las ventajas de usar la nueva cadena de intercambio de modelo flip y de la presentación de optimización mediante la especificación de rectángulos modificados y áreas desplazadas.

## <a name="dxgi-flip-model-presentation"></a>Presentación de modelo Flip de DXGI

DXGI 1,2 agrega compatibilidad con el modelo de presentación de flip para las API de Direct3D 10 y versiones posteriores. En Windows 7, Direct3D 9EX ha adoptado primero la [presentación de Flip-Model](../direct3darticles/direct3d-9ex-improvements.md) para evitar la copia innecesaria del búfer de la cadena de intercambio. Mediante el uso de Flip Model, los búferes de reserva se voltean entre el tiempo de ejecución y el Administrador de ventanas de escritorio (DWM), por lo que DWM siempre se compone directamente del búfer de reserva en lugar de copiar el contenido del búfer de reserva.

Las API de DXGI 1,2 incluyen una interfaz de cadena de intercambio de DXGI revisada, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). Puede usar varios métodos de interfaz [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) para crear el objeto **IDXGISwapChain1** adecuado para usarlo con un identificador [**hWnd**](../winprog/windows-data-types.md) , un objeto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , un [DirectComposition](../directcomp/directcomposition-portal.md)o el marco [**Windows. UI. Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .

Para seleccionar el modelo de presentación de flip, especifique el valor de la enumeración [**\_ \_ \_ \_ Sequential del efecto de intercambio de dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en el miembro **SwapEffect** de la estructura DESC1 de la [**\_ \_ cadena \_ de intercambio de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) y establezca el miembro **BufferCount** de la cadena de **intercambio de dxgi \_ \_ \_ DESC1** en un mínimo de 2. Para obtener más información sobre cómo usar DXGI Flip Model, consulte [modelo de volteo de dxgi](dxgi-flip-model.md). Debido a la presentación más suave del modelo de presentación flip y a otras nuevas funcionalidades, se recomienda usar Flip Presentation Model para todas las aplicaciones nuevas que escriba con Direct3D 10 y las API posteriores.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Usar rectángulos modificados y el rectángulo de desplazamiento en la presentación de la cadena de intercambio

Mediante el uso de rectángulos modificados y el rectángulo de desplazamiento en la presentación de la cadena de intercambio, se ahorra el uso del ancho de banda de la memoria y el uso relacionado de la energía del sistema, ya que la cantidad de datos de píxeles que el sistema operativo necesita para dibujar el siguiente fotograma presentado se reduce si el sistema operativo no necesita dibujar todo el marco. En el caso de las aplicaciones que se muestran a menudo a través de Conexión a Escritorio remoto y otras tecnologías de acceso remoto, el ahorro se percibe especialmente en la calidad de la pantalla, ya que estas tecnologías usan rectángulos modificados y metadatos de desplazamiento.

Solo se puede usar el desplazamiento con cadenas de intercambio de DXGI que se ejecuten en flip Presentation Model. Puede usar rectángulos modificados con cadenas de intercambio de DXGI que se ejecuten en el modelo de volteo y en el modelo de bitblt (establecido con el [**efecto de intercambio de dxgi \_ \_ \_ secuencial**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).

En este escenario y en la ilustración se muestra la funcionalidad de usar rectángulos modificados y desplazarse. Aquí, una aplicación desplazable contiene texto y animar vídeo. La aplicación usa rectángulos modificados para actualizar el vídeo animado y la nueva línea para la ventana, en lugar de actualizar toda la ventana. El rectángulo de desplazamiento permite que el sistema operativo copie y traduzca el contenido representado previamente en el nuevo marco y represente solo la nueva línea en el nuevo marco.

La aplicación realiza la presentación llamando al método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . En esta llamada, la aplicación pasa un puntero a una estructura de [**\_ \_ parámetros presentes de DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) que incluye rectángulos modificados y el número de rectángulos modificados, o el rectángulo de desplazamiento y el desplazamiento de desplazamiento asociado, o ambos rectángulos modificados y el rectángulo de desplazamiento. Nuestra aplicación pasa dos rectángulos modificados y el rectángulo de desplazamiento. El rectángulo de desplazamiento es el área del fotograma anterior que el sistema operativo necesita para copiar en el fotograma actual antes de representar el fotograma actual. La aplicación especifica el vídeo de animación y la nueva línea como rectángulos modificados, y el sistema operativo los representa en el marco actual.

![Ilustración de los rectángulos de desplazamiento y modificados superpuestos](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

El rectángulo discontinuo muestra el rectángulo de desplazamiento en el marco actual. El rectángulo de desplazamiento se especifica mediante el miembro **pScrollRect** de [**\_ \_ los parámetros presentes de DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters). La flecha muestra el desplazamiento de desplazamiento. El desplazamiento de desplazamiento lo especifica el miembro **pScrollOffset** de **\_ \_ los parámetros presentes de DXGI**. Los rectángulos rellenos muestran rectángulos modificados que la aplicación actualizó con contenido nuevo. Los rectángulos rellenos se especifican mediante los miembros **DirtyRectsCount** y **pDirtyRects** de los **\_ \_ parámetros presentes de DXGI**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Ejemplo 2: cadena de intercambio del modelo de volteo de búfer con rectángulos modificados y rectángulo de desplazamiento

En la siguiente ilustración y secuencia se muestra un ejemplo de una operación de presentación de modelo de marcado de DXGI que usa rectángulos modificados y un rectángulo de desplazamiento. En este ejemplo, se usa el número mínimo de búferes para la presentación de Flip-Model, que es un recuento de búferes de dos, un búfer frontal que contiene el contenido para mostrar la aplicación y un búfer de reserva que contiene el fotograma actual que la aplicación desea representar.

1.  Como se muestra en el búfer frontal al principio del fotograma, la aplicación desplazable muestra inicialmente un fotograma con algún texto y animar vídeo.
2.  Para representar el fotograma siguiente, la aplicación representa en el búfer de reserva los rectángulos modificados que actualizan el vídeo de animación y la nueva línea para la ventana.
3.  Cuando la aplicación llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), especifica los rectángulos modificados y el rectángulo de desplazamiento y el desplazamiento. Después, el tiempo de ejecución copia el rectángulo de desplazamiento del fotograma anterior menos los rectángulos modificados actualizados en el búfer de reserva actual.
4.  Finalmente, el tiempo de ejecución intercambia los búferes frontal y posterior.

![ejemplo de cadena de intercambio de modelo Flip con rectángulos de desplazamiento y modificados](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Seguimiento de rectángulos modificados y rectángulos de desplazamiento en varios marcos

Al usar rectángulos modificados en la aplicación, debe realizar un seguimiento de los rectángulos modificados para admitir la representación incremental. Cuando la aplicación llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rectángulos modificados, debe asegurarse de que todos los píxeles dentro de los rectángulos modificados estén actualizados. Si no va a volver a representar completamente todo el área del rectángulo sucio o si no sabe con certeza las áreas que han sido sucias, debe copiar algunos datos del búfer de reserva totalmente coherente en el búfer de reserva actual y obsoleto antes de comenzar la representación.

El motor en tiempo de ejecución solo copia las diferencias entre las áreas actualizadas del marco anterior y las áreas actualizadas del marco actual en el búfer de retroceso actual. Si estas áreas forman una intersección, el Runtime solo copia la diferencia entre ellas. Como puede ver en el siguiente diagrama y secuencia, debe copiar la intersección entre el rectángulo sucio desde el fotograma 1 y el rectángulo sucio del fotograma 2 al rectángulo sucio del marco 2.

1.  Presente rectángulo sucio en el marco 1.
2.  Copiar la intersección entre el rectángulo sucio desde el fotograma 1 y el rectángulo sucio desde el fotograma 2 al rectángulo sucio de la trama 2.
3.  Presente rectángulo sucio en el marco 2.

![seguimiento de rectángulos de desplazamiento y modificados en varios marcos](images/track-dirty-rects-scroll-rects.png)

Para generalizar, en una cadena de intercambio con N búferes, el área que el motor en tiempo de ejecución copia desde el último fotograma al fotograma actual en el marco actual está presente:

![ecuación para calcular el área en la que se copia en tiempo de ejecución](images/runtime-copy-equation.png)

donde buffer indica el índice de búfer en una cadena de intercambio, comenzando por el índice de búfer actual en cero.

Puede realizar un seguimiento de las intersecciones entre el fotograma anterior y los rectángulos modificados del fotograma actual manteniendo una copia de los rectángulos modificados del fotograma anterior o volviendo a representar los rectángulos modificados del nuevo fotograma con el contenido adecuado del fotograma anterior.

Del mismo modo, en los casos en los que la cadena de intercambio tenga más de 2 búferes de reserva, debe asegurarse de que las áreas superpuestas entre los rectángulos modificados del búfer actual y los rectángulos modificados de todos los fotogramas anteriores se copian o se vuelven a representar.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Seguimiento de una sola intersección entre dos rectángulos modificados

En el caso más simple, cuando se actualiza un único rectángulo modificado por fotograma, los rectángulos modificados en dos fotogramas podrían intersectar. Para averiguar si el rectángulo sucio del fotograma anterior y el rectángulo sucio del marco actual se superponen, debe comprobar si el rectángulo sucio del fotograma anterior forma una intersección con el rectángulo sucio del fotograma actual. Puede llamar a la función [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) de GDI para determinar si dos estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que representan los dos rectángulos modificados forman una intersección.

En este fragmento de código, una llamada a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) devuelve la intersección de dos rectángulos modificados en otro [**Rect**](/previous-versions//dd162897(v=vs.85)) denominado dirtyRectCopy. Después de que el fragmento de código determine que los dos rectángulos modificados forman una intersección, llama al método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar la región de intersección en el marco actual.

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

Si usa este fragmento de código en la aplicación, la aplicación estará lista para llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para actualizar el marco actual con el rectángulo modificado actual.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Seguimiento de intersecciones entre N rectángulos modificados

Si especifica varios rectángulos modificados, que pueden incluir un rectángulo sucio para la línea de desplazamiento recién revelada, por fotograma, deberá comprobar y realizar el seguimiento de los superposiciones que puedan producirse entre todos los rectángulos modificados del fotograma anterior y todos los rectángulos modificados del fotograma actual. Para calcular las intersecciones entre los rectángulos modificados del fotograma anterior y los rectángulos modificados del fotograma actual, puede agrupar los rectángulos modificados en regiones.

En este fragmento de código, se llama a la función GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) para convertir cada rectángulo sucio en una región rectangular y, a continuación, se llama a la función GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) para combinar todas las regiones rectangulares desfasadas en un grupo.

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

Ahora puede usar la función [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) de GDI para determinar la intersección entre la región desfasada del fotograma anterior y la región desfasada del fotograma actual. Después de obtener la región de intersección, llame a la función [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) de GDI para obtener cada rectángulo individual de la región de intersección y, a continuación, llame al método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar cada rectángulo intersectando en el búfer de retroceso actual. En el fragmento de código siguiente se muestra cómo usar estas funciones GDI y Direct3D.

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

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Cadena de intercambio del modelo bitblt con rectángulos modificados

Puede usar rectángulos modificados con cadenas de intercambio de DXGI que se ejecutan en el modelo de bitblt (establecido con el [**efecto de intercambio de dxgi \_ \_ \_ secuencial**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). Las cadenas de intercambio del modelo bitblt que usan más de un búfer también deben realizar el seguimiento de los rectángulos modificados superpuestos en los fotogramas de la misma manera que se describe en [seguimiento de rectángulos modificados y rectángulos de desplazamiento en varios fotogramas](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) para las cadenas de intercambio de modelo Las cadenas de intercambio del modelo bitblt con un solo búfer no necesitan realizar un seguimiento de los rectángulos modificados superpuestos, ya que todo el búfer se vuelve a dibujar en cada fotograma.

## <a name="related-topics"></a>Temas relacionados

[Mejoras en DXGI 1,2](dxgi-1-2-improvements.md)
