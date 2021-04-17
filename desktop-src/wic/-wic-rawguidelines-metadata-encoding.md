---
description: Encoding
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificación (componente de Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716637"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="b10ca-103">Codificación (componente de Windows Imaging)</span><span class="sxs-lookup"><span data-stu-id="b10ca-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="b10ca-104">El autor del codificador debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b10ca-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="b10ca-105">Implementar interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="b10ca-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="b10ca-106">Implemente [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en el codificador de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b10ca-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="b10ca-107">Si el códec admite metadatos de nivel de contenedor, esta interfaz se debe implementar en el codificador de nivel de contenedor, así como en el codificador de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b10ca-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="b10ca-108">Si el formato de contenedor contiene implícitamente cualquier bloque de metadatos obligatorio, cree una instancia de un escritor de metadatos para cada uno de estos bloques.</span><span class="sxs-lookup"><span data-stu-id="b10ca-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="b10ca-109">Por ejemplo, el formato TIFF requiere un dispositivo de interfaz (IFD) para cada fotograma, por lo que el escritor de la IFD siempre debe estar expuesto.</span><span class="sxs-lookup"><span data-stu-id="b10ca-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="b10ca-110">Implementar la compatibilidad para administrar la colección de escritores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="b10ca-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="b10ca-111">El escritor de bloques administra los requisitos de los pedidos o las restricciones de contenedor en los tipos de bloques de metadatos que se pueden codificar.</span><span class="sxs-lookup"><span data-stu-id="b10ca-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="b10ca-112">El escritor de bloques debe comprobar que los nuevos escritores de metadatos se pueden insertar en el formato del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b10ca-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="b10ca-113">Al codificar el flujo de imagen, llame a [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar el contenido de cada escritor de metadatos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b10ca-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="b10ca-114">Si el bloque de metadatos contiene metadatos "críticos", el codificador debe establecer los elementos de metadatos críticos antes de solicitar al escritor de metadatos que serialice el contenido.</span><span class="sxs-lookup"><span data-stu-id="b10ca-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="b10ca-115">Busque los controladores de metadatos desconocidos para asegurarse de que los bloques de metadatos redundantes no están presentes.</span><span class="sxs-lookup"><span data-stu-id="b10ca-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="b10ca-116">Esto es importante porque, mientras se conservan los metadatos en un escenario de descodificación o codificación, los bloques desconocidos podrían ser un duplicado de bloques de metadatos obligatorios.</span><span class="sxs-lookup"><span data-stu-id="b10ca-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b10ca-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b10ca-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b10ca-118">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b10ca-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b10ca-119">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="b10ca-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b10ca-120">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="b10ca-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b10ca-121">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b10ca-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



