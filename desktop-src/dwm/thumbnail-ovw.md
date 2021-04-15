---
title: Información general sobre las miniaturas de DWM
description: Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de las ventanas de la aplicación.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Administrador de ventanas de escritorio (DWM), miniaturas
- DWM (Administrador de ventanas de escritorio), miniaturas
- Administrador de ventanas de escritorio (DWM), relaciones en miniatura
- DWM (Administrador de ventanas de escritorio), relaciones en miniatura
- vistas en miniatura
- relaciones en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104569640"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="66eea-109">Información general sobre las miniaturas de DWM</span><span class="sxs-lookup"><span data-stu-id="66eea-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="66eea-110">Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de las ventanas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66eea-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="66eea-111">No son instantáneas estáticas de una ventana, sino que son dinámicas, las conexiones constantes entre una ventana de código fuente en miniatura y una ubicación en una ventana de destino que recibe la representación en miniatura activa.</span><span class="sxs-lookup"><span data-stu-id="66eea-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="66eea-112">Esto permite una vista rápida de las aplicaciones en ejecución si mantiene el puntero sobre la aplicación en la barra de tareas o usa el gesto de tecla ALT-TAB para ver y cambiar rápidamente a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="66eea-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="66eea-113">En la imagen siguiente se muestra la miniatura dinámica de Windows Vista que se muestra al mantener el mouse sobre la aplicación en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="66eea-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Captura de pantalla que muestra la miniatura D W M que se ve al mantener el mouse sobre una aplicación en la barra de tareas.](images/dwm-livethumbnail.png)

<span data-ttu-id="66eea-115">En la imagen siguiente se muestra el volteo de Windows Vista (ALT-TAB) habilitada por DWM.</span><span class="sxs-lookup"><span data-stu-id="66eea-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![captura de pantalla de la pestaña Alt-Tab habilitada para DWM](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="66eea-117">Las miniaturas de DWM no permiten a los desarrolladores crear aplicaciones como la característica Flip3D (WINKEY-TAB) de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="66eea-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="66eea-118">Las miniaturas se representan directamente en la ventana de destino en 2-D.</span><span class="sxs-lookup"><span data-stu-id="66eea-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="66eea-119">Relaciones en miniatura de DWM</span><span class="sxs-lookup"><span data-stu-id="66eea-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="66eea-120">Para mostrar las miniaturas en la aplicación, primero debe establecer una relación entre una ventana de código fuente y una ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="66eea-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="66eea-121">Esto se realiza mediante una llamada a la función [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="66eea-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="66eea-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) no representa una miniatura en la ventana de destino, sino que simplemente crea la relación y proporciona el identificador de miniatura.</span><span class="sxs-lookup"><span data-stu-id="66eea-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="66eea-123">La miniatura se representa una vez que se han establecido las [**\_ \_ propiedades de miniatura de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) y se ha llamado a la función [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="66eea-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="66eea-124">Las llamadas posteriores a **DwmUpdateThumbnailProperties** actualizan la miniatura con un nuevo conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="66eea-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="66eea-125">DWM también proporciona la función auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obtener el tamaño de la ventana de código fuente de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="66eea-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="66eea-126">Para finalizar una relación de miniatura, llame a la función [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="66eea-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="66eea-127">En el ejemplo siguiente se muestra cómo crear un releationship con el escritorio de Windows y mostrarlo en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="66eea-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="66eea-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66eea-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="66eea-129">[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)</span><span class="sxs-lookup"><span data-stu-id="66eea-129">[Desktop Window Manager Overview](dwm-overview.md)</span></span>
</dt> <dt>

[<span data-ttu-id="66eea-130">Habilitar y controlar la composición de DWM</span><span class="sxs-lookup"><span data-stu-id="66eea-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="66eea-131">Consideraciones de rendimiento y prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="66eea-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




