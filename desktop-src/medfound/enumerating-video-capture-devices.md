---
description: En este tema se describe cómo enumerar los dispositivos de captura de vídeo en el sistema de usuarios y cómo crear una instancia de un dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumerar dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423539"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="71f90-103">Enumerar dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="71f90-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="71f90-104">En este tema se describe cómo enumerar los dispositivos de captura de vídeo en el sistema del usuario y cómo crear una instancia de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71f90-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="71f90-105">Para enumerar los dispositivos de captura de vídeo en el sistema, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="71f90-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="71f90-106">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="71f90-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="71f90-107">Esta función recibe un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="71f90-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="71f90-108">Llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) para establecer el atributo de tipo de origen del [ \_ \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) .</span><span class="sxs-lookup"><span data-stu-id="71f90-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="71f90-109">Establezca el valor del atributo en **MF \_ DEVSOURCE tipo de origen de atributo de \_ \_ \_ \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="71f90-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="71f90-110">Llame a [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span><span class="sxs-lookup"><span data-stu-id="71f90-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="71f90-111">Esta función recibe una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) y el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="71f90-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="71f90-112">Cada puntero representa un dispositivo de captura de vídeo distinto.</span><span class="sxs-lookup"><span data-stu-id="71f90-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="71f90-113">Para crear una instancia de un dispositivo de captura:</span><span class="sxs-lookup"><span data-stu-id="71f90-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="71f90-114">Llame a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para obtener un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="71f90-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="71f90-115">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="71f90-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="71f90-116">Después de crear el origen de medios, libere los punteros de interfaz y libere la memoria de la matriz:</span><span class="sxs-lookup"><span data-stu-id="71f90-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="71f90-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71f90-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f90-118">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="71f90-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



