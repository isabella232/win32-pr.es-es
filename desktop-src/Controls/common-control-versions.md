---
title: Versiones de controles comunes
description: En este tema se enumeran las versiones disponibles de la biblioteca de controles comunes (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo establecer como destino la aplicación para una versión específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488591"
---
# <a name="common-control-versions"></a><span data-ttu-id="00d02-103">Versiones de controles comunes</span><span class="sxs-lookup"><span data-stu-id="00d02-103">Common Control Versions</span></span>

<span data-ttu-id="00d02-104">En este tema se enumeran las versiones disponibles de la biblioteca de controles comunes (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo establecer como destino la aplicación para una versión específica.</span><span class="sxs-lookup"><span data-stu-id="00d02-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="00d02-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="00d02-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="00d02-106">Números de versión de DLL de control común</span><span class="sxs-lookup"><span data-stu-id="00d02-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="00d02-107">Tamaños de estructura para diferentes versiones de control comunes</span><span class="sxs-lookup"><span data-stu-id="00d02-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="00d02-108">Uso de DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="00d02-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="00d02-109">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="00d02-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="00d02-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00d02-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="00d02-111">Números de versión de DLL de control común</span><span class="sxs-lookup"><span data-stu-id="00d02-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="00d02-112">ComCtl32.dll proporciona compatibilidad con los controles comunes, que incluyen todas las versiones de 32 y 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="00d02-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="00d02-113">Cada versión sucesiva del archivo DLL es compatible con las características y API de las versiones anteriores y agrega nuevas características.</span><span class="sxs-lookup"><span data-stu-id="00d02-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="00d02-114">Dado que varias versiones de ComCtl32.dll se distribuyeron con Internet Explorer, la versión que está activa a veces es diferente de la versión que se distribuyó con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00d02-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="00d02-115">Por lo tanto, la aplicación debe determinar directamente qué versión de ComCtl32.dll está presente.</span><span class="sxs-lookup"><span data-stu-id="00d02-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="00d02-116">En la documentación de referencia de controles comunes, muchos elementos de programación especifican un número de versión de DLL compatible mínima.</span><span class="sxs-lookup"><span data-stu-id="00d02-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="00d02-117">Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="00d02-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="00d02-118">Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes de la DLL.</span><span class="sxs-lookup"><span data-stu-id="00d02-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="00d02-119">En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron en los sistemas operativos compatibles.</span><span class="sxs-lookup"><span data-stu-id="00d02-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="00d02-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="00d02-120">ComCtl32.dll</span></span>

<span data-ttu-id="00d02-121">Versión</span><span class="sxs-lookup"><span data-stu-id="00d02-121">Version</span></span>

<span data-ttu-id="00d02-122">Plataforma de distribución</span><span class="sxs-lookup"><span data-stu-id="00d02-122">Distribution Platform</span></span>

<span data-ttu-id="00d02-123">5,81</span><span class="sxs-lookup"><span data-stu-id="00d02-123">5.81</span></span>

<span data-ttu-id="00d02-124">Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 y Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="00d02-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="00d02-125">5,82</span><span class="sxs-lookup"><span data-stu-id="00d02-125">5.82</span></span>

<span data-ttu-id="00d02-126">Windows Server 2003, Windows Vista, Windows Server 2008 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="00d02-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="00d02-127">6.0</span><span class="sxs-lookup"><span data-stu-id="00d02-127">6.0</span></span>

<span data-ttu-id="00d02-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00d02-128">Windows Server 2003</span></span>

<span data-ttu-id="00d02-129">6.10</span><span class="sxs-lookup"><span data-stu-id="00d02-129">6.10</span></span>

<span data-ttu-id="00d02-130">Windows Vista, Windows Server 2008 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="00d02-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="00d02-131">Tamaños de estructura para diferentes versiones de control comunes</span><span class="sxs-lookup"><span data-stu-id="00d02-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="00d02-132">Las mejoras continuas en los controles comunes han dado lugar a la necesidad de extender muchas de las estructuras.</span><span class="sxs-lookup"><span data-stu-id="00d02-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="00d02-133">Por esta razón, el tamaño de las estructuras ha cambiado entre las distintas versiones de commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="00d02-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="00d02-134">Dado que la mayoría de las estructuras de control comunes toman un tamaño de estructura como uno de los parámetros, se puede producir un error en un mensaje o una función si no se reconoce el tamaño.</span><span class="sxs-lookup"><span data-stu-id="00d02-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="00d02-135">Para solucionar este comportamiento, las constantes de tamaño de la estructura se han definido como ayuda para tener como destino una versión diferente de ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="00d02-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="00d02-136">En la lista siguiente se definen las constantes de tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="00d02-136">The following list defines the structure size constants.</span></span>



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-137">Tamaño de HDITEM \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-137">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="00d02-138">Tamaño de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-138">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="00d02-139">Tamaño de IMAGELISTDRAWPARAMS \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-139">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="00d02-140">Tamaño de la estructura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) en la versión 5,9.</span><span class="sxs-lookup"><span data-stu-id="00d02-140">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="00d02-141">Tamaño de LVCOLUMN \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-141">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="00d02-142">Tamaño de la estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-142">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="00d02-143">Tamaño de LVGROUP \_ V5 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-143">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="00d02-144">Tamaño de la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) en la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-144">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="00d02-145">Tamaño de LVHITTESTINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-145">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="00d02-146">Tamaño de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-146">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="00d02-147">Tamaño de LVITEM \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-147">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="00d02-148">Tamaño de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-148">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="00d02-149">Tamaño de LVITEM \_ V5 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-149">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="00d02-150">Tamaño de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="00d02-151">Tamaño de LVTILEINFO \_ V5 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-151">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="00d02-152">Tamaño de la estructura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) en la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-152">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="00d02-153">Tamaño de MCHITTESTINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-153">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="00d02-154">Tamaño de la estructura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-154">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="00d02-155">Tamaño de NMLVCUSTOMDRAW \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-155">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="00d02-156">Tamaño de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) en la versión 4,7.</span><span class="sxs-lookup"><span data-stu-id="00d02-156">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="00d02-157">Tamaño de NMTTDISPINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-157">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="00d02-158">Tamaño de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-158">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="00d02-159">Tamaño de NMTVCUSTOMDRAW \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-159">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="00d02-160">Tamaño de la estructura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) en la versión 4,7.</span><span class="sxs-lookup"><span data-stu-id="00d02-160">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="00d02-161">Tamaño de PROPSHEETHEADER \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-161">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="00d02-162">Tamaño de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-162">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="00d02-163">Tamaño de PROPSHEETPAGE \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-163">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="00d02-164">Tamaño de la estructura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-164">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="00d02-165">Tamaño de REBARBANDINFO \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-165">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="00d02-166">Tamaño de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 4,7.</span><span class="sxs-lookup"><span data-stu-id="00d02-166">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="00d02-167">Tamaño de REBARBANDINFO \_ V6 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-167">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="00d02-168">Tamaño de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="00d02-169">Tamaño de TTTOOLINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-169">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="00d02-170">Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-170">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="00d02-171">Tamaño de TTTOOLINFO \_ V2 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-171">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="00d02-172">Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4,7.</span><span class="sxs-lookup"><span data-stu-id="00d02-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="00d02-173">Tamaño de TTTOOLINFO \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-173">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="00d02-174">Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="00d02-175">Tamaño de TVINSERTSTRUCT \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="00d02-175">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="00d02-176">Tamaño de la estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) en la versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-176">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="00d02-177">Uso de DllGetVersion para determinar el número de versión</span><span class="sxs-lookup"><span data-stu-id="00d02-177">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="00d02-178">Una aplicación puede llamar a la función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para determinar qué versión de dll está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="00d02-178">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="00d02-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) devuelve una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="00d02-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="00d02-180">Además de la información proporcionada a través de [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** también proporciona el número de revisión que identifica la Service Pack instalada más reciente, que proporciona una manera más eficaz de comparar los números de versión.</span><span class="sxs-lookup"><span data-stu-id="00d02-180">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="00d02-181">Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO** , la estructura posterior es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-181">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="00d02-182">La función de ejemplo siguiente `GetVersion` carga un archivo dll especificado e intenta llamar a su función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="00d02-182">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="00d02-183">Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) en un **valor DWORD** que se devuelve a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="00d02-183">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="00d02-184">Si el archivo DLL no exporta **DllGetVersion**, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="00d02-184">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="00d02-185">Puede modificar la función para controlar la posibilidad de que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="00d02-185">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="00d02-186">Si es así, use la información del miembro **ullVersion** de la estructura **DLLVERSIONINFO2** para comparar las versiones, los números de compilación y las versiones de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="00d02-186">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="00d02-187">La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="00d02-187">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="00d02-188">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="00d02-188">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="00d02-189">Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="00d02-189">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


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



