---
title: Carga de una imagen en efectos de Direct2D mediante FilePicker
description: Muestra cómo usar el Windows Storage selectores de archivosOpenPicker para cargar una imagen en efectos de Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160536"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Carga de una imagen en efectos de Direct2D mediante FilePicker

Muestra cómo usar el [**Windows::Storage::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para cargar una imagen en efectos [de Direct2D.](effects-overview.md) Si desea permitir que el usuario seleccione un archivo de imagen del almacenamiento en una aplicación de Windows Store, se recomienda usar [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Direct2D](./direct2d-portal.md)
-   [Efectos de Direct2D](effects-overview.md)
-   [**Windows::Storage::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Prerrequisitos

-   Necesita un objeto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear efectos.
-   Necesita un objeto [**IWICImagingFactory para**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) crear objetos WIC.

## <a name="instructions"></a>Instructions

### <a name="step-1-open-the-file-picker"></a>Paso 1: Abrir el selector de archivos

Cree un [**objeto FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) y establezca *ViewMode*, *SuggestedStartLocation* y *FileTypeFilter* para seleccionar imágenes. Llame al [**método PickSingleFileAsync.**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync)


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Una vez [**completado PickSingleFileAsync,**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) se obtiene una secuencia de archivos de la [**interfaz IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) que devuelve.

### <a name="step-2-get-a-file-stream"></a>Paso 2: Obtener una secuencia de archivos

Declare un controlador de finalización para que se ejecute después de que se devuelva la operación asincrónica del selector de archivos. Use el [**método GetResults**](/previous-versions//br205815(v=vs.85)) para recuperar el archivo y obtener el objeto de secuencia de archivos.


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



En el paso siguiente se convierte el [**objeto IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) en un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que se puede pasar a [WIC.](/windows/desktop/wic/-wic-api)

### <a name="step-3-convert-the-file-stream"></a>Paso 3: Conversión de la secuencia de archivos

Use la [**función CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para convertir la secuencia de archivos. Windows Las API en tiempo de ejecución representan secuencias [**con IRandomAccessStream,**](/previous-versions//hh438400(v=vs.85))mientras [que WIC](/windows/desktop/wic/-wic-api) consume [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> Para usar [**la función CreateStreamOverRandomAccessStream,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) debe incluir *shcore.h* en el proyecto.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Paso 4: Crear un descodificador wic y obtener el marco

Cree un [**objeto IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) mediante el método [**IWICImagingFactory::CreateDecoderFromStream.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



Obtenga el primer fotograma de la imagen del descodificador mediante el método [**IWICBitmapDecoder::GetFrame.**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Paso 5: Crear un convertidor de WIC e inicializar

Convierta la imagen al formato de color BGRA mediante [WIC](/windows/desktop/wic/-wic-api). [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) devolverá el formato de píxel nativo de la imagen, al igual que los JPEG se almacenan en GUID \_ WICPixelFormat24bppBGR. Sin embargo, como optimización del rendimiento con Direct2D, se recomienda convertir a WICPixelFormat32bppPBGRA.

1.  Cree un [**objeto IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) mediante el [**método IWICImagingFactory::CreateFormatConverter.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Inicialice el convertidor de formato para usar WICPixelFormat32bppPBGRA y pase el marco de mapa de bits.

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

La [**interfaz IWICFormatConverter se**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) deriva de la interfaz [**IWICBitmapSource,**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) por lo que puede pasar el convertidor al efecto de origen del mapa [de](bitmap-source.md) bits.

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Paso 6: Crear efecto y pasar un IWICBitmapSource

Use el [**método CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) para crear un [objeto](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) de origen de mapa de bits mediante el [contexto del dispositivo Direct2D](getting-started-with-direct2d.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).

Use el [**método ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) para establecer la propiedad *D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC BITMAP \_ \_ SOURCE* en el convertidor [de formato WIC](/windows/desktop/wic/-wic-api) [](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).

> [!Note]  
> El [efecto de origen del](bitmap-source.md) mapa de bits no toma una entrada del método [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) como muchos efectos de [Direct2D.](effects-overview.md) En su lugar, [**el objeto IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) se especifica como una propiedad.

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



Ahora que tiene el efecto [de origen del](bitmap-source.md) mapa de bits, puede usarlo como entrada para cualquier [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) y crear un gráfico de efectos.

## <a name="complete-example"></a>Ejemplo completo

Este es el código completo de este ejemplo.


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 