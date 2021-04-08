---
title: Uso de las funciones de configuración del monitor de Low-Level
description: Uso de las funciones de configuración del monitor de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- supervisión, funciones
- supervisión, funciones de configuración de bajo nivel
- monitor, DDC/CI
- supervisar, Mostrar la interfaz de comandos del canal de datos
- supervisión de la configuración y las funciones de configuración de bajo nivel
- supervisión de la configuración, funciones
- configuración de monitor, DDC/CI
- configuración de monitor, Mostrar interfaz de comandos de canal de datos
- funciones de configuración de bajo nivel
- Mostrar interfaz de comandos del canal de datos
- DDC/CI
- Conjunto de comandos de control de monitor VESA (MCCS)
- Conjunto de comandos de control de supervisión (MCCS)
- MCCS (conjunto de comandos de control de monitor)
- Panel de control virtual (VCP)
- VCP (panel de control virtual)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995199"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="9aa0a-119">Uso de las funciones de configuración del monitor de Low-Level</span><span class="sxs-lookup"><span data-stu-id="9aa0a-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="9aa0a-120">Antes de usar las funciones de configuración del monitor de bajo nivel, debe estar familiarizado con estos estándares:</span><span class="sxs-lookup"><span data-stu-id="9aa0a-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="9aa0a-121">Mostrar la interfaz de comandos del canal de datos (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="9aa0a-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="9aa0a-122">Conjunto de comandos de control de monitor VESA (MCCS)</span><span class="sxs-lookup"><span data-stu-id="9aa0a-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="9aa0a-123">Las funciones de bajo nivel funcionan al obtener y establecer los valores de los códigos del panel de control virtual (VCP).</span><span class="sxs-lookup"><span data-stu-id="9aa0a-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="9aa0a-124">Un código VCP puede ser *continuo* o no *continuo*.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="9aa0a-125">Los códigos continuos pueden suponer cualquier valor entre cero y un valor máximo específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="9aa0a-126">Los códigos no continuos admiten un conjunto definido de valores, que también es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="9aa0a-127">Para usar las funciones de configuración del monitor de bajo nivel, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9aa0a-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="9aa0a-128">Obtenga un identificador **HMONITOR** llamando a [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span><span class="sxs-lookup"><span data-stu-id="9aa0a-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="9aa0a-129">Llame a [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) para obtener el número de monitores físicos asociados al identificador de **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="9aa0a-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="9aa0a-130">Llame a [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) para obtener una lista de identificadores para los monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="9aa0a-131">Llame a [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) para obtener la longitud de la cadena de funcionalidades DDC/CI de un monitor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="9aa0a-132">La cadena Capabilities es una cadena ASCII que contiene información estática sobre el monitor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="9aa0a-133">Una parte de la cadena muestra los códigos VCP que admite el monitor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="9aa0a-134">La cadena también muestra los valores admitidos de los códigos VCP no continuos.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="9aa0a-135">Asigne un búfer para que contenga la cadena de funcionalidades y llame a [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obtener la cadena.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="9aa0a-136">Analice la cadena de funciones para determinar qué códigos VCP admite el monitor.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="9aa0a-137">Para un código VCP continuo, llame a [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obtener los valores actuales y máximos del código.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="9aa0a-138">En el caso de un código VCP no continuo, analice la cadena de funcionalidades para obtener los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="9aa0a-139">Llame a [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para establecer un nuevo valor para un código VCP.</span><span class="sxs-lookup"><span data-stu-id="9aa0a-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aa0a-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9aa0a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa0a-141">**Uso de la configuración de monitor**</span><span class="sxs-lookup"><span data-stu-id="9aa0a-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 