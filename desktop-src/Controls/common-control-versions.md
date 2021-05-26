---
title: Versiones de control comunes
description: En este tema se enumeran las versiones disponibles de la biblioteca de control común (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo dirigir la aplicación para una versión específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423965"
---
# <a name="common-control-versions"></a><span data-ttu-id="9b3c8-103">Versiones de control comunes</span><span class="sxs-lookup"><span data-stu-id="9b3c8-103">Common Control Versions</span></span>

<span data-ttu-id="9b3c8-104">En este tema se enumeran las versiones disponibles de la biblioteca de control común (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo dirigir la aplicación para una versión específica.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="9b3c8-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9b3c8-106">Números comunes de versiones de DLL de control</span><span class="sxs-lookup"><span data-stu-id="9b3c8-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="9b3c8-107">Tamaños de estructura para diferentes versiones de control comunes</span><span class="sxs-lookup"><span data-stu-id="9b3c8-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="9b3c8-108">Usar DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="9b3c8-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="9b3c8-109">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="9b3c8-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="9b3c8-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b3c8-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="9b3c8-111">Números comunes de versiones de DLL de control</span><span class="sxs-lookup"><span data-stu-id="9b3c8-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="9b3c8-112">La compatibilidad con los controles comunes se proporciona ComCtl32.dll, que incluyen todas las versiones de 32 y 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="9b3c8-113">Cada versión sucesiva del archivo DLL admite las características y la API de versiones anteriores y agrega nuevas características.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="9b3c8-114">Dado que varias versiones de ComCtl32.dll se distribuyeron con Internet Explorer, la versión que está activa a veces es diferente de la versión que se distribuyó con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="9b3c8-115">Por lo tanto, la aplicación debe determinar directamente qué versión de ComCtl32.dll está presente.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="9b3c8-116">En la documentación de referencia de controles comunes, muchos elementos de programación especifican un número mínimo de versión de DLL compatible.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="9b3c8-117">Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="9b3c8-118">Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="9b3c8-119">En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron en sistemas operativos compatibles.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="9b3c8-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="9b3c8-120">ComCtl32.dll</span></span>

<span data-ttu-id="9b3c8-121">Versión</span><span class="sxs-lookup"><span data-stu-id="9b3c8-121">Version</span></span>

<span data-ttu-id="9b3c8-122">Plataforma de distribución</span><span class="sxs-lookup"><span data-stu-id="9b3c8-122">Distribution Platform</span></span>

<span data-ttu-id="9b3c8-123">5.81</span><span class="sxs-lookup"><span data-stu-id="9b3c8-123">5.81</span></span>

<span data-ttu-id="9b3c8-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5 y Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="9b3c8-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="9b3c8-125">5.82</span><span class="sxs-lookup"><span data-stu-id="9b3c8-125">5.82</span></span>

<span data-ttu-id="9b3c8-126">Windows Server 2003, Windows Vista, Windows Server 2008 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b3c8-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="9b3c8-127">6.0</span><span class="sxs-lookup"><span data-stu-id="9b3c8-127">6.0</span></span>

<span data-ttu-id="9b3c8-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b3c8-128">Windows Server 2003</span></span>

<span data-ttu-id="9b3c8-129">6.10</span><span class="sxs-lookup"><span data-stu-id="9b3c8-129">6.10</span></span>

<span data-ttu-id="9b3c8-130">Windows Vista, Windows Server 2008 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b3c8-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="9b3c8-131">Tamaños de estructura para diferentes versiones de control comunes</span><span class="sxs-lookup"><span data-stu-id="9b3c8-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="9b3c8-132">Las mejoras continuas en los controles comunes han dado lugar a la necesidad de extender muchas de las estructuras.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="9b3c8-133">Por esta razón, el tamaño de las estructuras ha cambiado entre diferentes versiones de Commctrl.h.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="9b3c8-134">Dado que la mayoría de las estructuras de control comunes toman un tamaño de estructura como uno de los parámetros, se puede producir un error en un mensaje o una función si no se reconoce el tamaño.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="9b3c8-135">Para solucionar este problema, se han definido constantes de tamaño de estructura para ayudar a tener como destino una versión diferente de ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="9b3c8-136">En la lista siguiente se definen las constantes de tamaño de estructura.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-136">The following list defines the structure size constants.</span></span>



|    <span data-ttu-id="9b3c8-137">Constante de tamaño de estructura</span><span class="sxs-lookup"><span data-stu-id="9b3c8-137">Structure Size Constant</span></span>                           |     <span data-ttu-id="9b3c8-138">Definición</span><span class="sxs-lookup"><span data-stu-id="9b3c8-138">Definition</span></span>                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3c8-139">TAMAÑO DE HDITEM \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-139">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="9b3c8-140">Tamaño de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) de la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-140">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="9b3c8-141">TAMAÑO DE IMAGELISTDRAWPARAMS \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-141">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="9b3c8-142">Tamaño de la [**estructura IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) en la versión 5.9.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-142">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="9b3c8-143">LVCOLUMN \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-143">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="9b3c8-144">Tamaño de la [**estructura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-144">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="9b3c8-145">LVGROUP \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-145">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="9b3c8-146">Tamaño de la [**estructura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) en la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-146">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="9b3c8-147">LVHITTESTINFO \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-147">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="9b3c8-148">Tamaño de la [**estructura LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-148">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="9b3c8-149">LVITEM \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-149">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="9b3c8-150">Tamaño de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="9b3c8-151">LVITEM \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-151">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="9b3c8-152">Tamaño de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-152">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="9b3c8-153">LVTILEINFO \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-153">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="9b3c8-154">Tamaño de la [**estructura LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) en la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-154">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="9b3c8-155">TAMAÑO DE MCHITTESTINFO \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-155">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="9b3c8-156">Tamaño de la [**estructura MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-156">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="9b3c8-157">TAMAÑO NMLVCUSTOMDRAW \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-157">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="9b3c8-158">Tamaño de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) en la versión 4.7.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-158">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="9b3c8-159">TAMAÑO NMTTDISPINFO \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-159">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="9b3c8-160">Tamaño de la [**estructura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-160">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="9b3c8-161">TAMAÑO NMTVCUSTOMDRAW \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-161">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="9b3c8-162">Tamaño de la [**estructura NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) en la versión 4.7.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-162">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="9b3c8-163">TAMAÑO PROPSHEETHEADER \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-163">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="9b3c8-164">Tamaño de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-164">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="9b3c8-165">TAMAÑO DE PROPSHEETPAGE \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-165">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="9b3c8-166">Tamaño de la estructura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-166">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="9b3c8-167">TAMAÑO DE REBARBANDINFO \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-167">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="9b3c8-168">Tamaño de la [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 4.7.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="9b3c8-169">TAMAÑO DE REBARBANDINFO \_ V6 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-169">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="9b3c8-170">Tamaño de la [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-170">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="9b3c8-171">TTTOOLINFO \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-171">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="9b3c8-172">Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="9b3c8-173">TTTOOLINFO \_ V2 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-173">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="9b3c8-174">Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4.7.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="9b3c8-175">TTTOOLINFO \_ V3 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="9b3c8-175">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="9b3c8-176">Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-176">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="9b3c8-177">TAMAÑO DE TVINSERTSTRUCT \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="9b3c8-177">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="9b3c8-178">Tamaño de la [**estructura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) en la versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-178">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="9b3c8-179">Usar DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="9b3c8-179">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="9b3c8-180">Una aplicación puede llamar a la función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para determinar qué versión de DLL está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-180">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="9b3c8-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) devuelve una [**estructura DLLVERSIONINFO2.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2)</span><span class="sxs-lookup"><span data-stu-id="9b3c8-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="9b3c8-182">Además de la información proporcionada a través de [**DLLVERSIONINFO,**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) **DLLVERSIONINFO2** también proporciona el número de revisión que identifica el Service Pack instalado más reciente, que proporciona una manera más sólida de comparar los números de versión.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-182">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="9b3c8-183">Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO,** la estructura posterior es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-183">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="9b3c8-184">La siguiente función de `GetVersion` ejemplo carga un archivo DLL especificado e intenta llamar a su función [**DllGetVersion.**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc)</span><span class="sxs-lookup"><span data-stu-id="9b3c8-184">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="9b3c8-185">Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) en un **DWORD** que se devuelve a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-185">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="9b3c8-186">Si el archivo DLL no exporta **DllGetVersion,** la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-186">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="9b3c8-187">Puede modificar la función para controlar la posibilidad de **que DllGetVersion** devuelva una [**estructura DLLVERSIONINFO2.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2)</span><span class="sxs-lookup"><span data-stu-id="9b3c8-187">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="9b3c8-188">Si es así, use la información del miembro **ullVersion** de esa estructura **DLLVERSIONINFO2** para comparar versiones, números de compilación y versiones de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-188">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="9b3c8-189">La [**macro MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion.**</span><span class="sxs-lookup"><span data-stu-id="9b3c8-189">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="9b3c8-190">El [**uso incorrecto de LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-190">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="9b3c8-191">Consulte la documentación **de LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-191">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="9b3c8-192">En el ejemplo de código siguiente se muestra cómo puede usar para probar si `GetVersion` ComCtl32.dll versión 6.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-192">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="9b3c8-193">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="9b3c8-193">Project Versions</span></span>

<span data-ttu-id="9b3c8-194">Para asegurarse de que la aplicación es compatible con diferentes versiones de destino de un archivo .dll, las macros de versión están presentes en los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-194">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="9b3c8-195">Estas macros se usan para definir, excluir o volver a definir determinadas definiciones para distintas versiones del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-195">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="9b3c8-196">Consulte [Uso de los encabezados de Windows](/windows/desktop/WinProg/using-the-windows-headers) para obtener una descripción detallada de estas macros.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-196">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="9b3c8-197">Por ejemplo, el nombre de macro **\_ WIN32 \_ IE** se encuentra normalmente en encabezados anteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-197">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="9b3c8-198">Usted es responsable de definir la macro como un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-198">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="9b3c8-199">Este número de versión define la versión de destino de la aplicación que usa el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-199">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="9b3c8-200">En la tabla siguiente se muestran los números de versión disponibles y el efecto que tiene cada uno en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-200">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="9b3c8-201">Versión</span><span class="sxs-lookup"><span data-stu-id="9b3c8-201">Version</span></span> | <span data-ttu-id="9b3c8-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b3c8-202">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3c8-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="9b3c8-203">0x0300</span></span>  | <span data-ttu-id="9b3c8-204">La aplicación es compatible con ComCtl32.dll versión 4.70 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-204">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="9b3c8-205">La aplicación no puede implementar características que se agregaron después de la versión 4.70.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-205">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="9b3c8-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="9b3c8-206">0x0400</span></span>  | <span data-ttu-id="9b3c8-207">La aplicación es compatible con ComCtl32.dll versión 4.71 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-207">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="9b3c8-208">La aplicación no puede implementar características que se agregaron después de la versión 4.71.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-208">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="9b3c8-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="9b3c8-209">0x0401</span></span>  | <span data-ttu-id="9b3c8-210">La aplicación es compatible con ComCtl32.dll versión 4.72 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-210">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="9b3c8-211">La aplicación no puede implementar características que se agregaron después de la versión 4.72.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-211">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="9b3c8-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="9b3c8-212">0x0500</span></span>  | <span data-ttu-id="9b3c8-213">La aplicación es compatible con ComCtl32.dll versión 5.80 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-213">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="9b3c8-214">La aplicación no puede implementar características que se agregaron después de la versión 5.80.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-214">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="9b3c8-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="9b3c8-215">0x0501</span></span>  | <span data-ttu-id="9b3c8-216">La aplicación es compatible con ComCtl32.dll versión 5.81 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-216">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="9b3c8-217">La aplicación no puede implementar características que se agregaron después de la versión 5.81.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-217">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="9b3c8-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="9b3c8-218">0x0600</span></span>  | <span data-ttu-id="9b3c8-219">La aplicación es compatible con ComCtl32.dll versión 6.0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-219">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="9b3c8-220">La aplicación no puede implementar características que se agregaron después de la versión 6.0.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-220">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="9b3c8-221">Si no define la macro **\_ WIN32 \_ IE** en el proyecto, se define automáticamente como 0x0500.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="9b3c8-222">Para definir un valor diferente, puede agregar lo siguiente a las directivas del compilador en el archivo make. sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="9b3c8-223">Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado de Shell.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="9b3c8-224">Sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-224">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="9b3c8-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b3c8-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b3c8-226">Acerca de los controles comunes</span><span class="sxs-lookup"><span data-stu-id="9b3c8-226">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 