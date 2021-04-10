---
description: Controlador MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Controlador MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906335"
---
# <a name="mstape-driver"></a><span data-ttu-id="9f7d3-103">Controlador MSTape</span><span class="sxs-lookup"><span data-stu-id="9f7d3-103">MSTape Driver</span></span>

<span data-ttu-id="9f7d3-104">Este tema se aplica a Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="9f7d3-105">El controlador MSTape admite dispositivos de vídeo D-VHS y MPEG camcorder.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="9f7d3-106">Se expone a las aplicaciones como el filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9f7d3-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="9f7d3-107">Su funcionalidad es similar a la de [MSDV](msdv-driver.md), el controlador de videocámara DV:</span><span class="sxs-lookup"><span data-stu-id="9f7d3-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="9f7d3-108">Aparece en las categorías de filtro "orígenes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) y "dispositivos de representación de transmisión por secuencias WDM" ( \_ KSCATEGORY \_ representar).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="9f7d3-109">Una aplicación puede crear una instancia del filtro mediante la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="9f7d3-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="9f7d3-110">Tiene un PIN de salida para la captura y el transporte desde el dispositivo y un PIN de entrada para el transporte al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="9f7d3-111">Solo se puede conectar un PIN a la vez.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="9f7d3-112">**Tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-112">**Media Types**</span></span>