<span data-ttu-id="00d02-190">En el ejemplo de código siguiente se muestra cómo puede usar `GetVersion` para comprobar si ComCtl32.dll es la versión 6,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="00d02-190">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


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



## <a name="project-versions"></a><span data-ttu-id="00d02-191">Versiones del proyecto</span><span class="sxs-lookup"><span data-stu-id="00d02-191">Project Versions</span></span>

<span data-ttu-id="00d02-192">Para asegurarse de que la aplicación es compatible con las distintas versiones de destino de un archivo. dll, las macros de versión están presentes en los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="00d02-192">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="00d02-193">Estas macros se utilizan para definir, excluir o volver a definir ciertas definiciones para diferentes versiones de la DLL.</span><span class="sxs-lookup"><span data-stu-id="00d02-193">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="00d02-194">Vea [usar los encabezados de Windows](/windows/desktop/WinProg/using-the-windows-headers) para obtener una descripción detallada de estas macros.</span><span class="sxs-lookup"><span data-stu-id="00d02-194">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="00d02-195">Por ejemplo, el nombre de macro **\_ Win32 \_ IE** suele encontrarse en encabezados más antiguos.</span><span class="sxs-lookup"><span data-stu-id="00d02-195">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="00d02-196">Usted es responsable de definir la macro como un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="00d02-196">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="00d02-197">Este número de versión define la versión de destino de la aplicación que está usando el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="00d02-197">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="00d02-198">En la tabla siguiente se muestran los números de versión disponibles y el efecto que cada tiene en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00d02-198">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="00d02-199">Versión</span><span class="sxs-lookup"><span data-stu-id="00d02-199">Version</span></span> | <span data-ttu-id="00d02-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="00d02-200">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d02-201">0x0300</span><span class="sxs-lookup"><span data-stu-id="00d02-201">0x0300</span></span>  | <span data-ttu-id="00d02-202">La aplicación es compatible con ComCtl32.dll versión 4,70 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-202">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="00d02-203">La aplicación no puede implementar características que se agregaron después de la versión 4,70.</span><span class="sxs-lookup"><span data-stu-id="00d02-203">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="00d02-204">0x0400</span><span class="sxs-lookup"><span data-stu-id="00d02-204">0x0400</span></span>  | <span data-ttu-id="00d02-205">La aplicación es compatible con ComCtl32.dll versión 4,71 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-205">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="00d02-206">La aplicación no puede implementar características que se agregaron después de la versión 4,71.</span><span class="sxs-lookup"><span data-stu-id="00d02-206">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="00d02-207">0x0401</span><span class="sxs-lookup"><span data-stu-id="00d02-207">0x0401</span></span>  | <span data-ttu-id="00d02-208">La aplicación es compatible con ComCtl32.dll versión 4,72 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-208">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="00d02-209">La aplicación no puede implementar características que se agregaron después de la versión 4,72.</span><span class="sxs-lookup"><span data-stu-id="00d02-209">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="00d02-210">0x0500</span><span class="sxs-lookup"><span data-stu-id="00d02-210">0x0500</span></span>  | <span data-ttu-id="00d02-211">La aplicación es compatible con ComCtl32.dll versión 5,80 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-211">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="00d02-212">La aplicación no puede implementar características que se agregaron después de la versión 5,80.</span><span class="sxs-lookup"><span data-stu-id="00d02-212">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="00d02-213">0x0501</span><span class="sxs-lookup"><span data-stu-id="00d02-213">0x0501</span></span>  | <span data-ttu-id="00d02-214">La aplicación es compatible con ComCtl32.dll versión 5,81 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-214">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="00d02-215">La aplicación no puede implementar características que se agregaron después de la versión 5,81.</span><span class="sxs-lookup"><span data-stu-id="00d02-215">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="00d02-216">0x0600</span><span class="sxs-lookup"><span data-stu-id="00d02-216">0x0600</span></span>  | <span data-ttu-id="00d02-217">La aplicación es compatible con ComCtl32.dll versión 6,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00d02-217">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="00d02-218">La aplicación no puede implementar características que se agregaron después de la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="00d02-218">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="00d02-219">Si no define la macro de **\_ \_ IE de Win32** en el proyecto, se define automáticamente como 0x0500.</span><span class="sxs-lookup"><span data-stu-id="00d02-219">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="00d02-220">Para definir un valor diferente, puede agregar lo siguiente a las directivas de compilador en el archivo make; Sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="00d02-220">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="00d02-221">Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado del shell.</span><span class="sxs-lookup"><span data-stu-id="00d02-221">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="00d02-222">Sustituya el número de versión deseado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="00d02-222">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="00d02-223">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00d02-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00d02-224">Acerca de los controles comunes</span><span class="sxs-lookup"><span data-stu-id="00d02-224">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 