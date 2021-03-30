---
description: Implementación de IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementación de IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816091"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="07177-103">Implementación de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="07177-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="07177-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="07177-104">IWICBitmapSource</span></span>

<span data-ttu-id="07177-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) es importante para trabajar con imágenes desde la perspectiva de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="07177-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="07177-106">Representa la abstracción de nivel superior para un origen de imagen y todas las interfaces de componentes de imágenes de Windows (WIC) que representan una imagen, como [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), y todas las interfaces de transformación ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)y [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) se derivan de ella.</span><span class="sxs-lookup"><span data-stu-id="07177-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="07177-107">En cualquier momento determinado, un objeto **IWICBitmapSource** puede o no estar respaldado por un mapa de bits real en la memoria.</span><span class="sxs-lookup"><span data-stu-id="07177-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="07177-108">Esto permite un procesamiento muy eficaz de una aplicación, ya que una imagen se puede tratar como una abstracción.</span><span class="sxs-lookup"><span data-stu-id="07177-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="07177-109">Las operaciones de transformación se pueden encadenar en una canalización de transformación sin consumir recursos de memoria hasta que la aplicación esté lista para representar o imprimir la imagen, momento en que invoca el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) en la transformación final para obtener un mapa de bits en la memoria de la imagen con las transformaciones seleccionadas aplicadas.</span><span class="sxs-lookup"><span data-stu-id="07177-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="07177-110">Desde la perspectiva del códec, los métodos de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) se implementan en el objeto de descodificador de marco.</span><span class="sxs-lookup"><span data-stu-id="07177-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="07177-111">Estos métodos se describen en implementar IWICBitmapSource, junto con los otros métodos de [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), que se derivan de **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="07177-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07177-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07177-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="07177-113">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="07177-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07177-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="07177-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="07177-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="07177-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="07177-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="07177-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="07177-117">**Vista**</span><span class="sxs-lookup"><span data-stu-id="07177-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07177-118">Implementación de IWICBitmapCodecProgressNotification (descodificador)</span><span class="sxs-lookup"><span data-stu-id="07177-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="07177-119">Implementación de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="07177-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="07177-120">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="07177-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="07177-121">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="07177-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



