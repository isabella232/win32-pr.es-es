---
title: Cómo guardar el contenido de Direct2D en un archivo de imagen
description: En este tema se muestra cómo usar IWICImageEncoder para guardar contenido en forma de ID2D1Image en un archivo de imagen codificado, como JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904651"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="20cc9-103">Cómo guardar el contenido de Direct2D en un archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="20cc9-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="20cc9-104">En este tema se muestra cómo usar [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para guardar contenido en forma de [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en un archivo de imagen codificado, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="20cc9-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="20cc9-105">Si está escribiendo una aplicación de la tienda Windows, puede hacer que el usuario seleccione un archivo de destino mediante [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span><span class="sxs-lookup"><span data-stu-id="20cc9-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="20cc9-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="20cc9-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="20cc9-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="20cc9-107">Technologies</span></span>

-   [<span data-ttu-id="20cc9-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="20cc9-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="20cc9-109">Efectos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="20cc9-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="20cc9-110">**Windows:: Storage::P ickers:: FileSavePicker**</span><span class="sxs-lookup"><span data-stu-id="20cc9-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="20cc9-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="20cc9-111">Prerequisites</span></span>

-   <span data-ttu-id="20cc9-112">Necesita un objeto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) y un objeto que contiene contenido de [Direct2D](./direct2d-portal.md) que implementa [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) o [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span><span class="sxs-lookup"><span data-stu-id="20cc9-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="20cc9-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="20cc9-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="20cc9-114">Paso 1: obtener un archivo de destino y una secuencia</span><span class="sxs-lookup"><span data-stu-id="20cc9-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="20cc9-115">Si desea permitir que el usuario seleccione un archivo de destino, puede usar [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), abrir el archivo devuelto y obtener una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) para usarla con WIC.</span><span class="sxs-lookup"><span data-stu-id="20cc9-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="20cc9-116">Cree un [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) y establezca sus parámetros para los archivos de imagen.</span><span class="sxs-lookup"><span data-stu-id="20cc9-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="20cc9-117">Llame al método [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .</span><span class="sxs-lookup"><span data-stu-id="20cc9-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


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



<span data-ttu-id="20cc9-118">Declare un controlador de finalización para que se ejecute después de que se devuelva la operación asincrónica del selector de archivos.</span><span class="sxs-lookup"><span data-stu-id="20cc9-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="20cc9-119">Use el método [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) para recuperar el archivo y obtener el objeto de secuencia de archivo.</span><span class="sxs-lookup"><span data-stu-id="20cc9-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="20cc9-120">Obtenga una [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) llamando a [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) en el archivo y obteniendo el resultado de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="20cc9-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="20cc9-121">Por último, use el método [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para convertir la secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="20cc9-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="20cc9-122">Windows Runtime API representan secuencias con [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), mientras que WIC consume [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="20cc9-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="20cc9-123">Para usar la función [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , debe incluir **shcore. h** en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="20cc9-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="20cc9-124">Paso 2: obtener el codificador de mapas de bits y tramas de WIC</span><span class="sxs-lookup"><span data-stu-id="20cc9-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="20cc9-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) y [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) proporcionan la funcionalidad para guardar los datos de la imagen en un formato de archivo codificado.</span><span class="sxs-lookup"><span data-stu-id="20cc9-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="20cc9-126">Cree e inicialice los objetos del codificador.</span><span class="sxs-lookup"><span data-stu-id="20cc9-126">Create and initialize the encoder objects.</span></span>


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



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="20cc9-127">Paso 3: obtener un IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="20cc9-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="20cc9-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) es una nueva interfaz de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20cc9-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="20cc9-129">Se puede crear a partir de [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), que amplía **IWICImagingFactory** y también es nuevo para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20cc9-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


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



<span data-ttu-id="20cc9-130">Llame a [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="20cc9-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="20cc9-131">El primer parámetro es un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) y debe ser el dispositivo en el que se creó la imagen que quiere codificar: no se pueden mezclar imágenes de distintos dominios de recursos dentro de un solo [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span><span class="sxs-lookup"><span data-stu-id="20cc9-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="20cc9-132">Paso 4: escribir el contenido de Direct2D mediante IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="20cc9-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="20cc9-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) puede escribir una imagen de [Direct2D](./direct2d-portal.md) en un marco de imagen, una miniatura de marco o la miniatura del contenedor.</span><span class="sxs-lookup"><span data-stu-id="20cc9-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="20cc9-134">Después, puede usar [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) y [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) para codificar los datos de la imagen en un archivo de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="20cc9-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="20cc9-135">Escriba la imagen de [Direct2D](./direct2d-portal.md) en el marco.</span><span class="sxs-lookup"><span data-stu-id="20cc9-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="20cc9-136">En este fragmento de código, escribimos un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que contiene contenido de Direct2D rasterizado.</span><span class="sxs-lookup"><span data-stu-id="20cc9-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="20cc9-137">Sin embargo, puede proporcionar cualquier interfaz que implemente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span><span class="sxs-lookup"><span data-stu-id="20cc9-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


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
> <span data-ttu-id="20cc9-138">El parámetro [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) se debe haber creado en el [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) que se pasó a [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="20cc9-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="20cc9-139">Confirme los recursos de WIC y de secuencia para finalizar la operación.</span><span class="sxs-lookup"><span data-stu-id="20cc9-139">Commit the WIC and stream resources to finalize the operation.</span></span>


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
> <span data-ttu-id="20cc9-140">Algunas implementaciones de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) no implementan el método [**commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) y devuelven **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="20cc9-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="20cc9-141">Ahora tiene un archivo que contiene la imagen de [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="20cc9-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="20cc9-142">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="20cc9-142">Complete example</span></span>

<span data-ttu-id="20cc9-143">Aquí se muestra el código completo de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="20cc9-143">Here the full code for this example.</span></span>

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



 

 