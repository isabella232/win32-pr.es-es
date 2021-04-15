---
description: Generar un nuevo objeto de encabezado ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Generar un nuevo objeto de encabezado ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539537"
---
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="f5cdd-103">Generar un nuevo objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="f5cdd-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="f5cdd-104">Para convertir la información contenida en el objeto ContentInfo en un formato de objeto de encabezado ASF binario, la aplicación debe llamar a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="f5cdd-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="f5cdd-105">Esta llamada se debe realizar después de que se generen los paquetes de datos y el objeto ContentInfo contiene información actualizada.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="f5cdd-106">**GenerateHeader** devuelve un puntero a un búfer multimedia que contiene la información de encabezado en el formato válido.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="f5cdd-107">A continuación, la aplicación puede escribir los datos, a los que apunta el búfer multimedia, al principio de un nuevo archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="f5cdd-108">Para escribir un nuevo objeto de encabezado mediante el objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="f5cdd-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="f5cdd-109">Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="f5cdd-110">Llame a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para proporcionar el objeto de perfil al objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="f5cdd-111">Para obtener información acerca de la creación de perfiles, consulte [crear un perfil ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="f5cdd-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="f5cdd-112">Llame a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) y pase **null** en el parámetro *pIHeader* y reciba el tamaño del objeto ContentInfo rellenado en el parámetro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="f5cdd-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="f5cdd-113">La aplicación puede utilizar este valor para asignar memoria o el búfer multimedia que contendrá el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="f5cdd-114">El tamaño del encabezado recibido incluye el tamaño del relleno, que se ajusta en función del tamaño real de los objetos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="f5cdd-115">El tamaño máximo de los objetos de encabezado es de 10 MB.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="f5cdd-116">Si el tamaño supera este valor, **GenerateHeader** produce un error con el \_ error INVALIDDATA de MF E \_ ASF \_ .</span><span class="sxs-lookup"><span data-stu-id="f5cdd-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="f5cdd-117">Llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para crear un búfer de medios del tamaño recibido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="f5cdd-118">Vuelva a llamar a **GenerateHeader** para generar el nuevo objeto de encabezado ASF del objeto ContentInfo en el búfer de medios creado en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="f5cdd-119">La longitud de los datos en el búfer multimedia se actualiza y el nuevo tamaño se devuelve en el parámetro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="f5cdd-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="f5cdd-120">Escribe el contenido del búfer multimedia al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="f5cdd-121">La aplicación puede usar el flujo de bytes para realizar la operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="f5cdd-122">Para obtener código de ejemplo, vea [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="f5cdd-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="f5cdd-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5cdd-123">Example</span></span>

<span data-ttu-id="f5cdd-124">En el ejemplo de código siguiente se muestra cómo crear un objeto ContentInfo y generar un búfer multimedia para almacenar el nuevo objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5cdd-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="f5cdd-125">Para obtener un ejemplo completo que usa este código, vea [Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="f5cdd-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f5cdd-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5cdd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5cdd-127">Escribir un objeto de encabezado ASF para un nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="f5cdd-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



