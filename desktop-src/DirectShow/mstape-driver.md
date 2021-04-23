---
description: Controlador MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Controlador MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909403"
---
# <a name="mstape-driver"></a><span data-ttu-id="aaab0-103">Controlador MSTape</span><span class="sxs-lookup"><span data-stu-id="aaab0-103">MSTape Driver</span></span>

<span data-ttu-id="aaab0-104">Este tema se aplica a Windows XP o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aaab0-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="aaab0-105">El controlador MSTape admite dispositivos D-VHS y MPEG.</span><span class="sxs-lookup"><span data-stu-id="aaab0-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="aaab0-106">Se expone a las aplicaciones como filtro [de captura de vídeo de WDM.](wdm-video-capture-filter.md)</span><span class="sxs-lookup"><span data-stu-id="aaab0-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="aaab0-107">Su funcionalidad es similar a la de [MSDV,](msdv-driver.md)el controlador de cámara dv:</span><span class="sxs-lookup"><span data-stu-id="aaab0-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="aaab0-108">Aparece en las categorías de filtro "Orígenes de captura de vídeo" (CLSID VideoInputDeviceCategory) y "Dispositivos de representación de streaming de \_ WDM" (AM \_ KSCATEGORY \_ RENDER).</span><span class="sxs-lookup"><span data-stu-id="aaab0-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="aaab0-109">Una aplicación puede crear una instancia del filtro mediante la [**interfaz ICreateDevEnum.**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)</span><span class="sxs-lookup"><span data-stu-id="aaab0-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="aaab0-110">Tiene un pin de salida para la captura y el transporte desde el dispositivo, y un pin de entrada para el transporte al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="aaab0-111">Solo se puede conectar un pin a la vez.</span><span class="sxs-lookup"><span data-stu-id="aaab0-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="aaab0-112">**Tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="aaab0-112">**Media Types**</span></span>

