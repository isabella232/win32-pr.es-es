---
description: Un codificador escribe datos de imagen en una secuencia. Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Información general sobre la codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278844"
---
# <a name="encoding-overview"></a>Información general sobre la codificación

Un codificador escribe datos de imagen en una secuencia. Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia. El uso de algunos codificadores produce contrapartidas (por ejemplo, JPEG), que compensa la información de color para una mejor compresión. Otros codificadores no producen tales pérdidas, por ejemplo, mapa de bits (BMP). Dado que muchos códecs usan tecnología propietaria para lograr una mejor compresión y una fidelidad de imagen, los detalles sobre cómo se codifica una imagen son el desarrollador de códecs.

En este tema se incluyen las secciones siguientes.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Ejemplo de codificación TIFF](#tiff-encoding-example)
-   [Uso de las opciones del codificador](#encoder-options-usage)
-   [Opciones del codificador](#encoder-options-usage)
-   [Ejemplos de opciones del codificador](#encoder-options-examples)
-   [Temas relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) es la interfaz principal para codificar una imagen en el formato de destino y usarse para serializar los componentes de una imagen, como miniatura ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) y marcos ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), en el archivo de imagen.

Cómo y cuándo se produce la serialización se dejan al desarrollador de códecs. Cada bloque de datos individual en el formato de archivo de destino debe poder establecerse de forma independiente del orden, pero de nuevo es la decisión del desarrollador de códecs. Sin embargo, una vez que se llama al método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) , no se deben permitir los cambios en la imagen y se debe cerrar la secuencia.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) es la interfaz para codificar los marcos individuales de una imagen. Proporciona métodos para establecer componentes de creación de imágenes de fotogramas individuales, como miniaturas y fotogramas, así como dimensiones de imagen, PPP y formatos de píxel.

Los fotogramas individuales se pueden codificar con metadatos específicos del marco para que [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) proporcione acceso a un escritor de metadatos mediante el método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

El método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del marco confirma todos los cambios en el marco individual e indica que ya no se deben aceptar los cambios en ese marco.

## <a name="tiff-encoding-example"></a>Ejemplo de codificación TIFF

En el ejemplo siguiente, una imagen de Tagged Image File Format (TIFF) se codifica mediante [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). La salida TIFF se personaliza mediante [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) y el marco de mapa de bits se inicializa con las opciones especificadas. Una vez que la imagen se ha creado con [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), el marco se confirma mediante la [**confirmación**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) y la imagen se guarda con [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Uso de las opciones del codificador

Los distintos codificadores para distintos formatos deben exponer distintas opciones para la codificación de una imagen. El componente de creación de imágenes de Windows (WIC) proporciona un mecanismo coherente para expresar si se requieren opciones de codificación mientras se sigue permitiendo que las aplicaciones funcionen con varios codificadores sin necesidad de conocer un formato determinado. Esto se consigue proporcionando un parámetro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) en el método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) y el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .

El generador de componentes proporciona un punto de creación fácil para crear un contenedor de propiedades de opciones de codificador. Los códecs pueden usar este servicio si necesitan proporcionar un conjunto simple, intuitivo y no conflictivo de opciones de codificador. La bolsa de propiedades de imágenes debe inicializarse durante la creación con todas las opciones de codificador relevantes para ese códec. En el caso de las opciones del codificador del conjunto canónico, el intervalo de valores se aplicará en la escritura. En el caso de las necesidades más avanzadas, los códecs deben escribir su propia implementación de contenedor de propiedades.

A una aplicación se le asigna el contenedor de opciones del codificador durante la creación del marco y debe configurar los valores antes de inicializar el marco del codificador. En el caso de una aplicación controlada por la interfaz de usuario, puede ofrecer una interfaz de usuario fija para las opciones canónicas del codificador y una vista avanzada para las opciones restantes. Los cambios se pueden realizar de una en una a través del método Write y cualquier error se informará a través de IErrorLog. La aplicación de interfaz de usuario siempre debe volver a leer y mostrar todas las opciones después de realizar un cambio en caso de que el cambio provocó un efecto en cascada. Una aplicación debe estar preparada para controlar la inicialización de fotogramas con errores para códecs que solo proporcionan informes de errores mínimos a través de su contenedor de propiedades.

## <a name="encoder-options"></a>Opciones del codificador

Una aplicación puede esperar encontrar el siguiente conjunto de opciones de codificador. Las opciones del codificador reflejan las capacidades de un codificador y el formato del contenedor subyacente y, por tanto, son por su naturaleza no es independiente del códec. Cuando sea posible, se deben normalizar las nuevas opciones para que se puedan aplicar a los nuevos códecs que surjan.



| Nombre de la propiedad      | VARTYPE  | Value                                                                     | Códecs aplicables |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1,0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1,0                                                                     | TIFF              |
| Lossless           | VT \_ bool | **true**, **false**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

El valor de ImageQualty de 0,0 significa que la última copia de fidelidad posible y 1,0 significa la mayor fidelidad, que también puede implicar pérdida de pérdida según el códec.

CompressionQuality es el esquema 0,0 de compresión menos eficaz disponible, que normalmente produce una codificación rápida pero una salida más grande. Un valor de 1,0 significa que el esquema más eficaz disponible, normalmente tarda más tiempo en codificarse, pero generando una salida más pequeña. En función de las capacidades del códec, este intervalo se puede asignar a un conjunto discreto de métodos de compresión disponibles.

Sin pérdida significa que el códec codifica la imagen como Lossless sin pérdida de datos de imagen. Si se habilita Lossless, se omite ImageQuality.

Además de las opciones de codificador genéricas anteriores, los códecs suministrados con WIC admiten las siguientes opciones. Si un códec tiene la necesidad de admitir una opción coherente con el uso de estos códecs suministrados, se recomienda hacerlo.



| Nombre de la propiedad           | VARTYPE           | Value                                                                             | Códecs aplicables |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ bool          | Activado/Desactivado                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | Matriz de VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | JPEG              |
| Chrominance             | Matriz de VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ bool          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ bool          | Activado/Desactivado                                                                            | BMP               |



 

Use **VT \_ vacío** para indicar que **\* no \* se ha establecido** como valor predeterminado. Si se establecen propiedades adicionales pero no se admiten, el codificador debe omitirlas. Esto permite que las aplicaciones codifiquen menos lógica si desean una funcionalidad que puede estar presente o no.

## <a name="encoder-options-examples"></a>Ejemplos de opciones del codificador

En el [ejemplo de codificación TIFF](#tiff-encoding-example) anterior, se establece una opción de codificador específica. El miembro *pstrName* de la estructura PROPBAG2 se establece en el nombre de propiedad adecuado y la variante se establece en el VARTYPE correspondiente y en el valor deseado (en este caso, un miembro de la enumeración [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) ).


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Para usar las opciones predeterminadas del codificador, solo tiene que inicializar el marco de mapa de bits con el contenedor de propiedades devuelto cuando se creó el marco.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



También es posible eliminar el contenedor de propiedades cuando no se están considerando opciones de codificador.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre descodificación](-wic-creating-decoder.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
