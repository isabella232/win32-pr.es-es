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
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="c0171-103">Mostrar un mapa de bits proporcionado por la aplicación en la imagen compuesta</span><span class="sxs-lookup"><span data-stu-id="c0171-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="c0171-104">Las aplicaciones pueden usar el modo de mezcla de VMR para mostrar logotipos de canal combinados alfa, una interfaz de usuario o anuncios de forma parcial o completa dentro del rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0171-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="c0171-105">Dado que el procesador de gráficos realiza la combinación en el hardware, el rendimiento de reproducción de la secuencia de vídeo tiene un impacto mínimo y no hay artefactos que se pueden detectar ni producir parpadeos.</span><span class="sxs-lookup"><span data-stu-id="c0171-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="c0171-106">Las aplicaciones pueden cambiar la imagen que se muestra con la frecuencia que deseen.</span><span class="sxs-lookup"><span data-stu-id="c0171-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="c0171-107">Se debe observar que los cambios solo se reflejan en la pantalla cuando el gráfico de filtros de DirectShow está en el estado en ejecución.</span><span class="sxs-lookup"><span data-stu-id="c0171-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="c0171-108">VMR usa su componente de mezclador para superponer el mapa de bits en la imagen compuesta.</span><span class="sxs-lookup"><span data-stu-id="c0171-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="c0171-109">Con la VMR-7, la aplicación debe forzar a la VMR a cargar su mezclador, aunque solo haya una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0171-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="c0171-110">Esto no es necesario con VMR-9, ya que carga de forma predeterminada su mezclador.</span><span class="sxs-lookup"><span data-stu-id="c0171-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="c0171-111">Para mezclar una imagen de mapa de bits estática con la secuencia de vídeo, la aplicación crea la VMR y la agrega al gráfico y, a continuación, llama a [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="c0171-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="c0171-112">El valor que se pasa a esta función identifica el número de clavijas de entrada que debe crear la VMR.</span><span class="sxs-lookup"><span data-stu-id="c0171-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="c0171-113">Las aplicaciones pueden especificar cualquier valor entre 1 y el número máximo \_ \_ de flujos de mezclador; si se especifica un valor de 1 es válido si la aplicación solo tiene intención de mostrar una única secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0171-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="c0171-114">Aunque VMR-7 tiene un único PIN de entrada de forma predeterminada, se debe llamar a este método para obligarlo a cargar su componente de mezclador.</span><span class="sxs-lookup"><span data-stu-id="c0171-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="c0171-115">(VMR-9 carga su mezclador y configura cuatro PIN de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="c0171-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="c0171-116">Para establecer el mapa de bits, use la interfaz [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) en la interfaz VMR-7 o [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) en VMR-9.</span><span class="sxs-lookup"><span data-stu-id="c0171-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="c0171-117">El mapa de bits se puede especificar mediante un identificador de un contexto de dispositivo GDI (hDC) o una interfaz de DirectDraw Surface.</span><span class="sxs-lookup"><span data-stu-id="c0171-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="c0171-118">Si la aplicación desea que la imagen contenga información alfa incrustada (también conocida como alfa por píxel), debe colocar los datos de la imagen en una interfaz de superficie de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c0171-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="c0171-119">Esto se debe a que actualmente no es posible colocar información alfa por píxel con un contexto de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="c0171-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="c0171-120">La superficie de DirectDraw debe ser RGB32 o ARGB32 y, preferiblemente, una superficie de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="c0171-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="c0171-121">No es necesario que las dimensiones de la superficie sean una potencia de 2.</span><span class="sxs-lookup"><span data-stu-id="c0171-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="c0171-122">VMR permite a las aplicaciones especificar la ubicación y un valor de transparencia general para la imagen.</span><span class="sxs-lookup"><span data-stu-id="c0171-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="c0171-123">En el código siguiente se muestra cómo pasar datos de imagen hacia abajo a la VMR para la fusión posterior:</span><span class="sxs-lookup"><span data-stu-id="c0171-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


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



<span data-ttu-id="c0171-124">Los conceptos descritos en este tema se muestran en la aplicación de ejemplo de [ejemplo VMRPlayer](vmrplayer-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="c0171-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="c0171-125">**Crear animaciones simples con la imagen de mapa de bits**</span><span class="sxs-lookup"><span data-stu-id="c0171-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="c0171-126">Para crear un logotipo de mapa de bits animado sencillo, coloque todos los "Marcos" de mapa de bits en una sola imagen, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c0171-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![banda de imágenes VMR](images/vmr-image-strip.png)

<span data-ttu-id="c0171-128">Al establecer el mapa de bits inicialmente con [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), si el mapa de bits está en una HDC, establezca el campo **rSrc** de la estructura **VMRALPHABITMAP** para especificar el tamaño del mapa de bits completo dentro de la HDC.</span><span class="sxs-lookup"><span data-stu-id="c0171-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="c0171-129">Los miembros **superior** e **izquierdo** de la estructura se establecen en 0, y los miembros **derecho** e **inferior** son el ancho y el alto del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c0171-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="c0171-130">Si el mapa de bits está en una superficie DirectDraw, se conoce el tamaño de la superficie, por lo que no es necesario especificar rSrc en este método.</span><span class="sxs-lookup"><span data-stu-id="c0171-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="c0171-131">Al llamar a [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use el miembro **rSrc** para los mapas de bits HDC y DirectDraw, para especificar el fotograma o rectángulo determinado dentro de la imagen que desea mostrar, y establezca la marca de **VMRBITMAP \_ SRCRECT** en el miembro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="c0171-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0171-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0171-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0171-133">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="c0171-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



