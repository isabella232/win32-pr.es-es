---
description: Internet Explorer 8- Protección de ejecución de datos/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8- Protección de ejecución de datos/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088253"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="a164b-103">Internet Explorer 8- Protección de ejecución de datos/NX</span><span class="sxs-lookup"><span data-stu-id="a164b-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a164b-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="a164b-104">Affected Platforms</span></span>

 <span data-ttu-id="a164b-105">**Clientes:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a164b-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="a164b-106">**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a164b-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="a164b-107">Internet Explorer 8 habilitará la protección DEP/NX cuando se ejecute en un sistema operativo con el Service Pack más reciente.</span><span class="sxs-lookup"><span data-stu-id="a164b-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="a164b-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 y Windows Server 2008 tienen DEP/NX habilitado de forma predeterminada en Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="a164b-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="a164b-109">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="a164b-109">Feature Impact</span></span>

<span data-ttu-id="a164b-110">**Gravedad:** media</span><span class="sxs-lookup"><span data-stu-id="a164b-110">**Severity** - Medium</span></span>  
<span data-ttu-id="a164b-111">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="a164b-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="a164b-112">Normalmente, cualquier aplicación que se ejecute en Internet Explorer y no sea compatible con DEP/NX se bloqueará durante el inicio y no funcionará.</span><span class="sxs-lookup"><span data-stu-id="a164b-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="a164b-113">Internet Explorer pueden bloquearse al iniciarse si están instalados complementos que no son compatibles con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="a164b-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="a164b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a164b-114">Description</span></span>

<span data-ttu-id="a164b-115">DEP/NX es una característica de seguridad que ayuda a mitigar las vulnerabilidades relacionadas con la memoria.</span><span class="sxs-lookup"><span data-stu-id="a164b-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="a164b-116">A partir Internet Explorer 8, todos los Internet Explorer habilitan la característica DEP/NX de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a164b-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a164b-117">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="a164b-117">Manifestation of Impact</span></span>

<span data-ttu-id="a164b-118">El kernel de Windows supervisa la ejecución de un programa.</span><span class="sxs-lookup"><span data-stu-id="a164b-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="a164b-119">Si el kernel detecta un intento de ejecutar código desde una página de memoria que no está marcada como ejecutable, el kernel detiene la ejecución del programa, lo que produce un "bloqueo".</span><span class="sxs-lookup"><span data-stu-id="a164b-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="a164b-120">Se trata de una medida de seguridad que ayuda a garantizar que las vulnerabilidades relacionadas con la memoria (por ejemplo, desbordamientos de búfer) de la aplicación no se puedan aprovechar para ejecutar código arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a164b-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="a164b-121">End-User mitigación</span><span class="sxs-lookup"><span data-stu-id="a164b-121">End-User Mitigation</span></span>

-   <span data-ttu-id="a164b-122">Instale una versión posterior del complemento o del marco que sea compatible con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="a164b-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="a164b-123">Ejecute Internet Explorer con privilegios elevados como administrador y,  a continuación, deshabilite DEP/NX mediante la casilla Habilitar la protección de memoria para ayudar a mitigar los ataques en línea en la pestaña Opciones avanzadas de **Internet.**  /  </span><span class="sxs-lookup"><span data-stu-id="a164b-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="a164b-124">Solución para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="a164b-124">Developer Solution</span></span>

<span data-ttu-id="a164b-125">Compile aplicaciones mediante las versiones más recientes de los marcos compatibles con DEP.</span><span class="sxs-lookup"><span data-stu-id="a164b-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="a164b-126">Aprovechamiento de las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="a164b-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="a164b-127">Use la opción del vinculador /NXCOMPAT para indicar la compatibilidad de DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="a164b-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="a164b-128">Opte por el código en otras defensas disponibles, como la defensa de pila (/GS), el control seguro de excepciones (/SafeSEH) y ASLR (/DynamicBase).</span><span class="sxs-lookup"><span data-stu-id="a164b-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="a164b-129">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="a164b-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="a164b-130">Pruebe el código con DEP/NX habilitado mediante la versión Internet Explorer más reciente en Windows Vista SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a164b-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="a164b-131">Pruebe con Internet Explorer 7 en Windows Vista después de habilitar la opción DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="a164b-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="a164b-132">Para habilitar DEP/NX para Internet Explorer 7, ejecute Internet Explorer como administrador y, a continuación, establezca la casilla adecuada en la pestaña Herramientas > Opciones de Internet > avanzadas.</span><span class="sxs-lookup"><span data-stu-id="a164b-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="a164b-133">Ejecute Internet Explorer Compatibility Test Tool (IECTT), que se proporciona con Application Compatibility Toolkit (ACT) para localizar los posibles problemas debidos a los cambios de DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="a164b-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a164b-134">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="a164b-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="a164b-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span><span class="sxs-lookup"><span data-stu-id="a164b-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="a164b-136">Prevención de ejecución de datos</span><span class="sxs-lookup"><span data-stu-id="a164b-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="a164b-137">Nuevas API nx agregadas a Windows Vista SP1, Windows XP SP3 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a164b-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="a164b-138">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a164b-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="a164b-139">[Problemas conocidos Internet Explorer características de seguridad de seguridad](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a164b-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
