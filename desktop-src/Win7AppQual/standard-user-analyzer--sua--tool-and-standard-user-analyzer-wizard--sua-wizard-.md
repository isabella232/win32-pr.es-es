---
description: Aprenda a usar la herramienta de analizador de usuario estándar (SUA) y el Asistente de SUA para probar sus aplicaciones y detectar posibles problemas de compatibilidad.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc0e729c37ff1650f0dab7f3dd1c05ffb4b5f370
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104083528"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="2ea6e-103">Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)</span><span class="sxs-lookup"><span data-stu-id="2ea6e-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="2ea6e-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="2ea6e-104">Affected Platforms</span></span>

<span data-ttu-id="2ea6e-105">**Clientes:** Windows XP Windows \| vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="2ea6e-105">**Clients:** Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="2ea6e-106">**Servidores:** Windows Server 2003 \| Windows server 2008 \| windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ea6e-106">**Servers:** Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="2ea6e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea6e-107">Description</span></span>

<span data-ttu-id="2ea6e-108">El kit de herramientas de compatibilidad de aplicaciones incluye la herramienta analizador de usuario estándar (SUA) y el Asistente para el analizador de usuarios estándar (Asistente para SUA).</span><span class="sxs-lookup"><span data-stu-id="2ea6e-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="2ea6e-109">Estas herramientas le permiten probar sus aplicaciones y supervisar las llamadas de API para detectar posibles problemas de compatibilidad debido a la característica control de cuentas de usuario (UAC) en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="2ea6e-110">UAC, anteriormente conocido como cuenta de usuario limitada (LUA), requiere que todos los usuarios (incluidos los miembros del grupo de administradores) se ejecuten como usuarios estándar mediante el cuadro de diálogo de mensaje de seguridad hasta que la aplicación se haya elevado deliberadamente.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="2ea6e-111">Sin embargo, las aplicaciones que requieren acceso y privilegios para ubicaciones que no están disponibles para un usuario estándar no se pueden ejecutar correctamente con el rol de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="2ea6e-112">Uso</span><span class="sxs-lookup"><span data-stu-id="2ea6e-112">Usage</span></span>

<span data-ttu-id="2ea6e-113">En las secciones siguientes se proporciona información detallada sobre cómo usar las herramientas del asistente SUA y SUA.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="2ea6e-114">**Herramienta SUA**</span><span class="sxs-lookup"><span data-stu-id="2ea6e-114">**SUA Tool**</span></span>

<span data-ttu-id="2ea6e-115">La herramienta SUA le permite analizar una aplicación, revisar un informe detallado sobre los problemas relacionados con UAC y, a continuación, aplicar las mitigaciones de la aplicación sugerida y seleccionada, tal como se muestra en el siguiente diagrama de flujo.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Diagrama que muestra el flujo de la herramienta S U A.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="2ea6e-117">*Herramienta SUA y virtualización*</span><span class="sxs-lookup"><span data-stu-id="2ea6e-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="2ea6e-118">Solo la herramienta SUA permite activar y desactivar la característica de virtualización.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="2ea6e-119">Al desactivar la característica de virtualización, la aplicación comprobada se comportará de la misma manera que cuando funciona en el sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="2ea6e-120">*Herramienta SUA y privilegios elevados*</span><span class="sxs-lookup"><span data-stu-id="2ea6e-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="2ea6e-121">Solo la herramienta SUA permite activar y desactivar la característica de **Inicio elevado** .</span><span class="sxs-lookup"><span data-stu-id="2ea6e-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="2ea6e-122">La característica de inicio elevado permite que la aplicación seleccionada se ejecute como administrador o como usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="2ea6e-123">En función de la selección, se localizarán diferentes tipos de problemas relacionados con UAC.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="2ea6e-124">Si desactiva la casilla **iniciar con privilegios elevados** , la aplicación se ejecutará con privilegios de administrador completos, lo que permite que sua prediga los problemas que pueden producirse para un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="2ea6e-125">Si activa la casilla iniciar con privilegios elevados, verá los errores resultantes de la aplicación que se ejecuta realmente y que generan errores.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="2ea6e-126">**Asistente para SUA**</span><span class="sxs-lookup"><span data-stu-id="2ea6e-126">**SUA Wizard**</span></span>

<span data-ttu-id="2ea6e-127">El Asistente para SUA le permite seguir un proceso guiado paso a paso por el que puede analizar una aplicación y, a continuación, aplicar las mitigaciones de la aplicación sugerida y seleccionada, tal como se muestra en el siguiente diagrama de flujo.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="2ea6e-128">A diferencia de la herramienta SUA, el asistente no permite revisar los problemas detallados relacionados con UAC.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Diagrama que muestra el flujo del asistente S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="2ea6e-130">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="2ea6e-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="2ea6e-131">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2ea6e-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="2ea6e-132">[Descripción de las herramientas del analizador de usuario estándar](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ea6e-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="2ea6e-133">[Referencia técnica del analizador de usuario estándar](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ea6e-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="2ea6e-134">[Prueba y mitigación de problemas con las herramientas de desarrollo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ea6e-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="2ea6e-135">Compatibilidad de aplicaciones y control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="2ea6e-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="2ea6e-136">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="2ea6e-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
