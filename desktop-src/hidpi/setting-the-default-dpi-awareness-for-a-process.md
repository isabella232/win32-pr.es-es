---
description: Más información acerca de cómo establecer el reconocimiento de PPP predeterminado para un proceso
title: Establecer el reconocimiento de PPP predeterminado para un proceso (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721388"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="c2a3c-103">Establecer el reconocimiento de PPP predeterminado para un proceso</span><span class="sxs-lookup"><span data-stu-id="c2a3c-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="c2a3c-104">Las aplicaciones de escritorio en Windows se pueden ejecutar en diferentes modos de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="c2a3c-105">Estos modos permiten un comportamiento de escalado de PPP distinto y pueden usar diferentes espacios de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="c2a3c-106">Para obtener más información sobre el reconocimiento de PPP, consulte [desarrollo de aplicaciones de escritorio de PPP alta en Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="c2a3c-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="c2a3c-107">Es importante que establezca explícitamente el modo de reconocimiento de PPP predeterminado del proceso para evitar un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="c2a3c-108">Hay dos métodos principales para especificar el reconocimiento de PPP predeterminado de un proceso:</span><span class="sxs-lookup"><span data-stu-id="c2a3c-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="c2a3c-109">1 \) a través de una configuración de manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="c2a3c-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="c2a3c-110">2 mediante \) programación a través de una llamada API</span><span class="sxs-lookup"><span data-stu-id="c2a3c-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="c2a3c-111">Se recomienda especificar el reconocimiento de PPP de proceso predeterminado a través de un valor de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="c2a3c-112">Aunque se admite la especificación de la API Via predeterminada, no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="c2a3c-113">Establecer el reconocimiento predeterminado con el manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="c2a3c-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="c2a3c-114">Hay dos configuraciones de manifiesto que le permiten especificar el modo de reconocimiento de PPP predeterminado del proceso: \<dpiAwareness\> y \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="c2a3c-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="c2a3c-115">\<dpiAware\> se presentó en Windows Vista y solo permite que el proceso predeterminado se establezca en reconocimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="c2a3c-116">\<dpiAwareness\> se presentó en la versión 1607 de Windows 10 y permite especificar una lista ordenada de los modos de reconocimiento de PPP predeterminados del proceso.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="c2a3c-117">Esto le permite establecer los modos de reconocimiento de PPP de copia de seguridad, que se usarán si la aplicación se ejecuta en una versión de Windows que no sea compatible con el primer modo de reconocimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="c2a3c-118">En versiones anteriores de Windows, se \<dpiAwareness\> omitirá la etiqueta más reciente.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="c2a3c-119">Esto significa que puede usar ambos valores del manifiesto para habilitar un escenario en el que el proceso predeterminado podría ser el reconocimiento del sistema en una versión anterior de Windows mientras se Per-Monitor en versiones posteriores a Windows 10, versión 1607.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="c2a3c-120">En Windows 10, versión 1607 y en, el \<dpiAware\> valor se omite si el \<dpiAwareness\> elemento está presente.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="c2a3c-121">En la tabla siguiente se muestra cómo especificar los diferentes modos de reconocimiento de PPP predeterminados del proceso mediante los dos valores del manifiesto:</span><span class="sxs-lookup"><span data-stu-id="c2a3c-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2a3c-122">Modo de reconocimiento de PPP predeterminado del proceso</span><span class="sxs-lookup"><span data-stu-id="c2a3c-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="c2a3c-123">&lt;configuración de dpiAware &gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="c2a3c-124">&lt;&gt;configuración de dpiAwareness (Windows 10, versión 1607 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2a3c-125">consciente</span><span class="sxs-lookup"><span data-stu-id="c2a3c-125">unaware</span></span></td>
<td><p><span data-ttu-id="c2a3c-126">N/A (no hay ningún valor de dpiAware en el manifiesto)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="c2a3c-127">or</span><span class="sxs-lookup"><span data-stu-id="c2a3c-127">or</span></span></p>
<p><span data-ttu-id="c2a3c-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="c2a3c-129">&lt;dpiAwareness no &gt; compatible &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2a3c-130">Compatible con el sistema</span><span class="sxs-lookup"><span data-stu-id="c2a3c-130">System aware</span></span></td>
<td><span data-ttu-id="c2a3c-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="c2a3c-132">&lt;dpiAwareness &gt; del sistema &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2a3c-133">Por monitor</span><span class="sxs-lookup"><span data-stu-id="c2a3c-133">Per Monitor</span></span></td>
<td><span data-ttu-id="c2a3c-134">&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="c2a3c-135">&lt;dpiAwareness &gt; permonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2a3c-136">Por monitor V2</span><span class="sxs-lookup"><span data-stu-id="c2a3c-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="c2a3c-137">No compatible</span><span class="sxs-lookup"><span data-stu-id="c2a3c-137">Not supported</span></span></td>
<td><span data-ttu-id="c2a3c-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="c2a3c-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2a3c-139">En el ejemplo siguiente se muestra el \<dpiAwareness\> y la \<dpiAware\> configuración que se usa en el mismo archivo de manifiesto para configurar el comportamiento de reconocimiento de PPP de proceso predeterminado para diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="c2a3c-140">Establecer el reconocimiento predeterminado mediante programación</span><span class="sxs-lookup"><span data-stu-id="c2a3c-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="c2a3c-141">Aunque no se recomienda, es posible establecer el reconocimiento de PPP predeterminado mediante programación.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="c2a3c-142">Una vez que se ha creado una ventana (HWND) en el proceso, ya no se admite el cambio del modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="c2a3c-143">Si está configurando el modo de reconocimiento de PPP predeterminado del proceso mediante programación, debe llamar a la API correspondiente antes de que se haya creado cualquier HWND.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="c2a3c-144">Hay varias API que permiten especificar el reconocimiento de PPP predeterminado para el proceso.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="c2a3c-145">La API recomendada actual es [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), ya que las API anteriores ofrecen menos funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2a3c-146">API</span><span class="sxs-lookup"><span data-stu-id="c2a3c-146">API</span></span></th>
<th><span data-ttu-id="c2a3c-147">Versión mínima de Windows</span><span class="sxs-lookup"><span data-stu-id="c2a3c-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="c2a3c-148">PPP no compatible</span><span class="sxs-lookup"><span data-stu-id="c2a3c-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="c2a3c-149">Reconocimiento de PPP del sistema</span><span class="sxs-lookup"><span data-stu-id="c2a3c-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="c2a3c-150">Con reconocimiento de PPP por monitor</span><span class="sxs-lookup"><span data-stu-id="c2a3c-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2a3c-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span><span class="sxs-lookup"><span data-stu-id="c2a3c-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="c2a3c-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2a3c-152">Windows Vista</span></span></td>
<td><span data-ttu-id="c2a3c-153">N/D</span><span class="sxs-lookup"><span data-stu-id="c2a3c-153">N/A</span></span></td>
<td><span data-ttu-id="c2a3c-154">SetProcessDpiAware()</span><span class="sxs-lookup"><span data-stu-id="c2a3c-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="c2a3c-155">N/D</span><span class="sxs-lookup"><span data-stu-id="c2a3c-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2a3c-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2a3c-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="c2a3c-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2a3c-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="c2a3c-158">SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="c2a3c-159">SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="c2a3c-160">SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2a3c-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2a3c-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="c2a3c-162">Windows 10, versión 1607</span><span class="sxs-lookup"><span data-stu-id="c2a3c-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="c2a3c-163">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="c2a3c-164">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="c2a3c-165">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="c2a3c-166">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="c2a3c-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="c2a3c-167">Proceso: predeterminado frente a subproceso predeterminado</span><span class="sxs-lookup"><span data-stu-id="c2a3c-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="c2a3c-168">Este documento hace referencia a la configuración del reconocimiento de PPP predeterminado para el proceso.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="c2a3c-169">Esto se debe a que Windows 10 incorporó compatibilidad para ejecutar más de un modo de reconocimiento de PPP en un único proceso (antes de Windows 10, todo el proceso tuvo que ajustarse a un único modo de reconocimiento de PPP).</span><span class="sxs-lookup"><span data-stu-id="c2a3c-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="c2a3c-170">La compatibilidad con la ejecución de más de un modo de reconocimiento de PPP dentro de un proceso se conoce como "escala de PPP en modo mixto".</span><span class="sxs-lookup"><span data-stu-id="c2a3c-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="c2a3c-171">Al usar el ajuste de PPP en modo mixto dentro del proceso, cada ventana de nivel superior puede ejecutarse en un modo de reconocimiento de PPP que puede ser diferente del valor predeterminado del proceso.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="c2a3c-172">A menos que se especifique explícitamente, cada subproceso usará de forma predeterminada el valor predeterminado del proceso cuando se cree.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="c2a3c-173">Para obtener más información sobre el escalado de PPP en modo mixto, consulte el artículo sobre el [escalado de PPP en modo mixto](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="c2a3c-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
