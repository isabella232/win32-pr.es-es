---
description: Windows Vista hace un mayor uso de las imágenes en miniatura específicas del archivo que las versiones anteriores de Windows.
title: Controladores en miniatura
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278491"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="1c6c7-103">Controladores en miniatura</span><span class="sxs-lookup"><span data-stu-id="1c6c7-103">Thumbnail Handlers</span></span>

<span data-ttu-id="1c6c7-104">Windows Vista hace un mayor uso de las imágenes en miniatura específicas del archivo que las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="1c6c7-105">Windows Vista los utiliza en todas las vistas, en los cuadros de diálogo y en cualquier tipo de archivo que las proporcione.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="1c6c7-106">Otras aplicaciones también pueden usar su miniatura.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="1c6c7-107">También se ha cambiado la presentación en miniatura.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="1c6c7-108">Ahora, hay disponible un espectro continuo de tamaños seleccionables por el usuario en lugar de los tamaños discretos, como los iconos y las miniaturas que se proporcionan en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="1c6c7-109">Podría oír estas miniaturas denominadas iconos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="1c6c7-110">En la interfaz de usuario de Windows Vista, a menudo se usan vistas en miniatura de la resolución de 32 bits y tan grandes como 256x256 píxeles.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="1c6c7-111">Los propietarios de formato de archivo deben estar preparados para mostrar sus miniaturas en ese tamaño.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="1c6c7-112">También deben proporcionar imágenes no estáticas para las miniaturas que reflejan el contenido de un archivo concreto.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="1c6c7-113">Por ejemplo, la miniatura de un archivo de texto debería mostrar una versión en miniatura del documento, incluido el texto.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="1c6c7-114">La interfaz [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) se ha introducido para proporcionar una miniatura más sencilla y más sencilla que en el pasado, cuando se habría usado [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="1c6c7-115">Tenga en cuenta que el código existente que usa **IExtractImage** sigue siendo válido en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="1c6c7-116">Sin embargo, **IExtractImage** no se admite en el panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="1c6c7-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="1c6c7-117">Este tema trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="1c6c7-118">Procesos en miniatura</span><span class="sxs-lookup"><span data-stu-id="1c6c7-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="1c6c7-119">Caché y tamaño de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="1c6c7-120">Superposiciones en miniatura</span><span class="sxs-lookup"><span data-stu-id="1c6c7-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="1c6c7-121">Elementos gráficos de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="1c6c7-122">Registrar el controlador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="1c6c7-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c6c7-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="1c6c7-124">Procesos en miniatura</span><span class="sxs-lookup"><span data-stu-id="1c6c7-124">Thumbnail Processes</span></span>

<span data-ttu-id="1c6c7-125">Los controladores, incluidos los controladores de miniaturas, se ejecutan de forma predeterminada en un proceso independiente.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="1c6c7-126">Puede forzar que el controlador se ejecute en proceso pasando un valor **null** como contexto de enlace en una llamada a [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="1c6c7-127">También puede optar por no quedarse fuera de proceso de forma predeterminada estableciendo la entrada DisableProcessIsolation en el registro tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="1c6c7-128">El identificador de clase (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} es el CLSID para las implementaciones de [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .</span><span class="sxs-lookup"><span data-stu-id="1c6c7-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="1c6c7-129">Caché y tamaño de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="1c6c7-130">Cuando se necesita una miniatura, Windows comprueba primero la caché en miniatura de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="1c6c7-131">Se llama al extractor de miniaturas si la imagen no se encuentra en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="1c6c7-132">También se llama cuando la hora de la última modificación de la imagen es posterior a la de la copia de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="1c6c7-133">Las imágenes en miniatura de esta caché se almacenan en un conjunto de tamaños discretos.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="1c6c7-134">Todos los tamaños se proporcionan en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="1c6c7-135">32x32</span><span class="sxs-lookup"><span data-stu-id="1c6c7-135">32x32</span></span>
-   <span data-ttu-id="1c6c7-136">96x96</span><span class="sxs-lookup"><span data-stu-id="1c6c7-136">96x96</span></span>
-   <span data-ttu-id="1c6c7-137">256x256</span><span class="sxs-lookup"><span data-stu-id="1c6c7-137">256x256</span></span>
-   <span data-ttu-id="1c6c7-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="1c6c7-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="1c6c7-139">Estos valores están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-139">These values are subject to change.</span></span> <span data-ttu-id="1c6c7-140">El código no debe suponer que siempre se usará un tamaño determinado.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="1c6c7-141">Si una imagen no es cuadrada, no debe rellenarla.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="1c6c7-142">Windows es responsable de respetar la relación de aspecto original y de rellenar la imagen con un tamaño cuadrado.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="1c6c7-143">Cuando se solicita una imagen de un tamaño determinado, a menos que se encuentre una coincidencia exacta, Windows Vista siempre recupera la siguiente imagen más grande y la escala hasta el tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="1c6c7-144">Una imagen nunca se escala verticalmente en tamaño como era el caso de las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="1c6c7-145">En la tabla siguiente se proporcionan algunos ejemplos de la relación entre el tamaño solicitado y el tamaño disponible.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="1c6c7-146">Tamaño máximo de la imagen que se proporciona</span><span class="sxs-lookup"><span data-stu-id="1c6c7-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="1c6c7-147">Tamaño solicitado por el extractor</span><span class="sxs-lookup"><span data-stu-id="1c6c7-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="1c6c7-148">Proporciona</span><span class="sxs-lookup"><span data-stu-id="1c6c7-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="1c6c7-149">156x120</span><span class="sxs-lookup"><span data-stu-id="1c6c7-149">156x120</span></span>                        | <span data-ttu-id="1c6c7-150">256x256</span><span class="sxs-lookup"><span data-stu-id="1c6c7-150">256x256</span></span>                         | <span data-ttu-id="1c6c7-151">156x120 (no rellenar, mantener relación de aspecto)</span><span class="sxs-lookup"><span data-stu-id="1c6c7-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="1c6c7-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="1c6c7-152">2048x1024</span></span>                      | <span data-ttu-id="1c6c7-153">256x256</span><span class="sxs-lookup"><span data-stu-id="1c6c7-153">256x256</span></span>                         | <span data-ttu-id="1c6c7-154">256x128 (no rellenar, mantener relación de aspecto)</span><span class="sxs-lookup"><span data-stu-id="1c6c7-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="1c6c7-155">Puede declarar un punto de corte como parte de la entrada de ID. de programa de la aplicación asociada en el registro.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="1c6c7-156">Por debajo de este tamaño, no se usan vistas en miniatura.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="1c6c7-157">La entrada ThumbnailCutoff es uno de estos valores de REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="1c6c7-158">Value</span><span class="sxs-lookup"><span data-stu-id="1c6c7-158">Value</span></span> | <span data-ttu-id="1c6c7-159">Límite</span><span class="sxs-lookup"><span data-stu-id="1c6c7-159">Cutoff</span></span> | <span data-ttu-id="1c6c7-160">HighDPI sensible</span><span class="sxs-lookup"><span data-stu-id="1c6c7-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="1c6c7-161">0</span><span class="sxs-lookup"><span data-stu-id="1c6c7-161">0</span></span>     | <span data-ttu-id="1c6c7-162">32x32</span><span class="sxs-lookup"><span data-stu-id="1c6c7-162">32x32</span></span>  | <span data-ttu-id="1c6c7-163">Sí</span><span class="sxs-lookup"><span data-stu-id="1c6c7-163">Yes</span></span>               |
| <span data-ttu-id="1c6c7-164">1</span><span class="sxs-lookup"><span data-stu-id="1c6c7-164">1</span></span>     | <span data-ttu-id="1c6c7-165">16x16</span><span class="sxs-lookup"><span data-stu-id="1c6c7-165">16x16</span></span>  | <span data-ttu-id="1c6c7-166">Sí</span><span class="sxs-lookup"><span data-stu-id="1c6c7-166">Yes</span></span>               |
| <span data-ttu-id="1c6c7-167">2</span><span class="sxs-lookup"><span data-stu-id="1c6c7-167">2</span></span>     | <span data-ttu-id="1c6c7-168">48x48</span><span class="sxs-lookup"><span data-stu-id="1c6c7-168">48x48</span></span>  | <span data-ttu-id="1c6c7-169">Sí</span><span class="sxs-lookup"><span data-stu-id="1c6c7-169">Yes</span></span>               |
| <span data-ttu-id="1c6c7-170">3</span><span class="sxs-lookup"><span data-stu-id="1c6c7-170">3</span></span>     | <span data-ttu-id="1c6c7-171">16x16</span><span class="sxs-lookup"><span data-stu-id="1c6c7-171">16x16</span></span>  | <span data-ttu-id="1c6c7-172">Sí</span><span class="sxs-lookup"><span data-stu-id="1c6c7-172">Yes</span></span>               |


<span data-ttu-id="1c6c7-173">La distinción de puntos por pulgada (PPP) de alto significa que las dimensiones de píxeles de la miniatura se ajustan automáticamente para un mayor tamaño de PPP.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="1c6c7-174">Por ejemplo, una imagen de 32 x 96 PPP sería una imagen 40 x 40 a 120 ppp.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="1c6c7-175">Si no se especifica la entrada ThumbnailCutoff, el límite predeterminado es 20x20 (no sensible a PPP).</span><span class="sxs-lookup"><span data-stu-id="1c6c7-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="1c6c7-176">Superposiciones en miniatura</span><span class="sxs-lookup"><span data-stu-id="1c6c7-176">Thumbnail Overlays</span></span>

<span data-ttu-id="1c6c7-177">Las superposiciones en miniatura, una pequeña imagen que se muestra en la esquina inferior derecha de la miniatura, proporcionan una oportunidad para que los desarrolladores apliquen la identificación de la marca a sus miniaturas.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="1c6c7-178">Las superposiciones se declaran en el registro como parte de la entrada del identificador de programa de la aplicación asociada, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="1c6c7-179">La entrada TypeOverlay contiene un valor de REG \_ SZ interpretado de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="1c6c7-180">Si el valor es una referencia de recursos (un archivo **. ico** incrustado en el archivo dll) como `ISVComponent.dll,-155` , esa imagen se utiliza como la superposición de los archivos con esa extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="1c6c7-181">Tenga en cuenta que en este ejemplo, **155** es el identificador de recurso y, si el archivo dll no está presente en una ruta de acceso estándar (como **C:/Windows/system32**), se requiere la ruta de acceso completa en lugar de solo el nombre del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="1c6c7-182">Si el valor es una cadena vacía, no se aplica ninguna superposición a la imagen.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="1c6c7-183">Si el valor no está presente, se usa el icono predeterminado de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="1c6c7-184">Las superposiciones de las miniaturas solo deben proporcionarse a través de este mecanismo y se pueden aplicar mediante Windows.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="1c6c7-185">No aplique las superposiciones por su cuenta.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="1c6c7-186">Elementos gráficos de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-186">Thumbnail Adornments</span></span>

<span data-ttu-id="1c6c7-187">Los elementos gráficos como las sombras paralelas se aplican a las miniaturas en función del tema seleccionado actualmente por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="1c6c7-188">Windows proporciona elementos gráficos; no las cree.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="1c6c7-189">Windows podría cambiar la apariencia de los elementos gráficos concretos en cualquier momento, por lo que si usted le proporcionó el riesgo, podría quedar fuera de la sincronización con el sistema.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="1c6c7-190">Es posible que las miniaturas se desplacen por la fecha o la ubicación.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="1c6c7-191">Los posibles elementos gráficos se declaran en el registro como parte de la entrada del identificador de programa de la aplicación asociada, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="1c6c7-192">La entrada de tratamiento contiene uno de estos \_ valores de REG DWORD:</span><span class="sxs-lookup"><span data-stu-id="1c6c7-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="1c6c7-193">Value</span><span class="sxs-lookup"><span data-stu-id="1c6c7-193">Value</span></span> | <span data-ttu-id="1c6c7-194">Significado</span><span class="sxs-lookup"><span data-stu-id="1c6c7-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="1c6c7-195">0</span><span class="sxs-lookup"><span data-stu-id="1c6c7-195">0</span></span>     | <span data-ttu-id="1c6c7-196">Sin elemento gráfico</span><span class="sxs-lookup"><span data-stu-id="1c6c7-196">No Adornment</span></span>    |
| <span data-ttu-id="1c6c7-197">1</span><span class="sxs-lookup"><span data-stu-id="1c6c7-197">1</span></span>     | <span data-ttu-id="1c6c7-198">Sombra paralela</span><span class="sxs-lookup"><span data-stu-id="1c6c7-198">Drop Shadow</span></span>     |
| <span data-ttu-id="1c6c7-199">2</span><span class="sxs-lookup"><span data-stu-id="1c6c7-199">2</span></span>     | <span data-ttu-id="1c6c7-200">Borde fotográfico</span><span class="sxs-lookup"><span data-stu-id="1c6c7-200">Photo Border</span></span>    |
| <span data-ttu-id="1c6c7-201">3</span><span class="sxs-lookup"><span data-stu-id="1c6c7-201">3</span></span>     | <span data-ttu-id="1c6c7-202">Engranajes de vídeo</span><span class="sxs-lookup"><span data-stu-id="1c6c7-202">Video Sprockets</span></span> |


<span data-ttu-id="1c6c7-203">De forma predeterminada, se aplica una sombra paralela a las imágenes.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="1c6c7-204">Registrar el controlador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="1c6c7-205">El registro de un controlador de miniaturas se basa en las asociaciones de archivo estándar.</span><span class="sxs-lookup"><span data-stu-id="1c6c7-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="1c6c7-206">El GUID de la extensión de Shell del controlador de miniaturas es `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="1c6c7-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c6c7-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c6c7-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6c7-208">**IThumbnailProvider**</span><span class="sxs-lookup"><span data-stu-id="1c6c7-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="1c6c7-209">Crear controladores de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="1c6c7-210">Instrucciones de controlador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1c6c7-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



