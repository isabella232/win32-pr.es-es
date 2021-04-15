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
# <a name="generating-a-new-asf-header-object"></a>Generar un nuevo objeto de encabezado ASF

Para convertir la información contenida en el objeto ContentInfo en un formato de objeto de encabezado ASF binario, la aplicación debe llamar a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Esta llamada se debe realizar después de que se generen los paquetes de datos y el objeto ContentInfo contiene información actualizada. **GenerateHeader** devuelve un puntero a un búfer multimedia que contiene la información de encabezado en el formato válido. A continuación, la aplicación puede escribir los datos, a los que apunta el búfer multimedia, al principio de un nuevo archivo ASF.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Para escribir un nuevo objeto de encabezado mediante el objeto ContentInfo

1.  Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo vacío.
2.  Llame a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para proporcionar el objeto de perfil al objeto ContentInfo. Para obtener información acerca de la creación de perfiles, consulte [crear un perfil ASF](creating-an-asf-profile.md).
3.  Llame a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) y pase **null** en el parámetro *pIHeader* y reciba el tamaño del objeto ContentInfo rellenado en el parámetro *pcbHeader* . La aplicación puede utilizar este valor para asignar memoria o el búfer multimedia que contendrá el objeto de encabezado.

    El tamaño del encabezado recibido incluye el tamaño del relleno, que se ajusta en función del tamaño real de los objetos de encabezado. El tamaño máximo de los objetos de encabezado es de 10 MB. Si el tamaño supera este valor, **GenerateHeader** produce un error con el \_ error INVALIDDATA de MF E \_ ASF \_ .

4.  Llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para crear un búfer de medios del tamaño recibido en el paso 3.
5.  Vuelva a llamar a **GenerateHeader** para generar el nuevo objeto de encabezado ASF del objeto ContentInfo en el búfer de medios creado en el paso 4.

    La longitud de los datos en el búfer multimedia se actualiza y el nuevo tamaño se devuelve en el parámetro *pcbHeader* .

6.  Escribe el contenido del búfer multimedia al principio del archivo. La aplicación puede usar el flujo de bytes para realizar la operación de escritura. Para obtener código de ejemplo, vea [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo crear un objeto ContentInfo y generar un búfer multimedia para almacenar el nuevo objeto de encabezado. Para obtener un ejemplo completo que usa este código, vea [Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



