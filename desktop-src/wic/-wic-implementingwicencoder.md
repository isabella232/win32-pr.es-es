---
description: Implementación de un codificador WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementación de un codificador WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277774"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="400e7-103">Implementación de un codificador WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="400e7-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="400e7-104">Introducción</span><span class="sxs-lookup"><span data-stu-id="400e7-104">Introduction</span></span>

<span data-ttu-id="400e7-105">La implementación de un codificador de Windows Imaging Component (WIC) requiere la escritura de dos clases, como también se cumple para implementar un descodificador de WIC.</span><span class="sxs-lookup"><span data-stu-id="400e7-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="400e7-106">Las interfaces de estas clases se corresponden directamente con las responsabilidades del codificador que se describen en la sección [codificación](-wic-howwicworks.md) de cómo funciona el componente de creación de imágenes de Windows.</span><span class="sxs-lookup"><span data-stu-id="400e7-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="400e7-107">Una de las clases proporciona servicios de nivel de contenedor y administra la serialización de los fotogramas de imagen individuales dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="400e7-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="400e7-108">Esta clase implementa la interfaz [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="400e7-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="400e7-109">Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en esta clase.</span><span class="sxs-lookup"><span data-stu-id="400e7-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="400e7-110">La otra clase proporciona servicios de nivel de marco y realiza la codificación real de los bits de imagen para cada fotograma del contenedor.</span><span class="sxs-lookup"><span data-stu-id="400e7-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="400e7-111">También recorre en iteración los bloques de metadatos de cada marco y solicita los escritores de metadatos adecuados para serializar los bloques.</span><span class="sxs-lookup"><span data-stu-id="400e7-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="400e7-112">Esta clase implementa la interfaz **IWICBitmapFrameEncode** y la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) .</span><span class="sxs-lookup"><span data-stu-id="400e7-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="400e7-113">Esta clase debe tener un miembro IStream que la clase de nivel de contenedor inicialice en la creación de instancias, en la que el método **commit** serializará los datos del marco.</span><span class="sxs-lookup"><span data-stu-id="400e7-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="400e7-114">En algunos casos, como los formatos sin procesar, es posible que el autor del códec no quiera que las aplicaciones puedan codificar o volver a codificar en el formato sin procesar, ya que el propósito de un archivo sin formato es contener los datos del sensor exactamente como procede de la cámara.</span><span class="sxs-lookup"><span data-stu-id="400e7-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="400e7-115">En los casos en los que el autor del códec no desea habilitar la codificación, sigue siendo necesario implementar un codificador rudimentario solo para habilitar la adición de metadatos.</span><span class="sxs-lookup"><span data-stu-id="400e7-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="400e7-116">En ese caso, el codificador solo necesita admitir los métodos necesarios para escribir metadatos y puede copiar los bits de imagen no tocados desde el descodificador.</span><span class="sxs-lookup"><span data-stu-id="400e7-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="400e7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="400e7-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="400e7-118">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="400e7-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="400e7-119">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="400e7-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="400e7-120">**Vista**</span><span class="sxs-lookup"><span data-stu-id="400e7-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="400e7-121">Implementación de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="400e7-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="400e7-122">Interfaces del codificador</span><span class="sxs-lookup"><span data-stu-id="400e7-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="400e7-123">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="400e7-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="400e7-124">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="400e7-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



