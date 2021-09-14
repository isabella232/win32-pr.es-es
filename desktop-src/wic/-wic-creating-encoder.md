---
description: Un codificador escribe datos de imagen en una secuencia. Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Información general sobre codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359616"
---
# <a name="encoding-overview"></a>Información general sobre codificación

Un codificador escribe datos de imagen en una secuencia. Los codificadores pueden comprimir, cifrar y modificar los píxeles de la imagen de varias maneras antes de escribirlos en la secuencia. El uso de algunos codificadores da como resultado un ajuste, por ejemplo, JPEG, que negocia la información de color para mejorar la compresión. Otros codificadores no tienen como resultado dichas pérdidas, por ejemplo, mapa de bits (BMP). Dado que muchos códecs usan tecnología propietaria para lograr una mejor compresión y fidelidad de la imagen, los detalles sobre cómo se codifica una imagen están en función del desarrollador del códec.

En este tema se incluyen las secciones siguientes.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Ejemplo de codificación TIFF](#tiff-encoding-example)
-   [Uso de opciones del codificador](#encoder-options-usage)
-   [Opciones del codificador](#encoder-options-usage)
-   [Ejemplos de opciones de codificador](#encoder-options-examples)
-   [Temas relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder es**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) la interfaz principal para codificar una imagen en el formato de destino y se usa para serializar los componentes de una imagen, como miniaturas [**(SetThumbnail)**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)y fotogramas [**(CreateNewFrame),**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)en el archivo de imagen.

Cómo y cuándo se produce la serialización se deja en el desarrollador del códec. Cada bloque individual de datos en el formato de archivo de destino debe ser capaz de establecerse independientemente del orden, pero de nuevo, esta es la decisión del desarrollador del códec. Sin [**embargo,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) una vez que se llama al método Commit, no se deben permitir cambios en la imagen y se debe cerrar la secuencia.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) es la interfaz para codificar los fotogramas individuales de una imagen. Proporciona métodos para establecer componentes individuales de creación de imágenes de fotogramas, como miniaturas y marcos, así como dimensiones de imagen, PPP y formatos de píxel.

Los fotogramas individuales se pueden codificar con metadatos específicos del marco, por lo que [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) proporciona acceso a un escritor de metadatos a través del [**método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)

El método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del marco confirma todos los cambios en el marco individual e indica que ya no se deben aceptar los cambios en ese marco.

## <a name="tiff-encoding-example"></a>Ejemplo de codificación TIFF

En el ejemplo siguiente, una imagen Tagged Image File Format (TIFF) se codifica mediante [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). La salida TIFF se personaliza mediante [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) y el marco de mapa de bits se inicializa con las opciones especificadas. Una vez creada la imagen mediante [**WritePixels,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)el marco se confirma mediante [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) y la imagen se guarda mediante [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


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
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

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



## <a name="encoder-options-usage"></a>Uso de opciones del codificador

Los distintos codificadores para distintos formatos deben exponer diferentes opciones para cómo se codifica una imagen. Windows El componente de creación de imágenes (WIC) proporciona un mecanismo coherente para expresar si se requieren opciones de codificación a la vez que permite que las aplicaciones funcionen con varios codificadores sin necesidad de conocer un formato determinado. Esto se logra proporcionando un parámetro [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) en el [**método CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) y el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)

El generador de componentes proporciona un punto de creación sencillo para crear un bolsa de propiedades de opciones del codificador. Los códecs pueden usar este servicio si necesitan proporcionar un conjunto sencillo, intuitivo y no conflictivo de opciones de codificador. El bolsa de propiedades de creación de imágenes se debe inicializar durante la creación con todas las opciones del codificador pertinentes para ese códec. Para las opciones de codificador del conjunto canónico, el intervalo de valores se aplicará en Escritura. Para necesidades más avanzadas, los códecs deben escribir su propia implementación de bolsa de propiedades.

Una aplicación tiene el bolsa de opciones del codificador durante la creación del fotograma y debe configurar los valores antes de inicializar el marco del codificador. Para una aplicación controlada por la interfaz de usuario, puede ofrecer una interfaz de usuario fija para las opciones del codificador canónico y una vista avanzada para las opciones restantes. Los cambios se pueden realizar de uno en uno a través del método Write y cualquier error se notifica a través de IErrorLog. La aplicación de interfaz de usuario siempre debe volver a leer y mostrar todas las opciones después de realizar un cambio en caso de que el cambio produjese un efecto en cascada. Una aplicación debe estar preparada para controlar la inicialización de fotogramas con error para códecs que solo proporcionan informes de errores mínimos a través de su bolsa de propiedades.

## <a name="encoder-options"></a>Opciones del codificador

Una aplicación puede esperar encontrar el siguiente conjunto de opciones de codificador. Las opciones del codificador reflejan las funcionalidades de un codificador y el formato de contenedor subyacente y, por lo tanto, no son realmente independientes del códec por su naturaleza. Cuando sea posible, se deben normalizar las nuevas opciones para que se puedan aplicar a nuevos códecs que surjan.



| Nombre de la propiedad      | VARTYPE  | Value                                                                     | Códecs aplicables |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1.0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1.0                                                                     | TIFF              |
| Lossless           | VT \_ BOOL | **TRUE**, **FALSE**                                                       | HDPhoto           |
| BitmapTransform    | VT \_ UI1  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty de 0,0 significa la representación de fidelidad más baja posible y 1,0 significa la fidelidad más alta, lo que también puede implicar la pérdida de datos en función del códec.

CompressionQuality de 0,0 significa el esquema de compresión menos eficaz disponible, lo que normalmente da lugar a una codificación rápida pero una salida mayor. Un valor de 1,0 significa el esquema más eficaz disponible, que normalmente tarda más tiempo en codificar, pero genera una salida más pequeña. En función de las funcionalidades del códec, este intervalo se puede asignar a un conjunto discreto de métodos de compresión disponibles.

Sin pérdida de datos significa que el códec codifica la imagen como sin pérdida sin pérdida de datos de imagen. Si La opción Sin pérdida está habilitada, se omite ImageQuality.

Además de las opciones de codificador genérico anteriores, los códecs proporcionados con WIC admiten las siguientes opciones. Si un códec tiene la necesidad de admitir una opción coherente con el uso de estos códecs proporcionados, se recomienda hacerlo.



| Nombre de la propiedad           | VARTYPE           | Value                                                                             | Códecs aplicables |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ BOOL          | Activado/Desactivado                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/VT \_ ARRAY | 64 entradas (DCT)                                                                  | JPEG              |
| Chrominance             | VT \_ UI4/VT \_ ARRAY | 64 entradas (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**WICOptionegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ BOOL          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ BOOL          | Activado/Desactivado                                                                            | BMP               |



 

Use **VT EMPTY \_ para** indicar **\* que no está establecido \*** como valor predeterminado. Si se establecen propiedades adicionales pero no se admiten, el codificador debe ignorarlas; esto permite a las aplicaciones codificar menos lógica si quieren una funcionalidad que puede estar presente o no.

## <a name="encoder-options-examples"></a>Ejemplos de opciones de codificador

En el ejemplo [de codificación TIFF anterior,](#tiff-encoding-example) se establece una opción de codificador específica. El *miembro pstrName* de la estructura PROPBAG2 se establece en el nombre de propiedad adecuado y VARIANT se establece en el VARTYPE correspondiente y el valor deseado, en este caso, un miembro de la enumeración [**WICTiffCompressionOption.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)


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



Para usar las opciones predeterminadas del codificador, basta con inicializar el marco de mapa de bits con la bolsa de propiedades devuelta cuando se creó el marco.


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



También es posible eliminar el bolsa de propiedades cuando no se tiene en cuenta ninguna opción del codificador.


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

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre lacoding](-wic-creating-decoder.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
