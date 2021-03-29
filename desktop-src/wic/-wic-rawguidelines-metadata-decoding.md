---
description: Descodificación
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Descodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911937"
---
# <a name="decoding"></a><span data-ttu-id="5876c-103">Descodificación</span><span class="sxs-lookup"><span data-stu-id="5876c-103">Decoding</span></span>

<span data-ttu-id="5876c-104">Para admitir correctamente los metadatos, los autores del descodificador deben hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5876c-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="5876c-105">Implementar interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="5876c-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="5876c-106">Implemente [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en el descodificador de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="5876c-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="5876c-107">Si el códec admite metadatos de nivel de contenedor, esta interfaz se debe implementar en el descodificador de nivel de contenedor, así como en el descodificador de Marcos.</span><span class="sxs-lookup"><span data-stu-id="5876c-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="5876c-108">Al descodificar el flujo de imagen, llame a [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para crear instancias de un lector de metadatos para cada bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="5876c-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="5876c-109">(Los nuevos lectores de metadatos que implemente el códec deben estar registrados con WIC).</span><span class="sxs-lookup"><span data-stu-id="5876c-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="5876c-110">El descodificador no debe crear lectores de metadatos por sí mismo, sino usar WIC para crearlos en función de los bloques de metadatos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5876c-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="5876c-111">El descodificador debe hacerlo en todos los bloques que encuentra, incluso si no son conocidos de forma nativa por el codificador, porque es posible que los lectores de metadatos futuros estén instalados en el sistema que comprenden cómo administrar estos bloques de metadatos.</span><span class="sxs-lookup"><span data-stu-id="5876c-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="5876c-112">Si no hay ningún controlador de metadatos para un bloque, cree una instancia del lector de metadatos desconocido mediante las opciones de creación de metadatos.</span><span class="sxs-lookup"><span data-stu-id="5876c-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="5876c-113">Exponga la colección de lectores de metadatos a través de la interfaz [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="5876c-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5876c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5876c-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5876c-115">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5876c-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5876c-116">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="5876c-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="5876c-117">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="5876c-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="5876c-118">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5876c-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



