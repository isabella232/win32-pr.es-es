---
description: Implementación de IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementación de IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547051"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="c0bcd-103">Implementación de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c0bcd-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="c0bcd-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c0bcd-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="c0bcd-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0bcd-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="c0bcd-106">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="c0bcd-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="c0bcd-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="c0bcd-108">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="c0bcd-109">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="c0bcd-110">La clase de codificación de nivel de marco implementa esta interfaz para exponer todos los bloques de metadatos y solicitar el escritor de metadatos adecuado para cada bloque.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="c0bcd-111">Si el formato de imagen admite metadatos globales, fuera de cualquier marco individual, también debe implementar esta interfaz en la clase de codificador de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="c0bcd-112">Para obtener una explicación más detallada de los controladores de metadatos, consulte la sección sobre [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en la sección sobre la implementación de un descodificador de WIC-Enabled.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="c0bcd-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0bcd-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="c0bcd-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) para inicializar el escritor de bloque.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="c0bcd-115">Puede obtener el **IWICMetadataBlockReader** desde el descodificador que descodifica la imagen.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="c0bcd-116">Dado que la inicialización de [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) crea una instancia de un escritor de metadatos para cada lector de metadatos expuesto por el objeto **iwicmetadatablockreader** , la aplicación no tiene que solicitar explícitamente un escritor para cada bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="c0bcd-117">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-117">GetWriterByIndex</span></span>

<span data-ttu-id="c0bcd-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) devuelve el objeto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) para el bloque de metadatos nth, donde n es el valor que se pasa en el parámetro *NINDEX* .</span><span class="sxs-lookup"><span data-stu-id="c0bcd-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="c0bcd-119">Si no hay ningún escritor de metadatos registrado que pueda controlar el tipo de metadatos en el bloque nth, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB).</span><span class="sxs-lookup"><span data-stu-id="c0bcd-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="c0bcd-120">Lo serializará como un flujo de bits sin intentar analizarlo.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="c0bcd-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="c0bcd-121">AddWriter</span></span>

<span data-ttu-id="c0bcd-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permite que un llamador agregue un nuevo escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="c0bcd-123">Esto es necesario si una aplicación desea agregar metadatos de un formato diferente al de cualquiera de los bloques de metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="c0bcd-124">Por ejemplo, es posible que una aplicación desee agregar algunos metadatos XMP.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="c0bcd-125">Si no hay ningún bloque de metadatos XMP existente, la aplicación debe crear una instancia de un escritor de metadatos XMP y usar el método **AddWriter** para incluirlo en la colección de escritores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="c0bcd-126">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-126">SetWriterByIndex</span></span>

<span data-ttu-id="c0bcd-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) se utiliza para agregar un escritor de metadatos en un índice específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="c0bcd-128">Si actualmente existe un escritor de metadatos en ese índice, el nuevo debe reemplazarlo.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="c0bcd-129">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="c0bcd-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="c0bcd-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) se utiliza para quitar un escritor de metadatos de la colección.</span><span class="sxs-lookup"><span data-stu-id="c0bcd-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0bcd-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0bcd-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0bcd-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c0bcd-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0bcd-133">Implementar IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="c0bcd-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="c0bcd-134">Instalación y registro de CÓDECs</span><span class="sxs-lookup"><span data-stu-id="c0bcd-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="c0bcd-135">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c0bcd-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c0bcd-136">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c0bcd-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



