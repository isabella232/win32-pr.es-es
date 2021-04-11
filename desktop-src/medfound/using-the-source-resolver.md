---
description: Usar el solucionador de origen
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Usar el solucionador de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276213"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="9d86e-103">Usar el solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="9d86e-103">Using the Source Resolver</span></span>

<span data-ttu-id="9d86e-104">La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión.</span><span class="sxs-lookup"><span data-stu-id="9d86e-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="9d86e-105">Para crear el solucionador de origen, llame a [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span><span class="sxs-lookup"><span data-stu-id="9d86e-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="9d86e-106">Esta función devuelve un puntero de la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="9d86e-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="9d86e-107">La resolución de origen tiene métodos sincrónicos y asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="9d86e-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="9d86e-108">Si usa la resolución de origen desde el subproceso de la aplicación principal, los métodos asincrónicos harán que la interfaz de usuario tenga mayor capacidad de respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d86e-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="9d86e-109">Los métodos sincrónicos pueden bloquearse durante un período de tiempo notable, especialmente si el solucionador de origen debe abrir un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="9d86e-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="9d86e-110">Los métodos sincrónicos son:</span><span class="sxs-lookup"><span data-stu-id="9d86e-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="9d86e-111">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="9d86e-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="9d86e-112">**IMFSourceResolver::CreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="9d86e-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="9d86e-113">Los métodos asincrónicos son:</span><span class="sxs-lookup"><span data-stu-id="9d86e-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="9d86e-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="9d86e-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="9d86e-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="9d86e-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="9d86e-116">Para los métodos asincrónicos, cada método tiene un método **End...** correspondiente para completar la solicitud asincrónica y un método **Cancel...** para cancelar una solicitud pendiente.</span><span class="sxs-lookup"><span data-stu-id="9d86e-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="9d86e-117">Para obtener más información sobre los métodos asincrónicos en Media Foundation, vea [métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9d86e-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="9d86e-118">En el ejemplo de código siguiente se crea un origen multimedia a partir de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9d86e-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="9d86e-119">En este ejemplo se usa el método sincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d86e-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9d86e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d86e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d86e-121">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="9d86e-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



