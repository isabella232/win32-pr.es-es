---
description: A partir de Windows Vista, se usa un mayor uso de imágenes en miniatura específicas del archivo que en versiones anteriores de Windows.
title: Crear controladores de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984355"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="6c5c8-103">Crear controladores de miniaturas</span><span class="sxs-lookup"><span data-stu-id="6c5c8-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="6c5c8-104">A partir de Windows Vista, se usa un mayor uso de imágenes en miniatura específicas del archivo que en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="6c5c8-105">Se usan en todas las vistas, en los cuadros de diálogo y para cualquier tipo de archivo que las proporcione.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="6c5c8-106">También se ha cambiado la presentación en miniatura.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="6c5c8-107">Hay disponible un espectro continuo de tamaños seleccionables por el usuario en lugar de los tamaños discretos, como iconos y miniaturas.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="6c5c8-108">La interfaz [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) facilita una miniatura más sencilla que la anterior [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) o [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span><span class="sxs-lookup"><span data-stu-id="6c5c8-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="6c5c8-109">Sin embargo, tenga en cuenta que el código existente que usa **IExtractImage** o **IExtractImage2** sigue siendo válido y es compatible.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="6c5c8-110">El ejemplo RecipeThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="6c5c8-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="6c5c8-111">El ejemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) que se disecciona en esta sección se incluye en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6c5c8-112">La ubicación de instalación predeterminada es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="6c5c8-113">Sin embargo, la mayor parte del código también se incluye aquí.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="6c5c8-114">En el ejemplo [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) se muestra la implementación de un controlador de miniaturas para un nuevo tipo de archivo registrado con una extensión. Recipe.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="6c5c8-115">En el ejemplo se muestra el uso de las distintas API de controlador de miniaturas para registrar los servidores del modelo de objetos componentes (COM) de extracción en miniatura para tipos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="6c5c8-116">Este tema le guía a través del código de ejemplo, resaltando las opciones de codificación y las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="6c5c8-117">Un controlador de miniaturas siempre debe implementar [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) junto con una de estas interfaces:</span><span class="sxs-lookup"><span data-stu-id="6c5c8-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="6c5c8-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="6c5c8-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="6c5c8-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="6c5c8-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="6c5c8-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="6c5c8-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="6c5c8-121">Hay casos en los que no es posible la inicialización con secuencias.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="6c5c8-122">En escenarios en los que el controlador de miniaturas no implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), debe dejar de ejecutarse en el proceso aislado, donde el indexador del sistema lo coloca de forma predeterminada cuando se produce un cambio en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="6c5c8-123">Para no participar en la característica de aislamiento de procesos, establezca el siguiente valor del registro.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="6c5c8-124">Si implementa [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) y realiza una inicialización basada en secuencias, el controlador es más seguro y confiable.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="6c5c8-125">Normalmente, deshabilitar el aislamiento de procesos solo está pensado para los controladores heredados; Evite deshabilitar esta característica para cualquier código nuevo.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="6c5c8-126">**IInitializeWithStream** debe ser la primera opción de la interfaz de inicialización siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="6c5c8-127">Dado que el archivo de imagen en el ejemplo no está incrustado en el archivo. receta y no forma parte de su secuencia de archivos, se usa [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="6c5c8-128">La implementación del método [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) simplemente pasa sus parámetros a las variables de clase privada.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="6c5c8-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) tiene solo un método,[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail), al que se llama con el mayor tamaño deseado de la imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="6c5c8-130">Aunque el parámetro se denomina *CX*, su valor se utiliza como el tamaño máximo de las dimensiones x e y de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="6c5c8-131">Si la miniatura recuperada no es cuadrada, el eje más largo está limitado por *CX* y se conserva la relación de aspecto de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="6c5c8-132">Cuando devuelve, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) proporciona un identificador a la imagen recuperada.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="6c5c8-133">También proporciona un valor que indica el formato de color de la imagen y si tiene información alfa válida.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="6c5c8-134">La implementación de GetThumbnail en el ejemplo comienza con una llamada al método privado **\_ GetBase64EncodedImageString** .</span><span class="sxs-lookup"><span data-stu-id="6c5c8-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="6c5c8-135">El tipo de archivo. Recipe es simplemente un archivo XML registrado como una extensión de nombre de archivo única.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="6c5c8-136">Incluye un elemento denominado **imagen** que proporciona la ruta de acceso relativa y el nombre de archivo de la imagen que se va a usar como miniatura para este archivo. receta determinado.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="6c5c8-137">El elemento de **imagen** está formado por el atributo de **origen** que especifica una imagen codificada en base 64 y un atributo de **tamaño** opcional.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="6c5c8-138">**El tamaño** tiene dos valores: pequeño y grande.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="6c5c8-139">Esto le permite proporcionar varios nodos de **imagen** con imágenes independientes.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="6c5c8-140">La imagen recuperada depende del valor de tamaño máximo (*CX*) proporcionado en la llamada a [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span><span class="sxs-lookup"><span data-stu-id="6c5c8-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="6c5c8-141">Dado que Windows nunca cambia el tamaño de la imagen a un tamaño mayor que el tamaño máximo, se pueden proporcionar diferentes imágenes para diferentes resoluciones.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="6c5c8-142">Sin embargo, para simplificar, el ejemplo omite el atributo de **tamaño** y proporciona una sola imagen para todas las situaciones.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="6c5c8-143">El método **\_ GetBase64EncodedImageString** , cuya implementación se muestra aquí, usa las API de Document Object Model XML (dom) para recuperar el nodo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="6c5c8-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="6c5c8-144">Desde ese nodo, extrae la imagen de los datos del atributo de **origen** .</span><span class="sxs-lookup"><span data-stu-id="6c5c8-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="6c5c8-145">A continuación, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) pasa la cadena recuperada a **\_ GetStreamFromString**.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="6c5c8-146">El método **\_ GetStreamFromString** , cuya implementación se muestra aquí, que convierte la imagen codificada en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="6c5c8-147">A continuación, **GetThumbnail** usa las API de Windows Imaging Component (WIC) para extraer un mapa de bits de la secuencia y obtener un identificador para dicho mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="6c5c8-148">La información alfa está establecida, WIC está correctamente cerrado y el método finaliza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6c5c8-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c5c8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c5c8-150">Controladores en miniatura</span><span class="sxs-lookup"><span data-stu-id="6c5c8-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="6c5c8-151">Instrucciones de controlador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="6c5c8-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="6c5c8-152">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="6c5c8-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
