---
description: Leer el objeto de encabezado ASF de un archivo existente
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Leer el objeto de encabezado ASF de un archivo existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e653154d632786995bdf45dcfa8e67e3cfd55cdf3f90103ce1cf995179e1266b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887345"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Leer el objeto de encabezado ASF de un archivo existente

El objeto ContentInfo de ASF almacena información que representa los objetos de encabezado ASF de un archivo multimedia. Se requiere un objeto ContentInfo rellenado para leer y analizar un archivo ASF existente.

Después de crear el objeto ContentInfo llamando a la función [**MFCreateASFContentInfo,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) la aplicación debe inicializarse con información de encabezado del archivo ASF que se va a leer. Para rellenar el objeto , llame [**a IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).

**ParseHeader requiere** un búfer multimedia que contenga el objeto de encabezado del archivo ASF. Una opción es rellenar un búfer multimedia con el objeto de encabezado para crear una secuencia de bytes para el archivo y, a continuación, leer los primeros 30 bytes de datos de la secuencia de bytes en un búfer multimedia. A continuación, puede obtener el tamaño pasando los primeros 24 bytes del objeto header al [**método IMFASFContentInfo::GetHeaderSize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) Después de obtener el tamaño, puede leer todo el objeto de encabezado en un búfer multimedia y pasarlo a **ParseHeader**. El método inicia el análisis en el desplazamiento desde el inicio del búfer multimedia especificado en el *parámetro cbOffsetWithinHeader.*

El código de ejemplo siguiente crea e inicializa un objeto ContentInfo para leer un archivo ASF existente contenido en una secuencia de bytes. En primer lugar, definimos una función auxiliar que lee datos de una secuencia de bytes y asigna un búfer multimedia para contener los datos:


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



En el ejemplo siguiente se lee el objeto de encabezado asf de una secuencia de bytes y se rellena un objeto ContentInfo de ASF.


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
> En estos ejemplos se usa [la función SafeRelease para](saferelease.md) liberar punteros de interfaz.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Obtener información de objetos de encabezado de ASF](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