<span data-ttu-id="aaab0-113">La patilla de entrada admite un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="aaab0-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="aaab0-114">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="aaab0-114">Label</span></span> | <span data-ttu-id="aaab0-115">Value</span><span class="sxs-lookup"><span data-stu-id="aaab0-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="aaab0-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="aaab0-116">Major Type</span></span>   | <span data-ttu-id="aaab0-117">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="aaab0-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="aaab0-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="aaab0-118">Subtype</span></span>      | <span data-ttu-id="aaab0-119">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="aaab0-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="aaab0-120">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="aaab0-120">Sample Size</span></span>  | <span data-ttu-id="aaab0-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="aaab0-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="aaab0-122">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="aaab0-122">Format Block</span></span> | [<span data-ttu-id="aaab0-123">**MPEG2 \_ TRANSPORT \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="aaab0-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="aaab0-124">El pin de salida admite dos tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="aaab0-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="aaab0-125">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="aaab0-125">Label</span></span> | <span data-ttu-id="aaab0-126">Value</span><span class="sxs-lookup"><span data-stu-id="aaab0-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="aaab0-127">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="aaab0-127">Major Type</span></span>   | <span data-ttu-id="aaab0-128">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="aaab0-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="aaab0-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="aaab0-129">Subtype</span></span>      | <span data-ttu-id="aaab0-130">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="aaab0-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="aaab0-131">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="aaab0-131">Sample Size</span></span>  | <span data-ttu-id="aaab0-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="aaab0-132">192 x 256</span></span>                              |
| <span data-ttu-id="aaab0-133">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="aaab0-133">Format Block</span></span> | <span data-ttu-id="aaab0-134">MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="aaab0-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="aaab0-135">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="aaab0-135">Label</span></span> | <span data-ttu-id="aaab0-136">Value</span><span class="sxs-lookup"><span data-stu-id="aaab0-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="aaab0-137">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="aaab0-137">Major Type</span></span>   | <span data-ttu-id="aaab0-138">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="aaab0-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="aaab0-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="aaab0-139">Subtype</span></span>      | <span data-ttu-id="aaab0-140">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="aaab0-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="aaab0-141">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="aaab0-141">Sample Size</span></span>  | <span data-ttu-id="aaab0-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="aaab0-142">188 x 256</span></span>                              |
| <span data-ttu-id="aaab0-143">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="aaab0-143">Format Block</span></span> | <span data-ttu-id="aaab0-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="aaab0-144">**NULL**</span></span>                               |



 

<span data-ttu-id="aaab0-145">**Información del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="aaab0-145">**Device Information**</span></span>

<span data-ttu-id="aaab0-146">El controlador lee dinámicamente información de la ROM de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="aaab0-147">La aplicación puede recuperar esta información enlazando el moniker de dispositivo a un bolsa de propiedades y llamando al **método IPropertyBag::Read.**</span><span class="sxs-lookup"><span data-stu-id="aaab0-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="aaab0-148">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aaab0-148">Property</span></span>            | <span data-ttu-id="aaab0-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaab0-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="aaab0-150">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aaab0-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="aaab0-151">UniqueID \_ Low</span><span class="sxs-lookup"><span data-stu-id="aaab0-151">UniqueID\_Low</span></span>       | <span data-ttu-id="aaab0-152">Identificador único del dispositivo **(DWORD bajo).**</span><span class="sxs-lookup"><span data-stu-id="aaab0-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="aaab0-153">**long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="aaab0-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="aaab0-154">UniqueID \_ High</span><span class="sxs-lookup"><span data-stu-id="aaab0-154">UniqueID\_High</span></span>      | <span data-ttu-id="aaab0-155">Identificador único del dispositivo **(DWORD alto)**</span><span class="sxs-lookup"><span data-stu-id="aaab0-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="aaab0-156">**long**</span><span class="sxs-lookup"><span data-stu-id="aaab0-156">**long**</span></span>            |
| <span data-ttu-id="aaab0-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="aaab0-157">VendorID</span></span>            | <span data-ttu-id="aaab0-158">Id. de proveedor.</span><span class="sxs-lookup"><span data-stu-id="aaab0-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="aaab0-159">**long**</span><span class="sxs-lookup"><span data-stu-id="aaab0-159">**long**</span></span>            |
| <span data-ttu-id="aaab0-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="aaab0-160">ModelID</span></span>             | <span data-ttu-id="aaab0-161">Identificador del modelo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="aaab0-162">**long**</span><span class="sxs-lookup"><span data-stu-id="aaab0-162">**long**</span></span>            |
| <span data-ttu-id="aaab0-163">VendorText</span><span class="sxs-lookup"><span data-stu-id="aaab0-163">VendorText</span></span>          | <span data-ttu-id="aaab0-164">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="aaab0-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="aaab0-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="aaab0-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="aaab0-166">ModelText</span><span class="sxs-lookup"><span data-stu-id="aaab0-166">ModelText</span></span>           | <span data-ttu-id="aaab0-167">Nombre del modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="aaab0-168">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="aaab0-168">**BSTR**</span></span>            |
| <span data-ttu-id="aaab0-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="aaab0-169">UnitModelText</span></span>       | <span data-ttu-id="aaab0-170">Nombre del modelo de unidad; puede ser igual que ModelText.</span><span class="sxs-lookup"><span data-stu-id="aaab0-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="aaab0-171">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="aaab0-171">**BSTR**</span></span>            |
| <span data-ttu-id="aaab0-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="aaab0-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="aaab0-173">Carga útil de oPCR (Output Plug Control).</span><span class="sxs-lookup"><span data-stu-id="aaab0-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="aaab0-174">Ejemplo: 146 cuádlets.</span><span class="sxs-lookup"><span data-stu-id="aaab0-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="aaab0-175">**long**</span><span class="sxs-lookup"><span data-stu-id="aaab0-175">**long**</span></span>            |
| <span data-ttu-id="aaab0-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="aaab0-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="aaab0-177">Velocidad de datos de oPCR.</span><span class="sxs-lookup"><span data-stu-id="aaab0-177">oPCR data rate.</span></span> <span data-ttu-id="aaab0-178">Ejemplos: 0 (S100), 1 (S200) o 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="aaab0-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="aaab0-179">**long**</span><span class="sxs-lookup"><span data-stu-id="aaab0-179">**long**</span></span>            |
| <span data-ttu-id="aaab0-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="aaab0-180">DeviceClassGUID</span></span>     | <span data-ttu-id="aaab0-181">GUID que identifica el controlador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="aaab0-182">Para MSTape, este valor es `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="aaab0-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="aaab0-183">Este GUID se define como MSTapeDeviceGUID en el archivo de encabezado Xprtdefs.h.</span><span class="sxs-lookup"><span data-stu-id="aaab0-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="aaab0-184">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="aaab0-184">**BSTR**</span></span>            |
| <span data-ttu-id="aaab0-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaab0-185">Description</span></span>         | <span data-ttu-id="aaab0-186">Descripción del dispositivo, tomada del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="aaab0-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="aaab0-187">Esta cadena normalmente contiene el nombre de marca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaab0-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="aaab0-188">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="aaab0-188">**BSTR**</span></span>            |



 

<span data-ttu-id="aaab0-189">El identificador de dispositivo es un entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aaab0-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="aaab0-190">El **DWORD bajo se** almacena en la propiedad UniqueID Low y el DWORD alto se almacena \_ en la propiedad UniqueID  \_ High.</span><span class="sxs-lookup"><span data-stu-id="aaab0-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="aaab0-191">Para obtener más información sobre los monikers de dispositivo, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="aaab0-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaab0-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aaab0-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaab0-193">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="aaab0-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="aaab0-194">Control de una cámara dv</span><span class="sxs-lookup"><span data-stu-id="aaab0-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



