---
title: Mostrar un mapa de bits proporcionado por la aplicación en la imagen compuesta
description: Mostrar un mapa Application-Supplied mapa de bits en la imagen compuesta
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90768cc9ba9ed3a7f53336c63b0112f297e1844ba9638799e8badf28588775eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653526"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Mostrar un mapa de bits proporcionado por la aplicación en la imagen compuesta

Las aplicaciones pueden usar el modo de combinación de VMR para mostrar logotipos de canales combinados alfa, una interfaz de usuario o anuncios parcial o completamente dentro del rectángulo de vídeo. Dado que el procesador de gráficos realiza la mezcla en hardware, el rendimiento de reproducción de Video Stream es mínimo y no hay artefactos detectables de parpadeo o desmontado. Las aplicaciones pueden cambiar la imagen que se muestra con la frecuencia que quieran. Debe tenerse en cuenta que los cambios solo se reflejan en la pantalla cuando DirectShow gráfico de filtros está en estado de ejecución.

VmR usa su componente mezclador para superponer el mapa de bits en la imagen compuesta. Con VMR-7, la aplicación debe forzar a vmr a cargar su mezclador, incluso si solo hay una secuencia de vídeo. Esto no es necesario con VMR-9, ya que carga su mezclador de forma predeterminada.

Para combinar una imagen de mapa de bits estática con la secuencia de vídeo, la aplicación crea la VMR y la agrega al gráfico y, a continuación, llama a [**IVMRFilterConfig::SetNumberOfStreams.**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) El valor pasado a esta función identifica el número de pines de entrada que debe crear el VMR. Las aplicaciones pueden especificar cualquier valor entre 1 y MAX MIXER STREAMS; especificar un valor de 1 es válido si la aplicación solo pretende mostrar una sola secuencia \_ \_ de vídeo. Aunque VMR-7 tiene un único pin de entrada de forma predeterminada, se debe llamar a este método para forzarle a cargar su componente mezclador. (VMR-9 carga su mezclador y configura cuatro pines de forma predeterminada).

Para establecer el mapa de bits, use la interfaz [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) en VMR-7 o la interfaz [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) en VMR-9.

El mapa de bits se puede especificar mediante un identificador para un contexto de dispositivo GDI (hDC) o mediante una interfaz de DirectDraw Surface. Si la aplicación quiere que la imagen contenga información alfa incrustada (también conocida como alfa por píxel), debe colocar los datos de la imagen en una interfaz de DirectDraw Surface. Esto se debe a que actualmente no es posible colocar información alfa por píxel con un contexto de dispositivo GDI. La superficie de DirectDraw debe ser RGB32 o ARGB32, y debe ser preferiblemente una superficie de memoria del sistema. No es necesario que las dimensiones de la superficie sean una potencia de 2.

VmR permite a las aplicaciones especificar la ubicación y un valor de transparencia general para la imagen. En el código siguiente se muestra cómo pasar datos de imagen a vmr para la mezcla posterior:


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



Los conceptos que se deban tratar en este tema se muestran en la aplicación de [ejemplo VMRPlayer.](vmrplayer-sample.md)

**Crear animaciones simples con la imagen de mapa de bits**

Para crear un logotipo de mapa de bits animado simple, coloque todos los "fotogramas" del mapa de bits en una sola imagen, como se muestra en la ilustración siguiente.

![franja de imágenes de vmr](images/vmr-image-strip.png)

Al establecer inicialmente el mapa de bits mediante [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), si el mapa de bits está en un HDC, establezca el **campo rSrc** de la estructura **VMRALPHABITMAP** para especificar el tamaño de todo el mapa de bits dentro de HDC. Los **miembros** superior **e izquierdo** de la estructura  se  establecen en 0, y los miembros derecho e inferior son el ancho y alto del mapa de bits. Si el mapa de bits está en una superficie de DirectDraw, se conoce el tamaño de la superficie, por lo que no es necesario especificar rSrc en este método.

Al llamar a [**IVMRMixerBitmap::UpdateAlphaBitmapParameters,**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)use el miembro **rSrc** para los mapas de bits de HDC y DirectDraw, para especificar el marco o rectángulo concreto dentro de la imagen que desea mostrar y establezca la marca **\_ SRCRECT de VMRBITMAP** en el **miembro dwFlags.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



