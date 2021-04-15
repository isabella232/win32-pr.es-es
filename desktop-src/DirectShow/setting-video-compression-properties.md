---
description: Establecer propiedades de compresión de vídeo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Establecer propiedades de compresión de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422940"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="c7df3-103">Establecer propiedades de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="c7df3-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="c7df3-104">Los filtros de compresión de vídeo pueden admitir la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) en sus clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="c7df3-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="c7df3-105">Use esta interfaz para establecer propiedades de compresión, como la velocidad de fotogramas clave, el número de fotogramas predichos (P) por fotograma clave y la calidad de compresión relativa.</span><span class="sxs-lookup"><span data-stu-id="c7df3-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="c7df3-106">En primer lugar, llame al método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para buscar el PIN de salida del filtro y consulte el PIN de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c7df3-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="c7df3-107">Es posible que algunos filtros no admitan la interfaz en absoluto.</span><span class="sxs-lookup"><span data-stu-id="c7df3-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="c7df3-108">Otros pueden exponer la interfaz pero no admiten todas las propiedades de compresión.</span><span class="sxs-lookup"><span data-stu-id="c7df3-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="c7df3-109">Para determinar qué propiedades se admiten, llame a [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="c7df3-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="c7df3-110">Este método devuelve varios datos:</span><span class="sxs-lookup"><span data-stu-id="c7df3-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="c7df3-111">Un conjunto de marcas de funcionalidades</span><span class="sxs-lookup"><span data-stu-id="c7df3-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="c7df3-112">Una cadena descriptiva y una cadena de número de versión</span><span class="sxs-lookup"><span data-stu-id="c7df3-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="c7df3-113">Valores predeterminados para la velocidad de fotogramas clave, la velocidad de fotogramas P y la calidad (si se admiten)</span><span class="sxs-lookup"><span data-stu-id="c7df3-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="c7df3-114">El método tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="c7df3-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="c7df3-115">Los parámetros *pszVersion* y *pszDesc* son búferes de caracteres anchos que reciben la cadena de versión y la cadena de descripción.</span><span class="sxs-lookup"><span data-stu-id="c7df3-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="c7df3-116">Los parámetros *cbVersion* y *cbDesc* reciben los tamaños de búfer necesarios en bytes (no en caracteres).</span><span class="sxs-lookup"><span data-stu-id="c7df3-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="c7df3-117">Los parámetros *lKeyFrame*, *lPFrame* y *dblQuality* reciben los valores predeterminados para la velocidad de fotogramas clave, la velocidad de fotogramas P y la calidad.</span><span class="sxs-lookup"><span data-stu-id="c7df3-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="c7df3-118">La calidad se expresa como un número de punto flotante de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c7df3-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="c7df3-119">El parámetro *lCap* recibe **una operación OR bit a bit** de las marcas de funciones, definidas por el tipo enumerado [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .</span><span class="sxs-lookup"><span data-stu-id="c7df3-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="c7df3-120">Cualquiera de estos parámetros puede ser **null**, en cuyo caso el método omite ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="c7df3-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="c7df3-121">Por ejemplo, para asignar búferes para las cadenas de versión y descripción, primero llame al método con **null** en el primer y tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="c7df3-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="c7df3-122">Use los valores devueltos para *cbVersion* y *cbDesc* para asignar los búferes y, a continuación, vuelva a llamar al método:</span><span class="sxs-lookup"><span data-stu-id="c7df3-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="c7df3-123">El valor de *lCap* indica cuál de los otros métodos **IAMVideoCompression** admite el filtro.</span><span class="sxs-lookup"><span data-stu-id="c7df3-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="c7df3-124">Por ejemplo, si *lCap* contiene la \_ marca CompressionCaps CanKeyFrame, puede llamar a [**IAMVideoCompression:: get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) para obtener la velocidad de fotogramas clave y [**IAMVideoCompression::p UT \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) para establecer la velocidad de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="c7df3-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="c7df3-125">Un valor negativo indica que el filtro utilizará el valor predeterminado, tal y como se obtiene de [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="c7df3-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="c7df3-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c7df3-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="c7df3-127">En el ejemplo de código siguiente se intenta encontrar la interfaz **IAMVideoCompression** en el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="c7df3-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="c7df3-128">Si se realiza correctamente, recupera los valores predeterminados y reales de las propiedades de compresión:</span><span class="sxs-lookup"><span data-stu-id="c7df3-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="c7df3-129">Si usa la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para compilar el gráfico, puede obtener la interfaz **IAMVideoCompression** llamando a [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), en lugar de usar **IBaseFilter:: EnumPins**.</span><span class="sxs-lookup"><span data-stu-id="c7df3-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="c7df3-130">El método **FindInterface** es un método auxiliar que busca filtros y PIN en el gráfico para una interfaz especificada.</span><span class="sxs-lookup"><span data-stu-id="c7df3-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



