---
title: Acerca de la actualización de la plataforma para Windows Vista
description: Proporciona información general sobre la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 y sus características.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Actualización de la plataforma para Windows Server 2008
- Actualización de la plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707639"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="8f257-105">Acerca de la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="8f257-106">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 son actualizaciones del sistema operativo del usuario final que admiten el uso de las tecnologías de Windows 7 seleccionadas en versiones anteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="8f257-107">Las actualizaciones incluyen un conjunto de bibliotecas en tiempo de ejecución que permiten a los desarrolladores de aplicaciones tener como destino las versiones actuales, Windows 7 y Windows Server 2008 R2, así como las versiones anteriores, Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="8f257-108">Resumen de API admitidas por tecnología</span><span class="sxs-lookup"><span data-stu-id="8f257-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="8f257-109">Cada tecnología compatible con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para las actualizaciones de Windows Server 2008 incluye un conjunto de API que se puede usar en una aplicación que tiene como destino la versión anterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="8f257-110">Para obtener más información sobre el uso de las API admitidas por las actualizaciones en una aplicación que tiene como destino versiones anteriores de Windows, consulte [desarrollo de aplicaciones para versiones anteriores de Windows](developing-applications-for-previous-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="8f257-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f257-111">Algunas API que están asociadas a una tecnología pueden no admitirse y el comportamiento, el rendimiento o los requisitos de algunas de las API admitidas pueden variar en función de las versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="8f257-112">Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.</span><span class="sxs-lookup"><span data-stu-id="8f257-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="8f257-113">Tecnologías compatibles con la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="8f257-114">Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.</span><span class="sxs-lookup"><span data-stu-id="8f257-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="8f257-115">En la tabla siguiente se muestran las tecnologías compatibles con Windows Vista y Windows XP con la actualización de la plataforma para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f257-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="8f257-116">Technology</span><span class="sxs-lookup"><span data-stu-id="8f257-116">Technology</span></span>                                                                                    | <span data-ttu-id="8f257-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-117">Windows Vista</span></span> | <span data-ttu-id="8f257-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f257-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="8f257-119">API de automatización de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="8f257-120">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-120">Yes</span></span>           | <span data-ttu-id="8f257-121">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-121">Yes</span></span>        |
| [<span data-ttu-id="8f257-122">Biblioteca de gráficos de Windows, de imágenes y XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="8f257-123">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-123">Yes</span></span>           | <span data-ttu-id="8f257-124">No</span><span class="sxs-lookup"><span data-stu-id="8f257-124">No</span></span>         |
| [<span data-ttu-id="8f257-125">Cinta de Windows y biblioteca del administrador de animaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="8f257-126">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-126">Yes</span></span>           | <span data-ttu-id="8f257-127">No</span><span class="sxs-lookup"><span data-stu-id="8f257-127">No</span></span>         |
| [<span data-ttu-id="8f257-128">Plataforma de dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="8f257-129">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-129">Yes</span></span>           | <span data-ttu-id="8f257-130">No</span><span class="sxs-lookup"><span data-stu-id="8f257-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="8f257-131">Tecnologías compatibles con la actualización de la plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f257-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="8f257-132">Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.</span><span class="sxs-lookup"><span data-stu-id="8f257-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="8f257-133">En la tabla siguiente se muestran las tecnologías compatibles con Windows Server 2008 y Windows Server 2003 con la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="8f257-134">Technology</span><span class="sxs-lookup"><span data-stu-id="8f257-134">Technology</span></span>                                                                                    | <span data-ttu-id="8f257-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f257-135">Windows Server 2008</span></span> | <span data-ttu-id="8f257-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f257-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="8f257-137">API de automatización de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="8f257-138">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-138">Yes</span></span>                 | <span data-ttu-id="8f257-139">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-139">Yes</span></span>                 |
| [<span data-ttu-id="8f257-140">Biblioteca de gráficos de Windows, de imágenes y XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="8f257-141">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-141">Yes</span></span>                 | <span data-ttu-id="8f257-142">No</span><span class="sxs-lookup"><span data-stu-id="8f257-142">No</span></span>                  |
| [<span data-ttu-id="8f257-143">Cinta de Windows y biblioteca del administrador de animaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="8f257-144">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-144">Yes</span></span>                 | <span data-ttu-id="8f257-145">No</span><span class="sxs-lookup"><span data-stu-id="8f257-145">No</span></span>                  |
| [<span data-ttu-id="8f257-146">Plataforma de dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="8f257-147">No</span><span class="sxs-lookup"><span data-stu-id="8f257-147">No</span></span>                  | <span data-ttu-id="8f257-148">No</span><span class="sxs-lookup"><span data-stu-id="8f257-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="8f257-149">Descripciones de API admitidas por tecnología</span><span class="sxs-lookup"><span data-stu-id="8f257-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="8f257-150">Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.</span><span class="sxs-lookup"><span data-stu-id="8f257-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="8f257-151">API de automatización de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="8f257-152">Biblioteca de gráficos de Windows, de imágenes y XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="8f257-153">Cinta de Windows y biblioteca del administrador de animaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="8f257-154">Plataforma de dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="8f257-155">API de automatización de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-155">Windows Automation API</span></span>

<span data-ttu-id="8f257-156">Windows Automation API 3,0 es un conjunto de archivos dll y elementos de API que permiten a los productos de tecnología de asistencia (AT) proporcionar un mejor acceso al equipo para usuarios que tienen dificultades físicas o cognitivas, deficiencias o discapacidades.</span><span class="sxs-lookup"><span data-stu-id="8f257-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="8f257-157">Además, dado que la API de Windows Automation 3,0 permite a las aplicaciones tener acceso a los elementos de la interfaz de usuario (UI) de otras aplicaciones y manipularlos, es una tecnología ideal para implementar herramientas de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="8f257-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="8f257-158">Microsoft Active Accessibility (MSAA) y la automatización de la interfaz de usuario son similares en que ambos proporcionan un medio para exponer y recopilar información sobre los elementos y controles de la interfaz de usuario para admitir la automatización de la prueba de software y la accesibilidad de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f257-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="8f257-159">La automatización de la interfaz de usuario es una implementación de Windows de la especificación de UI Automation.</span><span class="sxs-lookup"><span data-stu-id="8f257-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="8f257-160">Se trata de una tecnología más reciente que aborda muchas de las limitaciones de MSAA.</span><span class="sxs-lookup"><span data-stu-id="8f257-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="8f257-161">Para obtener más información sobre la API de Windows Automation 3,0, consulte [API de Windows Automation: información general](/windows/desktop/WinAuto/windows-automation-api-overview).</span><span class="sxs-lookup"><span data-stu-id="8f257-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="8f257-162">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 admiten la siguiente API de automatización de Windows 3,0:</span><span class="sxs-lookup"><span data-stu-id="8f257-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="8f257-163">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="8f257-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="8f257-164">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="8f257-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="8f257-165">Ediciones de Windows válidas para las actualizaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="8f257-166">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con la API de Windows Automation 3,0 en las ediciones de Windows que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f257-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8f257-167">Versión de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-167">Windows Version</span></span></th>
<th><span data-ttu-id="8f257-168">Ediciones válidas para la actualización</span><span class="sxs-lookup"><span data-stu-id="8f257-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f257-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="8f257-170">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="8f257-171">Home Basic con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-172">Home Premium con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-173">Empresa con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-174">Enterprise con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-175">Ultimate con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f257-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f257-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="8f257-177">Windows XP Home con SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="8f257-178">Windows XP Professional con SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f257-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f257-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="8f257-180">Windows Server 2008 con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f257-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f257-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="8f257-182">Windows Server 2003 con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="8f257-183">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="8f257-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="8f257-184">Microsoft Active Accessibility (MSAA) es una tecnología heredada que se presentó por primera vez con Windows 95.</span><span class="sxs-lookup"><span data-stu-id="8f257-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="8f257-185">Es un conjunto de API que mejora la forma en que los productos de tecnología de asistencia (AT) funcionan con las aplicaciones que se ejecutan en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="8f257-186">La API proporciona interfaces y métodos de programación para exponer información sobre los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f257-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="8f257-187">Para obtener más información acerca de Microsoft Active Accessibility, consulte la [información técnica](/windows/desktop/WinAuto/technical-overview).</span><span class="sxs-lookup"><span data-stu-id="8f257-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="8f257-188">Elementos de la API de Microsoft Active Accessibility admitidos</span><span class="sxs-lookup"><span data-stu-id="8f257-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="8f257-189">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="8f257-190">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="8f257-190">UI Automation</span></span>

<span data-ttu-id="8f257-191">La automatización de la interfaz de usuario es una tecnología más reciente que implementa la especificación de automatización de la interfaz de usuario y aborda muchas de las limitaciones de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="8f257-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="8f257-192">Es un conjunto de API que proporciona acceso mediante programación a los elementos de la interfaz de usuario de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8f257-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="8f257-193">La API proporcionada ayuda a los productos de tecnología de asistencia y a las herramientas de pruebas automatizadas a obtener acceso, identificar y manipular los elementos de interfaz de usuario estándar y personalizados de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f257-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="8f257-194">Para obtener más información sobre la automatización de la interfaz de usuario, consulte [API de automatización de Windows: UI Automation](../winauto/entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="8f257-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="8f257-195">Elementos de API de automatización de la interfaz de usuario admitidos</span><span class="sxs-lookup"><span data-stu-id="8f257-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="8f257-196">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="8f257-197">Ejecutar automatización de la interfaz de usuario en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="8f257-198">Debido a las diferencias en la forma en que los controles comunes y los controles estándar de Windows se implementan en distintas versiones de Windows, pueden existir ligeras diferencias en la información que los proxies de automatización de la interfaz de usuario recuperan para estos controles de una versión a otra.</span><span class="sxs-lookup"><span data-stu-id="8f257-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="8f257-199">Biblioteca de gráficos de Windows, de imágenes y XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="8f257-200">La actualización de la plataforma para Windows Vista admite las siguientes API de Windows 7 de la biblioteca de gráficos, imágenes y XPS de Windows:</span><span class="sxs-lookup"><span data-stu-id="8f257-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="8f257-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f257-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="8f257-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="8f257-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="8f257-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8f257-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="8f257-204">Packaging</span><span class="sxs-lookup"><span data-stu-id="8f257-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="8f257-205">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="8f257-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="8f257-206">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="8f257-207">Impresión XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="8f257-208">Ediciones de Windows válidas para las actualizaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="8f257-209">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con gráficos, imágenes y biblioteca XPS de Windows en las ediciones de Windows que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f257-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8f257-210">Versión de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-210">Windows Version</span></span></th>
<th><span data-ttu-id="8f257-211">Ediciones válidas para la actualización</span><span class="sxs-lookup"><span data-stu-id="8f257-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f257-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="8f257-213">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="8f257-214">Home Basic con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-215">Home Premium con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-216">Empresa con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-217">Enterprise con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-218">Ultimate con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f257-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f257-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="8f257-220">Windows Server 2008 con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="8f257-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f257-221">Direct2D</span></span>

<span data-ttu-id="8f257-222">La API de Direct2D es una nueva API de gráficos 2D de modo inmediato y con aceleración de hardware que proporciona alto rendimiento y representación de alta calidad para la geometría 2D, los mapas de bits y el texto.</span><span class="sxs-lookup"><span data-stu-id="8f257-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="8f257-223">La API de Direct2D está diseñada para interoperar bien con el código existente que usa GDI, GDI+ o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8f257-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="8f257-224">Para obtener más información sobre Direct2D, consulte [acerca de direct2d](/windows/desktop/Direct2D/direct2d-overview).</span><span class="sxs-lookup"><span data-stu-id="8f257-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="8f257-225">Elementos compatibles de la API de Direct2D</span><span class="sxs-lookup"><span data-stu-id="8f257-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="8f257-226">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="8f257-227">Ejecutar Direct2D en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="8f257-228">Si falta el controlador WDDM 1,1 en Windows Vista, el rendimiento de la interoperabilidad de Direct2D/GDI disminuye.</span><span class="sxs-lookup"><span data-stu-id="8f257-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="8f257-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="8f257-229">Direct3D</span></span>

<span data-ttu-id="8f257-230">La actualización de la plataforma para Windows Vista proporciona compatibilidad con la superficie de BGRA para las rutas de acceso de código de Direct3D10 y Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="8f257-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="8f257-231">Direct3D10Level9 permite que la funcionalidad de Direct3D10 funcione en el hardware de Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="8f257-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="8f257-232">Direct3D WARP10 es un rasterizador de software con rendimiento para aplicaciones de Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="8f257-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="8f257-233">Direct3D 11, la versión más reciente de Direct3D, proporciona nuevas funcionalidades, como compatibilidad mejorada con multithreading, Teselación, funcionalidad de DirectCompute y vinculación dinámica de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8f257-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="8f257-234">Si crea aplicaciones que usan Direct3D, el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) es obligatorio).</span><span class="sxs-lookup"><span data-stu-id="8f257-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="8f257-235">Para obtener más información sobre Direct3D, vea [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f257-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="8f257-236">Elementos compatibles de la API de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8f257-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="8f257-237">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="8f257-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8f257-238">DirectWrite</span></span>

<span data-ttu-id="8f257-239">La API de DirectWrite es una nueva API de texto que proporciona varios niveles de funcionalidad, como el diseño de texto, el procesamiento de scripts, la representación de glifos y el sistema de fuentes.</span><span class="sxs-lookup"><span data-stu-id="8f257-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="8f257-240">DirectWrite usa fuentes OpenType y representación de ClearType de subpíxeles para mejorar la experiencia de texto que proporcionan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8f257-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="8f257-241">La representación de texto se acelera por hardware cuando se usa con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8f257-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="8f257-242">Para obtener más información sobre DirectWrite, consulte [Introducción a directwrite](/windows/desktop/DirectWrite/introducing-directwrite).</span><span class="sxs-lookup"><span data-stu-id="8f257-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="8f257-243">Elementos compatibles de la API de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8f257-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="8f257-244">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="8f257-245">Ejecución de DirectWrite en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="8f257-246">Los siguientes problemas de comportamiento pueden afectar al uso de la API de DirectWrite en versiones anteriores de Windows:</span><span class="sxs-lookup"><span data-stu-id="8f257-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="8f257-247">Es posible que los scripts nuevos en Windows 7 no se representen correctamente en las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="8f257-248">Las configuraciones regionales que no están disponibles en versiones anteriores de Windows revierten al comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f257-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="8f257-249">El sintonizador ClearType no está disponible en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="8f257-250">La interoperabilidad de GDI tiene un costo de memoria mayor en algunos escenarios en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="8f257-251">Packaging</span><span class="sxs-lookup"><span data-stu-id="8f257-251">Packaging</span></span>

<span data-ttu-id="8f257-252">La actualización de la plataforma para Windows Vista admite un subconjunto limitado de las API de empaquetado que se necesitan para realizar tareas con la API de documentos XPS en aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="8f257-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="8f257-253">Para obtener más información sobre las API de empaquetado, consulte la [Introducción a la API de empaquetado](/previous-versions/windows/desktop/opc/packaging-api-overview).</span><span class="sxs-lookup"><span data-stu-id="8f257-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="8f257-254">Elementos de la API de empaquetado compatibles</span><span class="sxs-lookup"><span data-stu-id="8f257-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="8f257-255">Solo se admiten las siguientes interfaces de empaquetado:</span><span class="sxs-lookup"><span data-stu-id="8f257-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="8f257-256">IOpcUri</span><span class="sxs-lookup"><span data-stu-id="8f257-256">IOpcUri</span></span>
-   <span data-ttu-id="8f257-257">IOpcPartUri</span><span class="sxs-lookup"><span data-stu-id="8f257-257">IOpcPartUri</span></span>
-   <span data-ttu-id="8f257-258">IOpcFactory (solo se admiten los siguientes métodos)</span><span class="sxs-lookup"><span data-stu-id="8f257-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="8f257-259">CreatePackageRootUri</span><span class="sxs-lookup"><span data-stu-id="8f257-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="8f257-260">CreatePartUri</span><span class="sxs-lookup"><span data-stu-id="8f257-260">CreatePartUri</span></span>
    -   <span data-ttu-id="8f257-261">CreateStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="8f257-261">CreateStreamOnFile</span></span>

<span data-ttu-id="8f257-262">Las API de empaquetado compatibles se pueden usar para crear transmisiones a través de archivos, así como para crear e interactuar con el URI basado en paquetes.</span><span class="sxs-lookup"><span data-stu-id="8f257-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="8f257-263">Ejecutar la API de empaquetado en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="8f257-264">El comportamiento y el rendimiento de las interfaces de empaquetado y métodos admitidos son los mismos en todas las plataformas compatibles.</span><span class="sxs-lookup"><span data-stu-id="8f257-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="8f257-265">Si una aplicación intenta crear una instancia o llamar a un método o una interfaz de empaquetado no admitidos, se producirá un error en el intento.</span><span class="sxs-lookup"><span data-stu-id="8f257-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="8f257-266">Si la llamada se realiza a un método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) no compatible, se \_ devolverá el código de error E NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8f257-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="8f257-267">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="8f257-267">Windows Imaging Component</span></span>

<span data-ttu-id="8f257-268">Entre las nuevas características del componente de creación de imágenes de Windows (WIC) se incluyen la seguridad mejorada, la compatibilidad con alto color y una mejor interoperabilidad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="8f257-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="8f257-269">Además, el componente de creación de imágenes de Windows amplía su compatibilidad con estándares proporcionando compatibilidad para descodificación progresiva de imágenes, características de PNG expandidas, metadatos GIF, actualizaciones fotográficas de HD y metadatos que abarcan segmentos APPn.</span><span class="sxs-lookup"><span data-stu-id="8f257-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="8f257-270">Para obtener más información sobre el componente de creación de imágenes de Windows, vea [información general](/windows/desktop/wic/-wic-about-windows-imaging-codec)sobre el componente de creación de imágenes de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="8f257-271">Elementos de la API de WIC compatibles</span><span class="sxs-lookup"><span data-stu-id="8f257-271">Supported WIC API Elements</span></span>

<span data-ttu-id="8f257-272">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="8f257-273">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-273">XPS Document</span></span>

<span data-ttu-id="8f257-274">Las API de documentos XPS admiten la creación, modificación y guardado de documentos XPS en aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="8f257-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="8f257-275">Para obtener más información acerca de las API de documentos XPS, consulte la [Guía de programación de documentos XPS.](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f257-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="8f257-276">Elementos compatibles de la API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="8f257-277">Solo las interfaces de [firmas digitales XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) no se admiten en las versiones de sistema operativo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="8f257-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="8f257-278">Impresión XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-278">XPS Print</span></span>

<span data-ttu-id="8f257-279">Las API de impresión XPS admiten la impresión de documentos XPS desde aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="8f257-280">Para obtener más información acerca de las API de impresión XPS, consulte la [API de XpsPrint](/windows/desktop/printdocs/xpsprint-api).</span><span class="sxs-lookup"><span data-stu-id="8f257-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="8f257-281">Elementos admitidos de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="8f257-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="8f257-282">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="8f257-283">Cinta de Windows y biblioteca del administrador de animaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="8f257-284">La actualización de la plataforma para Windows Vista admite las siguientes API de Windows 7 desde la cinta de Windows y la biblioteca de animaciones:</span><span class="sxs-lookup"><span data-stu-id="8f257-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="8f257-285">Marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="8f257-286">Administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="8f257-287">Ediciones de Windows válidas para las actualizaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="8f257-288">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con la cinta y la biblioteca del administrador de animaciones de Windows en las ediciones de Windows que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f257-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8f257-289">Versión de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-289">Windows Version</span></span></th>
<th><span data-ttu-id="8f257-290">Ediciones válidas para la actualización</span><span class="sxs-lookup"><span data-stu-id="8f257-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f257-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="8f257-292">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="8f257-293">Home Basic con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-294">Home Premium con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-295">Empresa con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-296">Enterprise con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-297">Ultimate con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f257-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f257-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="8f257-299">Windows Server 2008 con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="8f257-300">Marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="8f257-301">El marco de cinta de Windows (cinta) es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.</span><span class="sxs-lookup"><span data-stu-id="8f257-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="8f257-302">El marco de trabajo es una colección de API de Microsoft Win32 que proporciona un host de nuevas capacidades de interfaz de usuario para los desarrolladores de Windows e incluye la cinta de opciones y un sistema de menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="8f257-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="8f257-303">Para obtener más información sobre el marco de la cinta de opciones, vea [Introducción al marco de cinta de Windows](../windowsribbon/windowsribbon-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="8f257-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="8f257-304">Elementos de API del marco de cinta admitidos</span><span class="sxs-lookup"><span data-stu-id="8f257-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="8f257-305">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="8f257-306">Administrador de animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-306">Windows Animation Manager</span></span>

<span data-ttu-id="8f257-307">El administrador de animaciones de Windows (animación de Windows) es una interfaz de programación que admite la animación de elementos visuales de aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="8f257-308">La animación de Windows está diseñada para simplificar el desarrollo y el mantenimiento de las secuencias de animación y para permitir que los desarrolladores implementen animaciones coherentes e intuitivas.</span><span class="sxs-lookup"><span data-stu-id="8f257-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="8f257-309">La animación de Windows se puede usar con cualquier plataforma de gráficos, como Direct2D, Direct3D o GDI+.</span><span class="sxs-lookup"><span data-stu-id="8f257-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="8f257-310">Windows Animation es una API de un solo subproceso que proporciona todo lo que un desarrollador necesita para crear, administrar y controlar la animación de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f257-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="8f257-311">Para obtener más información sobre el administrador de animaciones de Windows, vea Introducción a la [animación de Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span><span class="sxs-lookup"><span data-stu-id="8f257-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="8f257-312">Elementos de API del administrador de animaciones admitidos</span><span class="sxs-lookup"><span data-stu-id="8f257-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="8f257-313">Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f257-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="8f257-314">Plataforma de dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="8f257-315">La actualización de la plataforma para Windows Vista es compatible con las extensiones de Windows 7 para la plataforma de dispositivos portátiles de Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="8f257-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="8f257-316">Esta característica permite que los equipos se comuniquen con los medios y dispositivos de almacenamiento conectados.</span><span class="sxs-lookup"><span data-stu-id="8f257-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="8f257-317">WPD proporciona una forma flexible y robusta de que los equipos se comuniquen con cámaras digitales, reproductores de música, teléfonos móviles y muchos otros tipos de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="8f257-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="8f257-318">Para obtener más información acerca de los dispositivos portátiles de Windows, consulte [dispositivos portátiles de Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .</span><span class="sxs-lookup"><span data-stu-id="8f257-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="8f257-319">Ediciones de Windows válidas para las actualizaciones</span><span class="sxs-lookup"><span data-stu-id="8f257-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="8f257-320">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con dispositivos portátiles de Windows (WPD) en las ediciones de Windows que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f257-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8f257-321">Versión de Windows</span><span class="sxs-lookup"><span data-stu-id="8f257-321">Windows Version</span></span></th>
<th><span data-ttu-id="8f257-322">Ediciones válidas para la actualización</span><span class="sxs-lookup"><span data-stu-id="8f257-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f257-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="8f257-324">Starter con SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="8f257-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="8f257-325">Home Basic con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-326">Home Premium con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-327">Empresa con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-328">Enterprise con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="8f257-329">Ultimate con SP2 (x86 y AMD64)</span><span class="sxs-lookup"><span data-stu-id="8f257-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="8f257-330">Elementos compatibles de la API de WPD</span><span class="sxs-lookup"><span data-stu-id="8f257-330">Supported WPD API Elements</span></span>

<span data-ttu-id="8f257-331">En la tabla siguiente se identifican las características compatibles con las versiones de Windows 7, Windows Vista y Windows Vista con actualización de plataforma para Windows Vista del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8f257-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="8f257-332">Característica de WPD</span><span class="sxs-lookup"><span data-stu-id="8f257-332">WPD Feature</span></span>                    | <span data-ttu-id="8f257-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f257-333">Windows 7</span></span> | <span data-ttu-id="8f257-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-334">Windows Vista</span></span> | <span data-ttu-id="8f257-335">Windows Vista con actualización de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="8f257-336">MTP a través de USB</span><span class="sxs-lookup"><span data-stu-id="8f257-336">MTP over USB</span></span>                   | <span data-ttu-id="8f257-337">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-337">Yes</span></span>       | <span data-ttu-id="8f257-338">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-338">Yes</span></span>           | <span data-ttu-id="8f257-339">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-339">Yes</span></span>                                                  |
| <span data-ttu-id="8f257-340">MTP a través de IP</span><span class="sxs-lookup"><span data-stu-id="8f257-340">MTP over IP</span></span>                    | <span data-ttu-id="8f257-341">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-341">Yes</span></span>       | <span data-ttu-id="8f257-342">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-342">Yes</span></span>           | <span data-ttu-id="8f257-343">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-343">Yes</span></span>                                                  |
| <span data-ttu-id="8f257-344">MTP a través de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="8f257-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="8f257-345">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-345">Yes</span></span>       | <span data-ttu-id="8f257-346">No</span><span class="sxs-lookup"><span data-stu-id="8f257-346">No</span></span>            | <span data-ttu-id="8f257-347">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-347">Yes</span></span>                                                  |
| <span data-ttu-id="8f257-348">WPD y servicios de dispositivos MTP</span><span class="sxs-lookup"><span data-stu-id="8f257-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="8f257-349">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-349">Yes</span></span>       | <span data-ttu-id="8f257-350">No</span><span class="sxs-lookup"><span data-stu-id="8f257-350">No</span></span>            | <span data-ttu-id="8f257-351">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-351">Yes</span></span>                                                  |
| <span data-ttu-id="8f257-352">Automatización de WPD</span><span class="sxs-lookup"><span data-stu-id="8f257-352">WPD Automation</span></span>                 | <span data-ttu-id="8f257-353">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-353">Yes</span></span>       | <span data-ttu-id="8f257-354">No</span><span class="sxs-lookup"><span data-stu-id="8f257-354">No</span></span>            | <span data-ttu-id="8f257-355">No</span><span class="sxs-lookup"><span data-stu-id="8f257-355">No</span></span>                                                   |
| <span data-ttu-id="8f257-356">Múltiples funciones/transporte múltiple</span><span class="sxs-lookup"><span data-stu-id="8f257-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="8f257-357">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-357">Yes</span></span>       | <span data-ttu-id="8f257-358">No</span><span class="sxs-lookup"><span data-stu-id="8f257-358">No</span></span>            | <span data-ttu-id="8f257-359">No</span><span class="sxs-lookup"><span data-stu-id="8f257-359">No</span></span>                                                   |
| <span data-ttu-id="8f257-360">Device Stage (puede estar en inglés)</span><span class="sxs-lookup"><span data-stu-id="8f257-360">Device Stage</span></span>                   | <span data-ttu-id="8f257-361">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-361">Yes</span></span>       | <span data-ttu-id="8f257-362">No</span><span class="sxs-lookup"><span data-stu-id="8f257-362">No</span></span>            | <span data-ttu-id="8f257-363">No</span><span class="sxs-lookup"><span data-stu-id="8f257-363">No</span></span>                                                   |
| <span data-ttu-id="8f257-364">Plataforma de sincronización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="8f257-364">Device Sync Platform</span></span>           | <span data-ttu-id="8f257-365">Sí</span><span class="sxs-lookup"><span data-stu-id="8f257-365">Yes</span></span>       | <span data-ttu-id="8f257-366">No</span><span class="sxs-lookup"><span data-stu-id="8f257-366">No</span></span>            | <span data-ttu-id="8f257-367">No</span><span class="sxs-lookup"><span data-stu-id="8f257-367">No</span></span>                                                   |



 

<span data-ttu-id="8f257-368">En el caso de las ediciones de Windows 7 y Windows Vista que no tienen Microsoft Windows Media Player instalado de forma predeterminada (las ediciones N y KN), debe instalar el [SDK de Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) para habilitar la funcionalidad de WPD).</span><span class="sxs-lookup"><span data-stu-id="8f257-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="8f257-369">Para obtener más información, vea el [artículo de Knowledge Base](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , que se publicó originalmente como una solución para Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="8f257-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f257-370">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f257-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f257-371">Actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="8f257-372">**Temas de introducción**</span><span class="sxs-lookup"><span data-stu-id="8f257-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="8f257-373">Acerca de la actualización de la plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f257-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="8f257-374">Artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="8f257-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 