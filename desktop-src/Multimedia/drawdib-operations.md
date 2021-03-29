---
title: Operaciones de DrawDib
description: Operaciones de DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, acerca de
- DrawDib, acceso
- DrawDib, abrir
- DrawDib, operaciones
- DrawDib, contexto de dispositivo (DC)
- DC (contexto de dispositivo)
- DrawDibOpen función)
- DrawDibClose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487038"
---
# <a name="drawdib-operations"></a><span data-ttu-id="2fbf3-111">Operaciones de DrawDib</span><span class="sxs-lookup"><span data-stu-id="2fbf3-111">DrawDib Operations</span></span>

<span data-ttu-id="2fbf3-112">Puede tener acceso a todo el grupo de funciones de DrawDib mediante la función [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) .</span><span class="sxs-lookup"><span data-stu-id="2fbf3-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="2fbf3-113">Esta función carga la biblioteca de vínculos dinámicos (DLL), asigna recursos de memoria, crea un contexto de dispositivo DrawDib (DC) y mantiene un recuento de referencias del número de controladores de dominio que se inicializan.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="2fbf3-114">**DrawDibOpen** también devuelve un identificador del nuevo controlador de dominio que se usa con las otras funciones de DrawDib.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="2fbf3-115">Puede liberar un controlador de dominio de DrawDib cuando termine de usarlo mediante la función [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) .</span><span class="sxs-lookup"><span data-stu-id="2fbf3-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="2fbf3-116">**DrawDibClose** también reduce el recuento de referencias de las aplicaciones que tienen acceso a la dll.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="2fbf3-117">La llamada a **DrawDibClose** debe ser la última función DrawDib de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="2fbf3-118">Puede crear tantos controladores de usuario de DrawDib como desee.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="2fbf3-119">Puede usar varios controladores de usuario de DrawDib para dibujar varios mapas de bits simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="2fbf3-120">También puede crear varios controladores de dominio de DrawDib, cada uno con características únicas, de modo que la aplicación pueda elegir y usar el controlador de dominio con la configuración más adecuada.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="2fbf3-121">Por ejemplo, puede crear dos controladores de DrawDib en una aplicación: uno que muestre una imagen en su resolución normal y otro que muestre una parte ampliada de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="2fbf3-122">Para ejecutarse de forma eficaz, las funciones de DrawDib requieren información sobre el adaptador de pantalla y su controlador.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="2fbf3-123">El perfil de visualización se obtiene ejecutando una serie de pruebas en el adaptador de pantalla la primera vez que se tiene acceso a la DLL que contiene las funciones de DrawDib.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="2fbf3-124">Las funciones DrawDib usan esta información para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="2fbf3-125">Puede repetir estas pruebas cuando sea necesario mediante la función [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .</span><span class="sxs-lookup"><span data-stu-id="2fbf3-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="2fbf3-126">Recuperar y almacenar el perfil de visualización suele ser una sola vez.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="2fbf3-127">No obstante, si se elimina la información de perfil u otro controlador de pantalla está instalado en el sistema, DrawDib vuelve a ejecutar las pruebas.</span><span class="sxs-lookup"><span data-stu-id="2fbf3-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2fbf3-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fbf3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fbf3-129">Acerca de las funciones de DrawDib</span><span class="sxs-lookup"><span data-stu-id="2fbf3-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




