---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-cadena de agente de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314798"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="190f2-103">Internet Explorer 8-cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="190f2-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="190f2-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="190f2-104">Affected Platforms</span></span>

 <span data-ttu-id="190f2-105">**Clientes** : Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="190f2-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="190f2-106">**Servidores** : windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="190f2-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="190f2-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="190f2-107">Feature Impact</span></span>

<span data-ttu-id="190f2-108">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="190f2-108">**Severity** - Medium</span></span>  
<span data-ttu-id="190f2-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="190f2-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="190f2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="190f2-110">Description</span></span>

<span data-ttu-id="190f2-111">La cadena de agente de usuario es el identificador de Internet Explorer que proporciona datos sobre su versión y otros atributos a los servidores Web.</span><span class="sxs-lookup"><span data-stu-id="190f2-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="190f2-112">Muchas aplicaciones web se basan en la cadena de agente de usuario de IE y se superponer en ella.</span><span class="sxs-lookup"><span data-stu-id="190f2-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="190f2-113">Los que lo hacen y dependen de un número de versión anterior se verán afectados.</span><span class="sxs-lookup"><span data-stu-id="190f2-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="190f2-114">La cadena de agente de usuario ahora incluye la cadena ' Trident/4.0 ' para permitir la diferencia entre la cadena de agente de usuario de Internet Explorer 7 y la cadena de agente de usuario de Internet Explorer 8 cuando se ejecuta en la vista de compatibilidad de Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="190f2-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="190f2-115">Consulte Descripción de las cadenas de agente de usuario para más información.</span><span class="sxs-lookup"><span data-stu-id="190f2-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="190f2-116">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="190f2-116">Manifestation of Impact</span></span>

<span data-ttu-id="190f2-117">Hay dos áreas afectadas:</span><span class="sxs-lookup"><span data-stu-id="190f2-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="190f2-118">Es posible que las páginas web que comprueben explícitamente la cadena de agente de usuario y no admitan la cadena de agente de usuario de Internet Explorer 8 no se ejecuten correctamente.</span><span class="sxs-lookup"><span data-stu-id="190f2-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="190f2-119">En la mayoría de los casos, esto significa que las páginas bloquearán a los usuarios el contenido al que intentan acceder o que muestren contenido incorrecto o con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="190f2-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="190f2-120">Las aplicaciones que hospedan Trident (consulte hospedaje y reutilización) tendrán como valor predeterminado Internet Explorer 7 mediante el componente opcional Web, pero no tendrán acceso a las características de Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="190f2-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="190f2-121">Solución</span><span class="sxs-lookup"><span data-stu-id="190f2-121">Solution</span></span>

<span data-ttu-id="190f2-122">Asegúrese de que las aplicaciones controlan correctamente la nueva versión de "MSIE 8,0" en la cadena de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="190f2-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="190f2-123">También puede optar por la vista de compatibilidad de Internet Explorer 7 para esas aplicaciones basadas en Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="190f2-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="190f2-124">Esto puede hacerse con etiquetas meta.</span><span class="sxs-lookup"><span data-stu-id="190f2-124">This can be done with meta tags.</span></span> <span data-ttu-id="190f2-125">Consulte la explicación de descripción de las cadenas de agente de usuario para más información.</span><span class="sxs-lookup"><span data-stu-id="190f2-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="190f2-126">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="190f2-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="190f2-127">Ejecute las aplicaciones y las páginas web en un entorno de Internet Explorer 8 en Windows Vista o Windows XP para asegurarse de que se comportan de la manera deseada.</span><span class="sxs-lookup"><span data-stu-id="190f2-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="190f2-128">Como alternativa, puede ejecutar la herramienta de prueba de compatibilidad de Internet Explorer (IECTT) que se proporciona con el kit de herramientas de compatibilidad de aplicaciones (ACT) para localizar cualquier posible problema debido a las actualizaciones de las características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="190f2-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="190f2-129">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="190f2-129">Links to Other Resources</span></span>

-   <span data-ttu-id="190f2-130">[Descripción de las cadenas de agente de usuario](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="190f2-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="190f2-131">Cadena de User-Agent de Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="190f2-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="190f2-132">Vector de versión y cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="190f2-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="190f2-133">[Hospedaje y reutilización](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="190f2-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="190f2-134">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="190f2-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="190f2-135">[Problemas conocidos de la característica de seguridad de Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="190f2-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