<span data-ttu-id="9f7d3-113">El PIN de entrada admite un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="9f7d3-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="9f7d3-114">Major Type</span></span>   | <span data-ttu-id="9f7d3-115">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9f7d3-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="9f7d3-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="9f7d3-116">Subtype</span></span>      | <span data-ttu-id="9f7d3-117">\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="9f7d3-118">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="9f7d3-118">Sample Size</span></span>  | <span data-ttu-id="9f7d3-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="9f7d3-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="9f7d3-120">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="9f7d3-120">Format Block</span></span> | [<span data-ttu-id="9f7d3-121">**\_Intervalo de transporte de MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="9f7d3-122">El PIN de salida admite dos tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="9f7d3-123">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="9f7d3-123">Major Type</span></span>   | <span data-ttu-id="9f7d3-124">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9f7d3-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="9f7d3-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="9f7d3-125">Subtype</span></span>      | <span data-ttu-id="9f7d3-126">\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="9f7d3-127">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="9f7d3-127">Sample Size</span></span>  | <span data-ttu-id="9f7d3-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="9f7d3-128">192 x 256</span></span>                              |
| <span data-ttu-id="9f7d3-129">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="9f7d3-129">Format Block</span></span> | <span data-ttu-id="9f7d3-130">\_Intervalo de transporte de MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="9f7d3-131">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="9f7d3-131">Major Type</span></span>   | <span data-ttu-id="9f7d3-132">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9f7d3-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="9f7d3-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="9f7d3-133">Subtype</span></span>      | <span data-ttu-id="9f7d3-134">\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="9f7d3-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="9f7d3-135">Tamaño de muestra</span><span class="sxs-lookup"><span data-stu-id="9f7d3-135">Sample Size</span></span>  | <span data-ttu-id="9f7d3-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="9f7d3-136">188 x 256</span></span>                              |
| <span data-ttu-id="9f7d3-137">Bloque de formato</span><span class="sxs-lookup"><span data-stu-id="9f7d3-137">Format Block</span></span> | <span data-ttu-id="9f7d3-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-138">**NULL**</span></span>                               |



 

<span data-ttu-id="9f7d3-139">**Información del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-139">**Device Information**</span></span>

<span data-ttu-id="9f7d3-140">El controlador Lee dinámicamente la información del ROM de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="9f7d3-141">La aplicación puede recuperar esta información enlazando el moniker del dispositivo a un contenedor de propiedades y llamando al método **IPropertyBag:: Read** .</span><span class="sxs-lookup"><span data-stu-id="9f7d3-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="9f7d3-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f7d3-142">Property</span></span>            | <span data-ttu-id="9f7d3-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f7d3-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="9f7d3-144">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9f7d3-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9f7d3-145">UniqueID \_ bajo</span><span class="sxs-lookup"><span data-stu-id="9f7d3-145">UniqueID\_Low</span></span>       | <span data-ttu-id="9f7d3-146">IDENTIFICADOR único del dispositivo ( **DWORD** inferior).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="9f7d3-147">**Long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="9f7d3-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="9f7d3-148">UniqueID \_ alto</span><span class="sxs-lookup"><span data-stu-id="9f7d3-148">UniqueID\_High</span></span>      | <span data-ttu-id="9f7d3-149">IDENTIFICADOR único del dispositivo ( **DWORD** alto)</span><span class="sxs-lookup"><span data-stu-id="9f7d3-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="9f7d3-150">**long**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-150">**long**</span></span>            |
| <span data-ttu-id="9f7d3-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="9f7d3-151">VendorID</span></span>            | <span data-ttu-id="9f7d3-152">IDENTIFICADOR del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="9f7d3-153">**long**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-153">**long**</span></span>            |
| <span data-ttu-id="9f7d3-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="9f7d3-154">ModelID</span></span>             | <span data-ttu-id="9f7d3-155">Identificador del modelo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="9f7d3-156">**long**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-156">**long**</span></span>            |
| <span data-ttu-id="9f7d3-157">VendorText</span><span class="sxs-lookup"><span data-stu-id="9f7d3-157">VendorText</span></span>          | <span data-ttu-id="9f7d3-158">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="9f7d3-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="9f7d3-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="9f7d3-160">ModelText</span><span class="sxs-lookup"><span data-stu-id="9f7d3-160">ModelText</span></span>           | <span data-ttu-id="9f7d3-161">Nombre del modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="9f7d3-162">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-162">**BSTR**</span></span>            |
| <span data-ttu-id="9f7d3-163">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="9f7d3-163">UnitModelText</span></span>       | <span data-ttu-id="9f7d3-164">Nombre del modelo de unidad; puede ser igual que ModelText.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="9f7d3-165">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-165">**BSTR**</span></span>            |
| <span data-ttu-id="9f7d3-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="9f7d3-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="9f7d3-167">carga de oPCR (control de conector de salida).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="9f7d3-168">Ejemplo: 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="9f7d3-169">**long**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-169">**long**</span></span>            |
| <span data-ttu-id="9f7d3-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="9f7d3-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="9f7d3-171">velocidad de datos oPCR.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-171">oPCR data rate.</span></span> <span data-ttu-id="9f7d3-172">Ejemplos: 0 (S100), 1 (S200) o 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="9f7d3-173">**long**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-173">**long**</span></span>            |
| <span data-ttu-id="9f7d3-174">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="9f7d3-174">DeviceClassGUID</span></span>     | <span data-ttu-id="9f7d3-175">GUID que identifica el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="9f7d3-176">En el caso de MSTape, este valor es `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="9f7d3-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="9f7d3-177">Este GUID se define como MSTapeDeviceGUID en el archivo de encabezado Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="9f7d3-178">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-178">**BSTR**</span></span>            |
| <span data-ttu-id="9f7d3-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f7d3-179">Description</span></span>         | <span data-ttu-id="9f7d3-180">Descripción del dispositivo, tomada del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="9f7d3-181">Esta cadena normalmente contiene el nombre de marca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="9f7d3-182">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="9f7d3-182">**BSTR**</span></span>            |



 

<span data-ttu-id="9f7d3-183">El identificador de dispositivo es un entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="9f7d3-184">El **valor DWORD** inferior se almacena en la \_ propiedad UniqueID Low y el **valor DWORD** superior se almacena en la \_ propiedad UniqueID High.</span><span class="sxs-lookup"><span data-stu-id="9f7d3-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="9f7d3-185">Para obtener más información acerca de los monikers de dispositivo, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="9f7d3-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f7d3-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f7d3-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f7d3-187">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f7d3-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9f7d3-188">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="9f7d3-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



