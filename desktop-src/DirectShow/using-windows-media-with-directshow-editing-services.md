---
description: Usar Windows Media con los servicios de edición de DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Usar Windows Media con los servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678621"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="79e59-103">Usar Windows Media con los servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="79e59-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="79e59-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="79e59-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="79e59-105">En esta sección se describe cómo usar el contenido basado en Windows Media en una aplicación de [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="79e59-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="79e59-106">Hay dos escenarios principales:</span><span class="sxs-lookup"><span data-stu-id="79e59-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="79e59-107">Clips de origen.</span><span class="sxs-lookup"><span data-stu-id="79e59-107">Source clips.</span></span> <span data-ttu-id="79e59-108">Un proyecto DES puede contener clips de audio y vídeo de archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79e59-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="79e59-109">Formato de destino.</span><span class="sxs-lookup"><span data-stu-id="79e59-109">Target format.</span></span> <span data-ttu-id="79e59-110">Windows Media es un formato ideal para la salida final de un proyecto de edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79e59-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="79e59-111">Para trabajar con archivos de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave.</span><span class="sxs-lookup"><span data-stu-id="79e59-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="79e59-112">Para ello, implementa un objeto de proveedor de claves.</span><span class="sxs-lookup"><span data-stu-id="79e59-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="79e59-113">El proveedor de claves es un objeto COM que expone la interfaz **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="79e59-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="79e59-114">Para obtener información acerca de la implementación del proveedor de claves, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="79e59-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="79e59-115">Para usar DES con archivos de Windows Media, los siguientes objetos DES requieren la clave de software:</span><span class="sxs-lookup"><span data-stu-id="79e59-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="79e59-116">El motor de representación, para la vista previa o la escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="79e59-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="79e59-117">El objeto MediaDet, para obtener fotogramas de vídeo o tipos de medios de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="79e59-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="79e59-118">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="79e59-118">\[!Important\]</span></span>  
    > <span data-ttu-id="79e59-119">No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79e59-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="79e59-120">Use siempre el motor de representación básico (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="79e59-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="79e59-121">Para asignar a un objeto la clave de software, consulte ese objeto para la interfaz **IObjectWithSite** y llame a **IObjectWithSite:: SetSite** con un puntero al proveedor de claves.</span><span class="sxs-lookup"><span data-stu-id="79e59-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="79e59-122">Por ejemplo, el código siguiente proporciona la clave de software al motor de representación:</span><span class="sxs-lookup"><span data-stu-id="79e59-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="79e59-123">Para usar clips de origen de Windows Media en un proyecto DES, basta con llamar a **IObjectWithSite:: SetSite** en el motor de representación con un puntero al proveedor de claves.</span><span class="sxs-lookup"><span data-stu-id="79e59-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="79e59-124">Para obtener información acerca de cómo escribir archivos de Windows Media, consulte [escribir un archivo de Windows Media en des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="79e59-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79e59-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79e59-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e59-126">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="79e59-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



