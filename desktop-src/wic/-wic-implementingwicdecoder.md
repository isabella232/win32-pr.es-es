---
description: Más información acerca de cómo implementar un descodificador de WIC-Enabled
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementar un descodificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911381"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="b9621-103">Implementar un descodificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9621-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="b9621-104">La implementación de un descodificador de Windows Imaging Component (WIC) requiere la escritura de dos clases.</span><span class="sxs-lookup"><span data-stu-id="b9621-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="b9621-105">Las interfaces de estas clases se corresponden directamente con las responsabilidades del descodificador que se describen en la sección [descodificación](-wic-howwicworks.md) de [Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md).</span><span class="sxs-lookup"><span data-stu-id="b9621-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="b9621-106">Una de las clases proporciona servicios de nivel de contenedor e implementa la interfaz [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) .</span><span class="sxs-lookup"><span data-stu-id="b9621-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="b9621-107">Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la interfaz [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) en esta clase.</span><span class="sxs-lookup"><span data-stu-id="b9621-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="b9621-108">Se recomienda que admita la interfaz [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) en el descodificador y el codificador para admitir una mejor experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="b9621-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="b9621-109">La otra clase que se va a implementar proporciona servicios de nivel de marco y realiza la descodificación real de los bits de imagen para cada fotograma del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b9621-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="b9621-110">Esta clase implementa la interfaz [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) y la interfaz [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) .</span><span class="sxs-lookup"><span data-stu-id="b9621-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="b9621-111">Si está escribiendo un descodificador para un formato sin formato, también debe implementar la interfaz [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) en esta clase.</span><span class="sxs-lookup"><span data-stu-id="b9621-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="b9621-112">Además de las interfaces requeridas, se recomienda encarecidamente implementar la interfaz [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) en esta clase para habilitar el mejor rendimiento posible para el formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="b9621-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="b9621-113">Uno de los objetos proporcionados por WIC es [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="b9621-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="b9621-114">A menudo se usa la interfaz [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) en este objeto para crear varios componentes.</span><span class="sxs-lookup"><span data-stu-id="b9621-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="b9621-115">Dado que se usa con frecuencia, debe mantener una referencia a ella como una propiedad de miembro en las clases del descodificador y del codificador.</span><span class="sxs-lookup"><span data-stu-id="b9621-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="b9621-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9621-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b9621-117">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b9621-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9621-118">Cómo funciona el componente de creación de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="b9621-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="b9621-119">Interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="b9621-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="b9621-120">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9621-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b9621-121">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="b9621-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b9621-122">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="b9621-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="b9621-123">Información general sobre la codificación</span><span class="sxs-lookup"><span data-stu-id="b9621-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



