---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: 'Internet Explorer 8: protección de ejecución de datos/NX'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf23ba40be518e3d4c1421012e6b46fdb7b5e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910593"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="7642b-103">Internet Explorer 8: protección de ejecución de datos/NX</span><span class="sxs-lookup"><span data-stu-id="7642b-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7642b-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="7642b-104">Affected Platforms</span></span>

 <span data-ttu-id="7642b-105">**Clientes** -Windows XP Windows \| vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="7642b-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="7642b-106">**Servidores** : windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7642b-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="7642b-107">Internet Explorer 8 habilitará la protección de DEP/NX cuando se ejecute en un sistema operativo con la Service Pack más reciente.</span><span class="sxs-lookup"><span data-stu-id="7642b-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="7642b-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 y Windows Server 2008 tienen DEP/NX habilitado de forma predeterminada en Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="7642b-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="7642b-109">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="7642b-109">Feature Impact</span></span>

<span data-ttu-id="7642b-110">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="7642b-110">**Severity** - Medium</span></span>  
<span data-ttu-id="7642b-111">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="7642b-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="7642b-112">Normalmente, cualquier aplicación que se ejecute en Internet Explorer y que no sea compatible con DEP/NX se bloqueará al iniciarse y no funcionará.</span><span class="sxs-lookup"><span data-stu-id="7642b-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="7642b-113">Es posible que Internet Explorer se bloquee al iniciar si se instalan complementos que no son compatibles con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7642b-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="7642b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7642b-114">Description</span></span>

<span data-ttu-id="7642b-115">DEP/NX es una característica de seguridad que ayuda a mitigar las vulnerabilidades relacionadas con la memoria.</span><span class="sxs-lookup"><span data-stu-id="7642b-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="7642b-116">A partir de Internet Explorer 8, todos los procesos de Internet Explorer habilitan la característica DEP/NX de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7642b-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7642b-117">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="7642b-117">Manifestation of Impact</span></span>

<span data-ttu-id="7642b-118">El kernel de Windows supervisa la ejecución de un programa.</span><span class="sxs-lookup"><span data-stu-id="7642b-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="7642b-119">Si el kernel detecta un intento de ejecutar código desde una página de memoria que no está marcada como ejecutable, el kernel detiene la ejecución del programa, lo que produce un "bloqueo".</span><span class="sxs-lookup"><span data-stu-id="7642b-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="7642b-120">Se trata de una medida de seguridad que ayuda a garantizar que las vulnerabilidades relacionadas con la memoria (por ejemplo, desbordamientos del búfer) en la aplicación no se puedan aprovechar para ejecutar código arbitrario.</span><span class="sxs-lookup"><span data-stu-id="7642b-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="7642b-121">Mitigación de End-User</span><span class="sxs-lookup"><span data-stu-id="7642b-121">End-User Mitigation</span></span>

-   <span data-ttu-id="7642b-122">Instale una versión posterior del complemento o marco que sea compatible con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7642b-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="7642b-123">Ejecute Internet Explorer con privilegios elevados como administrador y, a continuación, deshabilite DEP/NX mediante la casilla **Habilitar protección de memoria para ayudar a mitigar los ataques en línea** en la pestaña **Opciones**  /  **avanzadas** de Internet.</span><span class="sxs-lookup"><span data-stu-id="7642b-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="7642b-124">Solución para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="7642b-124">Developer Solution</span></span>

<span data-ttu-id="7642b-125">Compile aplicaciones con las versiones más recientes de los marcos de trabajo compatibles con DEP.</span><span class="sxs-lookup"><span data-stu-id="7642b-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="7642b-126">Aprovechar las capacidades de características</span><span class="sxs-lookup"><span data-stu-id="7642b-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="7642b-127">Use la opción del vinculador/NXCOMPAT para indicar la compatibilidad de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7642b-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="7642b-128">Opte por su código en otras defensas disponibles, como la defensa de pila (/GS), el control de excepciones seguro (/SafeSEH) y ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="7642b-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="7642b-129">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="7642b-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="7642b-130">Pruebe el código con DEP/NX habilitado mediante la última versión de Internet Explorer Publicada en Windows Vista SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7642b-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="7642b-131">Pruebe con Internet Explorer 7 en Windows Vista después de habilitar la opción DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7642b-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="7642b-132">Para habilitar DEP/NX para Internet Explorer 7, ejecute Internet Explorer como administrador y, después, active la casilla correspondiente en la pestaña Herramientas > opciones de Internet > avanzadas.</span><span class="sxs-lookup"><span data-stu-id="7642b-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="7642b-133">Ejecute la herramienta de prueba de compatibilidad de Internet Explorer (IECTT), que se proporciona con el kit de herramientas de compatibilidad de aplicaciones (ACT) para localizar cualquier posible problema debido a los cambios de DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7642b-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7642b-134">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="7642b-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="7642b-135">Internet Explorer 8 Security Part I: protección de memoria de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7642b-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="7642b-136">Prevención de ejecución de datos</span><span class="sxs-lookup"><span data-stu-id="7642b-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="7642b-137">Nuevas API de NX agregadas a Windows Vista SP1, Windows XP SP3 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7642b-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="7642b-138">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7642b-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="7642b-139">[Problemas conocidos de la característica de seguridad de Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="7642b-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
