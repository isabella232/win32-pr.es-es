---
description: Leer el objeto de encabezado ASF de un archivo existente
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Leer el objeto de encabezado ASF de un archivo existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705891"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="b0e85-103">Leer el objeto de encabezado ASF de un archivo existente</span><span class="sxs-lookup"><span data-stu-id="b0e85-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="b0e85-104">El objeto ContentInfo de ASF almacena información que representa los objetos de encabezado ASF de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="b0e85-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="b0e85-105">Se requiere un objeto ContentInfo rellenado para leer y analizar un archivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="b0e85-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="b0e85-106">Después de crear el objeto ContentInfo mediante una llamada a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , la aplicación debe inicializarlo con la información de encabezado del archivo ASF que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="b0e85-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="b0e85-107">Para rellenar el objeto, llame a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="b0e85-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="b0e85-108">**ParseHeader** requiere un búfer de medios que contenga el objeto de encabezado del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="b0e85-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="b0e85-109">Una opción consiste en rellenar un búfer multimedia con el objeto de encabezado para crear una secuencia de bytes para el archivo y, a continuación, leer los primeros 30 bytes de datos de la secuencia de bytes en un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="b0e85-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="b0e85-110">A continuación, puede obtener el tamaño pasando los primeros 24 bytes del objeto de encabezado al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="b0e85-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="b0e85-111">Después de obtener el tamaño, puede leer el objeto de encabezado completo en un búfer multimedia y pasarlo a **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="b0e85-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="b0e85-112">El método comienza el análisis en el desplazamiento desde el inicio del búfer de medios especificado en el parámetro *cbOffsetWithinHeader* .</span><span class="sxs-lookup"><span data-stu-id="b0e85-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="b0e85-113">En el ejemplo de código siguiente se crea e inicializa un objeto ContentInfo para leer un archivo ASF existente contenido en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="b0e85-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="b0e85-114">En primer lugar, se define una función auxiliar que lee los datos de una secuencia de bytes y asigna un búfer multimedia para almacenar los datos:</span><span class="sxs-lookup"><span data-stu-id="b0e85-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="b0e85-115">En el ejemplo siguiente se lee el objeto de encabezado ASF de una secuencia de bytes y se rellena un objeto ContentInfo ASF.</span><span class="sxs-lookup"><span data-stu-id="b0e85-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> <span data-ttu-id="b0e85-116">En estos ejemplos se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b0e85-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b0e85-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0e85-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e85-118">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="b0e85-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="b0e85-119">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="b0e85-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b0e85-120">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e85-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b0e85-121">Obtener información de los objetos de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="b0e85-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



