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
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Leer el objeto de encabezado ASF de un archivo existente

El objeto ContentInfo de ASF almacena información que representa los objetos de encabezado ASF de un archivo multimedia. Se requiere un objeto ContentInfo rellenado para leer y analizar un archivo ASF existente.

Después de crear el objeto ContentInfo mediante una llamada a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , la aplicación debe inicializarlo con la información de encabezado del archivo ASF que se va a leer. Para rellenar el objeto, llame a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).

**ParseHeader** requiere un búfer de medios que contenga el objeto de encabezado del archivo ASF. Una opción consiste en rellenar un búfer multimedia con el objeto de encabezado para crear una secuencia de bytes para el archivo y, a continuación, leer los primeros 30 bytes de datos de la secuencia de bytes en un búfer multimedia. A continuación, puede obtener el tamaño pasando los primeros 24 bytes del objeto de encabezado al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Después de obtener el tamaño, puede leer el objeto de encabezado completo en un búfer multimedia y pasarlo a **ParseHeader**. El método comienza el análisis en el desplazamiento desde el inicio del búfer de medios especificado en el parámetro *cbOffsetWithinHeader* .

En el ejemplo de código siguiente se crea e inicializa un objeto ContentInfo para leer un archivo ASF existente contenido en una secuencia de bytes. En primer lugar, se define una función auxiliar que lee los datos de una secuencia de bytes y asigna un búfer multimedia para almacenar los datos:


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



En el ejemplo siguiente se lee el objeto de encabezado ASF de una secuencia de bytes y se rellena un objeto ContentInfo ASF.


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
> En estos ejemplos se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Obtener información de los objetos de encabezado ASF](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



