---
title: Compilación de los archivos IDL proporcionados con el SDK
description: Compilación de los archivos IDL proporcionados con el SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Archivos IDL Administrador de dispositivos Windows Media
- Administrador de dispositivos,archivos IDL
- aplicaciones de escritorio, archivos IDL
- proveedores de servicios, archivos IDL
- guía de programación, archivos IDL
- IDL (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444016"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="d61e0-109">Compilación de los archivos IDL proporcionados con el SDK</span><span class="sxs-lookup"><span data-stu-id="d61e0-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="d61e0-110">Windows Media Administrador de dispositivos SDK incluye los archivos de encabezado y los archivos IDL de origen para la mayoría de estos archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d61e0-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="d61e0-111">Los archivos de encabezado se encuentran en la \\ carpeta inc en la ruta de instalación del \\ SDK.</span><span class="sxs-lookup"><span data-stu-id="d61e0-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="d61e0-112">Los archivos IDL se encuentran en la \\ carpeta \\ idl.</span><span class="sxs-lookup"><span data-stu-id="d61e0-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="d61e0-113">Los encabezados precompilados son mucho más sencillos de usar y varios de los archivos IDL se combinan en un único encabezado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d61e0-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="d61e0-114">Sin embargo, si decide procesar sus propios archivos de encabezado a partir de los archivos IDL proporcionados, en este tema se describen qué archivos IDL crean qué archivos de encabezado y también se describen las dependencias de cada archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d61e0-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="d61e0-115">**Archivos de encabezado IDL y proporcionados equivalentes**</span><span class="sxs-lookup"><span data-stu-id="d61e0-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="d61e0-116">**Idl**</span><span class="sxs-lookup"><span data-stu-id="d61e0-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="d61e0-117">**Encabezado proporcionado equivalente**</span><span class="sxs-lookup"><span data-stu-id="d61e0-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="d61e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d61e0-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d61e0-119">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-119">WMDM.idl</span></span><br/> <span data-ttu-id="d61e0-120">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-120">WMSP.idl</span></span><br/> <span data-ttu-id="d61e0-121">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-121">WMSCP.idl</span></span><br/> <span data-ttu-id="d61e0-122">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="d61e0-123">Mswmdm.h</span><span class="sxs-lookup"><span data-stu-id="d61e0-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="d61e0-124">Los cuatro archivos IDL se incluyen en este encabezado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d61e0-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="d61e0-125">**WMDM.idl** Define todas las interfaces de aplicación y las estructuras, constantes y códigos de error necesarios.</span><span class="sxs-lookup"><span data-stu-id="d61e0-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="d61e0-126">**WMSP.idl** Define todas las interfaces del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d61e0-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="d61e0-127">**WMSCP.idl** Define todas las interfaces, valores GUID y constantes que requieren los proveedores de contenido seguro.</span><span class="sxs-lookup"><span data-stu-id="d61e0-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="d61e0-128">**icomponentauthenticate.idl Define** la [**interfaz IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)</span><span class="sxs-lookup"><span data-stu-id="d61e0-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="d61e0-129">Wmdmlog.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="d61e0-130">Wmdmlog.h</span><span class="sxs-lookup"><span data-stu-id="d61e0-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="d61e0-131">wmdmlog \_ i.c</span><span class="sxs-lookup"><span data-stu-id="d61e0-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="d61e0-132">Define las interfaces de registro.</span><span class="sxs-lookup"><span data-stu-id="d61e0-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="d61e0-133">Ambos archivos de encabezado proporcionados deben usarse, en lugar de solo el archivo .h, debido a un problema con el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d61e0-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d61e0-134">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="d61e0-135">Wmdrmdeviceapp.h</span><span class="sxs-lookup"><span data-stu-id="d61e0-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="d61e0-136">Define las [**interfaces IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) que usan las aplicaciones que actualizan DRM en dispositivos o recuentos de reproducción de medidores en dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d61e0-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="d61e0-137">**Dependencias de IDL**</span><span class="sxs-lookup"><span data-stu-id="d61e0-137">**IDL Dependencies**</span></span>

<span data-ttu-id="d61e0-138">Varios de los archivos IDL proporcionados tienen dependencias de compilación.</span><span class="sxs-lookup"><span data-stu-id="d61e0-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="d61e0-139">Si planea compilar los archivos IDL usted mismo, debe procesar estas dependencias externas en el orden que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d61e0-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="d61e0-140">Idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-140">IDL</span></span>                      |   <span data-ttu-id="d61e0-141">Dependencias</span><span class="sxs-lookup"><span data-stu-id="d61e0-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d61e0-142">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="d61e0-143">import "oaidl.idl";</span><span class="sxs-lookup"><span data-stu-id="d61e0-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="d61e0-144">\#include "icomponentauthenticate.idl"</span><span class="sxs-lookup"><span data-stu-id="d61e0-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="d61e0-145">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-145">WMDM.idl</span></span>                   | <span data-ttu-id="d61e0-146">Sin dependencias externas</span><span class="sxs-lookup"><span data-stu-id="d61e0-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="d61e0-147">WmdmLog.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-147">WmdmLog.idl</span></span>                | <span data-ttu-id="d61e0-148">Sin dependencias externas</span><span class="sxs-lookup"><span data-stu-id="d61e0-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="d61e0-149">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="d61e0-150">Sin dependencias externas</span><span class="sxs-lookup"><span data-stu-id="d61e0-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="d61e0-151">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-151">WMSCP.idl</span></span>                  | <span data-ttu-id="d61e0-152">\#incluir "WMDRMDeviceApp.idl"</span><span class="sxs-lookup"><span data-stu-id="d61e0-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="d61e0-153">\#incluir "WMSP.idl"</span><span class="sxs-lookup"><span data-stu-id="d61e0-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="d61e0-154">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="d61e0-154">WMSP.idl</span></span>                   | <span data-ttu-id="d61e0-155">\#incluir "WMDM.idl"</span><span class="sxs-lookup"><span data-stu-id="d61e0-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d61e0-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d61e0-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d61e0-157">**Tareas comunes para aplicaciones y proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="d61e0-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





