---
description: 'Internet Explorer 8: Cadena del agente de usuario'
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: 'Internet Explorer 8: Cadena del agente de usuario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088243"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="ac865-103">Internet Explorer 8: Cadena del agente de usuario</span><span class="sxs-lookup"><span data-stu-id="ac865-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ac865-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="ac865-104">Affected Platforms</span></span>

 <span data-ttu-id="ac865-105">**Clientes:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac865-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="ac865-106">**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac865-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="ac865-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="ac865-107">Feature Impact</span></span>

<span data-ttu-id="ac865-108">**Gravedad:** media</span><span class="sxs-lookup"><span data-stu-id="ac865-108">**Severity** - Medium</span></span>  
<span data-ttu-id="ac865-109">**Frecuencia:** alta</span><span class="sxs-lookup"><span data-stu-id="ac865-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="ac865-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac865-110">Description</span></span>

<span data-ttu-id="ac865-111">La cadena del agente de usuario es el Internet Explorer que proporciona datos sobre su versión y otros atributos a los servidores web.</span><span class="sxs-lookup"><span data-stu-id="ac865-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="ac865-112">Muchas aplicaciones web se basan en la cadena del agente de usuario de IE y se basan en ello.</span><span class="sxs-lookup"><span data-stu-id="ac865-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="ac865-113">Los que lo hagan y dependan de un número de versión anterior se verán afectados.</span><span class="sxs-lookup"><span data-stu-id="ac865-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="ac865-114">La cadena del Agente de usuario ahora incluye la cadena "Trident/4.0" para permitir la diferenciación entre la cadena del agente de usuario de Internet Explorer 7 y la cadena del Agente de usuario de Internet Explorer 8 cuando se ejecuta en Internet Explorer 7 Vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac865-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="ac865-115">Consulte Understanding User Agent Strings (Descripción de las cadenas del agente de usuario) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ac865-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ac865-116">Demostración del impacto</span><span class="sxs-lookup"><span data-stu-id="ac865-116">Manifestation of Impact</span></span>

<span data-ttu-id="ac865-117">Hay dos áreas afectadas:</span><span class="sxs-lookup"><span data-stu-id="ac865-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="ac865-118">Es posible que las páginas web que comprueban explícitamente la cadena del agente de usuario y no admiten la cadena del agente de Internet Explorer 8 no se ejecuten correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac865-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="ac865-119">En la mayoría de los casos, esto significa que las páginas bloquearán a los usuarios del contenido al que están intentando acceder o mostrarán contenido incorrecto o incorrecto.</span><span class="sxs-lookup"><span data-stu-id="ac865-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="ac865-120">Las aplicaciones que hospedan Trident (consulte Hospedaje y reutilización) tendrán como valor predeterminado Internet Explorer 7 mediante el componente opcional web, pero no tendrán acceso a Internet Explorer 8 características.</span><span class="sxs-lookup"><span data-stu-id="ac865-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="ac865-121">Solución</span><span class="sxs-lookup"><span data-stu-id="ac865-121">Solution</span></span>

<span data-ttu-id="ac865-122">Asegúrese de que las aplicaciones controlan correctamente la nueva versión "MSIE 8.0" en la cadena del agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="ac865-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="ac865-123">También puede participar en la Internet Explorer 7 Vista de compatibilidad para esas aplicaciones basadas en Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="ac865-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="ac865-124">Esto se puede hacer con metaetiquetas.</span><span class="sxs-lookup"><span data-stu-id="ac865-124">This can be done with meta tags.</span></span> <span data-ttu-id="ac865-125">Consulte la explicación en Descripción de las cadenas del agente de usuario para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ac865-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="ac865-126">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="ac865-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="ac865-127">Ejecute sus aplicaciones y páginas web en un entorno Internet Explorer 8 en Windows Vista o Windows XP para asegurarse de que se comportan de la manera deseada.</span><span class="sxs-lookup"><span data-stu-id="ac865-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="ac865-128">Como alternativa, puede ejecutar la herramienta de prueba de compatibilidad de Internet Explorer (IECTT) que se proporciona con el kit de herramientas de compatibilidad de aplicaciones (ACT) para localizar posibles problemas debidos a las actualizaciones de características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ac865-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ac865-129">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="ac865-129">Links to Other Resources</span></span>

-   <span data-ttu-id="ac865-130">[Descripción de las cadenas del Agente de usuario](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ac865-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="ac865-131">Internet Explorer 8 User-Agent String</span><span class="sxs-lookup"><span data-stu-id="ac865-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="ac865-132">Cadena de agente de usuario y vector de versión</span><span class="sxs-lookup"><span data-stu-id="ac865-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="ac865-133">[Hospedaje y reutilización](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ac865-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="ac865-134">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ac865-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="ac865-135">[Problemas conocidos Internet Explorer características de seguridad](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ac865-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
