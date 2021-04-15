---
title: Mostrar un mapa de bits proporcionado por la aplicación en la imagen compuesta
description: Mostrar un mapa de bits de Application-Supplied en la imagen compuesta
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536585"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Mostrar un mapa de bits proporcionado por la aplicación en la imagen compuesta

Las aplicaciones pueden usar el modo de mezcla de VMR para mostrar logotipos de canal combinados alfa, una interfaz de usuario o anuncios de forma parcial o completa dentro del rectángulo de vídeo. Dado que el procesador de gráficos realiza la combinación en el hardware, el rendimiento de reproducción de la secuencia de vídeo tiene un impacto mínimo y no hay artefactos que se pueden detectar ni producir parpadeos. Las aplicaciones pueden cambiar la imagen que se muestra con la frecuencia que deseen. Se debe observar que los cambios solo se reflejan en la pantalla cuando el gráfico de filtros de DirectShow está en el estado en ejecución.

VMR usa su componente de mezclador para superponer el mapa de bits en la imagen compuesta. Con la VMR-7, la aplicación debe forzar a la VMR a cargar su mezclador, aunque solo haya una secuencia de vídeo. Esto no es necesario con VMR-9, ya que carga de forma predeterminada su mezclador.

Para mezclar una imagen de mapa de bits estática con la secuencia de vídeo, la aplicación crea la VMR y la agrega al gráfico y, a continuación, llama a [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). El valor que se pasa a esta función identifica el número de clavijas de entrada que debe crear la VMR. Las aplicaciones pueden especificar cualquier valor entre 1 y el número máximo \_ \_ de flujos de mezclador; si se especifica un valor de 1 es válido si la aplicación solo tiene intención de mostrar una única secuencia de vídeo. Aunque VMR-7 tiene un único PIN de entrada de forma predeterminada, se debe llamar a este método para obligarlo a cargar su componente de mezclador. (VMR-9 carga su mezclador y configura cuatro PIN de forma predeterminada).

Para establecer el mapa de bits, use la interfaz [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) en la interfaz VMR-7 o [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) en VMR-9.

El mapa de bits se puede especificar mediante un identificador de un contexto de dispositivo GDI (hDC) o una interfaz de DirectDraw Surface. Si la aplicación desea que la imagen contenga información alfa incrustada (también conocida como alfa por píxel), debe colocar los datos de la imagen en una interfaz de superficie de DirectDraw. Esto se debe a que actualmente no es posible colocar información alfa por píxel con un contexto de dispositivo GDI. La superficie de DirectDraw debe ser RGB32 o ARGB32 y, preferiblemente, una superficie de memoria del sistema. No es necesario que las dimensiones de la superficie sean una potencia de 2.

VMR permite a las aplicaciones especificar la ubicación y un valor de transparencia general para la imagen. En el código siguiente se muestra cómo pasar datos de imagen hacia abajo a la VMR para la fusión posterior:


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



Los conceptos descritos en este tema se muestran en la aplicación de ejemplo de [ejemplo VMRPlayer](vmrplayer-sample.md) .

**Crear animaciones simples con la imagen de mapa de bits**

Para crear un logotipo de mapa de bits animado sencillo, coloque todos los "Marcos" de mapa de bits en una sola imagen, como se muestra en la siguiente ilustración.

![banda de imágenes VMR](images/vmr-image-strip.png)

Al establecer el mapa de bits inicialmente con [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), si el mapa de bits está en una HDC, establezca el campo **rSrc** de la estructura **VMRALPHABITMAP** para especificar el tamaño del mapa de bits completo dentro de la HDC. Los miembros **superior** e **izquierdo** de la estructura se establecen en 0, y los miembros **derecho** e **inferior** son el ancho y el alto del mapa de bits. Si el mapa de bits está en una superficie DirectDraw, se conoce el tamaño de la superficie, por lo que no es necesario especificar rSrc en este método.

Al llamar a [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use el miembro **rSrc** para los mapas de bits HDC y DirectDraw, para especificar el fotograma o rectángulo determinado dentro de la imagen que desea mostrar, y establezca la marca de **VMRBITMAP \_ SRCRECT** en el miembro **dwFlags** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



