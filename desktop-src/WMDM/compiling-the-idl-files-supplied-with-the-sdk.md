---
title: Compilar los archivos IDL suministrados con el SDK
description: Compilar los archivos IDL suministrados con el SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Administrador de dispositivos de Windows Media, archivos IDL
- Administrador de dispositivos, archivos IDL
- aplicaciones de escritorio, archivos IDL
- proveedores de servicios, archivos IDL
- Guía de programación, archivos IDL
- IDL (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695380"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="212e9-109">Compilar los archivos IDL suministrados con el SDK</span><span class="sxs-lookup"><span data-stu-id="212e9-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="212e9-110">El SDK de Administrador de dispositivos de Windows Media incluye tanto archivos de encabezado como archivos IDL de origen para la mayoría de estos archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="212e9-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="212e9-111">Los archivos de encabezado se encuentran en \\ la \\ carpeta Inc de la ruta de instalación del SDK.</span><span class="sxs-lookup"><span data-stu-id="212e9-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="212e9-112">Los archivos IDL se encuentran en la \\ \\ carpeta IDL.</span><span class="sxs-lookup"><span data-stu-id="212e9-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="212e9-113">Los encabezados precompilados son mucho más fáciles de usar y varios de los archivos IDL se combinan en un único encabezado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="212e9-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="212e9-114">Sin embargo, si decide procesar sus propios archivos de encabezado a partir de los archivos IDL proporcionados, en este tema se describen los archivos IDL que crean los archivos de encabezado y también se describen las dependencias de cada archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="212e9-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="212e9-115">**Archivos de encabezado IDL y proporcionados equivalentes**</span><span class="sxs-lookup"><span data-stu-id="212e9-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="212e9-116">**IDL**</span><span class="sxs-lookup"><span data-stu-id="212e9-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="212e9-117">**Encabezado proporcionado equivalente**</span><span class="sxs-lookup"><span data-stu-id="212e9-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="212e9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="212e9-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="212e9-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-119">WMDM.idl</span></span><br/> <span data-ttu-id="212e9-120">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-120">WMSP.idl</span></span><br/> <span data-ttu-id="212e9-121">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-121">WMSCP.idl</span></span><br/> <span data-ttu-id="212e9-122">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="212e9-123">Mswmdm. h</span><span class="sxs-lookup"><span data-stu-id="212e9-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="212e9-124">Los cuatro archivos IDL se incluyen en este único encabezado proporcionado.</span><span class="sxs-lookup"><span data-stu-id="212e9-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="212e9-125">**WMDM. idl** define todas las interfaces de aplicación y las estructuras, constantes y códigos de error necesarios.</span><span class="sxs-lookup"><span data-stu-id="212e9-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="212e9-126">**WMSP. idl** define todas las interfaces del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="212e9-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="212e9-127">**WMSCP. idl** define todas las interfaces, los valores de GUID y las constantes que requieren los proveedores de contenido seguro.</span><span class="sxs-lookup"><span data-stu-id="212e9-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="212e9-128">**icomponentauthenticate. idl** define la interfaz [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="212e9-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="212e9-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="212e9-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="212e9-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="212e9-131">wmdmlog \_ c</span><span class="sxs-lookup"><span data-stu-id="212e9-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="212e9-132">Define las interfaces de registro.</span><span class="sxs-lookup"><span data-stu-id="212e9-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="212e9-133">Se deben usar ambos archivos de encabezado suministrados, en lugar de solo el archivo. h, debido a un problema con el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="212e9-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="212e9-134">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="212e9-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="212e9-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="212e9-136">Define las interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) y [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) que usan las aplicaciones que actualizan DRM en dispositivos o recuentos de las métricas en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="212e9-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="212e9-137">**Dependencias IDL**</span><span class="sxs-lookup"><span data-stu-id="212e9-137">**IDL Dependencies**</span></span>

<span data-ttu-id="212e9-138">Varios de los archivos IDL proporcionados tienen dependencias de compilación.</span><span class="sxs-lookup"><span data-stu-id="212e9-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="212e9-139">Si tiene previsto compilar los archivos IDL personalmente, debe procesar estas dependencias externas en el orden que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="212e9-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="212e9-140">**IDL**</span><span class="sxs-lookup"><span data-stu-id="212e9-140">**IDL**</span></span>                    | <span data-ttu-id="212e9-141">**Dependencias**</span><span class="sxs-lookup"><span data-stu-id="212e9-141">**Dependencies**</span></span>                                                                 |
| <span data-ttu-id="212e9-142">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="212e9-143">importar "oaidl. idl";</span><span class="sxs-lookup"><span data-stu-id="212e9-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="212e9-144">\#incluir "icomponentauthenticate. idl"</span><span class="sxs-lookup"><span data-stu-id="212e9-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="212e9-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-145">WMDM.idl</span></span>                   | <span data-ttu-id="212e9-146">No hay dependencias externas</span><span class="sxs-lookup"><span data-stu-id="212e9-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="212e9-147">WmdmLog. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-147">WmdmLog.idl</span></span>                | <span data-ttu-id="212e9-148">No hay dependencias externas</span><span class="sxs-lookup"><span data-stu-id="212e9-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="212e9-149">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="212e9-150">No hay dependencias externas</span><span class="sxs-lookup"><span data-stu-id="212e9-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="212e9-151">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-151">WMSCP.idl</span></span>                  | <span data-ttu-id="212e9-152">\#incluir "WMDRMDeviceApp. idl"</span><span class="sxs-lookup"><span data-stu-id="212e9-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="212e9-153">\#incluir "WMSP. idl"</span><span class="sxs-lookup"><span data-stu-id="212e9-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="212e9-154">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="212e9-154">WMSP.idl</span></span>                   | <span data-ttu-id="212e9-155">\#incluir "WMDM. idl"</span><span class="sxs-lookup"><span data-stu-id="212e9-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="212e9-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="212e9-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212e9-157">**Tareas comunes a las aplicaciones y proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="212e9-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





