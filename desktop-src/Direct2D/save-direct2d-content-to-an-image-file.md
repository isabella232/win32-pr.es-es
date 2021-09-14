---
title: Cómo guardar el contenido de Direct2D en un archivo de imagen
description: En este tema se muestra cómo usar IWICImageEncoder para guardar contenido en forma de ID2D1Image en un archivo de imagen codificado como JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162598"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Cómo guardar el contenido de Direct2D en un archivo de imagen

En este tema se muestra cómo usar [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para guardar contenido en forma de [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en un archivo de imagen codificado como JPEG. Si va a escribir una aplicación de Windows Store, puede hacer que el usuario seleccione un archivo de destino [**mediante Windows::Storage::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Direct2D](./direct2d-portal.md)
-   [Efectos de Direct2D](effects-overview.md)
-   [**Windows::Storage::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Requisitos previos

-   Necesita un [**objeto ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) y un objeto que contenga contenido de [Direct2D](./direct2d-portal.md) que implemente [**ID2D1Image,**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) o [**ID2D1Bitmap1.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)

## <a name="instructions"></a>Instructions

### <a name="step-1-get-a-destination-file-and-stream"></a>Paso 1: Obtener un archivo de destino y una secuencia

Si desea permitir que el usuario seleccione un archivo de destino, puede usar [**FileSavePicker,**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)abrir el archivo devuelto y obtener un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) para usarlo con WIC.

Cree un [**Windows::Storage::P ickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) y establezca sus parámetros para los archivos de imagen. Llame al [**método PickSaveFileAsync.**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync)


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



Declare un controlador de finalización para que se ejecute después de que se devuelva la operación asincrónica del selector de archivos. Use el [**método GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) para recuperar el archivo y obtener el objeto de secuencia de archivos.


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



Obtenga un [**elemento IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) llamando [**a OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) en el archivo y obteniendo el resultado de la operación asincrónica.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Por último, use [**el método CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para convertir la secuencia de archivos. Windows Las API en tiempo de ejecución representan secuencias [**con IRandomAccessStream,**](/previous-versions//hh438400(v=vs.85))mientras que WIC consume [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Para usar la [**función CreateStreamOverRandomAccessStream,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) debe incluir **shcore.h** en el proyecto.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Paso 2: Obtener el mapa de bits de WIC y el codificador de fotogramas

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) proporcionan la funcionalidad para guardar los datos de creación de imágenes en un formato de archivo codificado.

Cree e inicialice los objetos del codificador.


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a>Paso 3: Obtener un IWICImageEncoder

[**IWICImageEncoder es**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) una nueva interfaz en Windows 8. Se puede crear a partir [**de IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), que extiende **IWICImagingFactory** y también es nuevo para Windows 8.


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



Llame [**a IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). El primer parámetro es [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) y debe ser el dispositivo en el que se creó la imagen que desea codificar: no se pueden mezclar imágenes de dominios de recursos diferentes dentro de un único [**IWICImageEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Paso 4: Escritura del contenido de Direct2D mediante IWICImageEncoder

[**IWICImageEncoder puede**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) escribir una imagen [de Direct2D](./direct2d-portal.md) en un marco de imagen, una miniatura de marco o la miniatura del contenedor. A continuación, puede usar [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) para codificar los datos de creación de imágenes en un archivo de la forma habitual.

Escriba la [imagen de Direct2D](./direct2d-portal.md) en el marco. En este fragmento de código se escribe [**un ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que contiene contenido de Direct2D rasterizado. Sin embargo, puede proporcionar cualquier interfaz que implemente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> El [**parámetro ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) debe haber sido creado en [**el id2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) que se pasó a [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).

 

Confirme el WIC y los recursos de transmisión para finalizar la operación.


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> Algunas implementaciones de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) no implementan el [**método Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) y **devuelven E \_ NOTIMPL**.

 

Ahora tiene un archivo que contiene la [imagen de Direct2D.](./direct2d-portal.md)

## <a name="complete-example"></a>Ejemplo completo

Aquí se muestra el código completo de este ejemplo.

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 