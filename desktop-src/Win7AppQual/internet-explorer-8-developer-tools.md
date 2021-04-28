---
description: Herramientas para desarrolladores de Internet Explorer 8
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Herramientas para desarrolladores de Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a4314d5d0392b9bc4933b945f7da32040e1570
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088213"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="00c24-103">Herramientas para desarrolladores de Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="00c24-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="00c24-104">Windows Internet Explorer 8 incluye Herramientas de desarrollo característica.</span><span class="sxs-lookup"><span data-stu-id="00c24-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="00c24-105">Esta característica le permite depurar Microsoft JScript rápidamente, investigar un comportamiento específico de Windows Internet Explorer o iterar rápidamente para crear prototipos o probar una nueva solución de diseño.</span><span class="sxs-lookup"><span data-stu-id="00c24-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="00c24-106">En las secciones siguientes se describen las características importantes del Herramientas de desarrollo en Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="00c24-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="00c24-107">Integrado y fácil de usar</span><span class="sxs-lookup"><span data-stu-id="00c24-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="00c24-108">Los Herramientas de desarrollo se incluyen con cada instalación de Internet Explorer 8, por lo que puede depurar problemas en cualquier equipo que ejecute Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="00c24-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="00c24-109">Además, las herramientas solo se cargan cuando las necesita para limitar cómo afectan al rendimiento del explorador.</span><span class="sxs-lookup"><span data-stu-id="00c24-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="00c24-110">Mediante el uso de Herramientas de desarrollo, puede depurar rápidamente solo el proceso de Internet Explorer actual, en lugar de depurar para todos los Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="00c24-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="00c24-111">Proporcionar una interfaz visual a la plataforma</span><span class="sxs-lookup"><span data-stu-id="00c24-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="00c24-112">En lugar de realizar ingeniería inversa sobre cómo funciona el sitio web o modificar el sitio para generar información de depuración, el Herramientas de desarrollo permite buscar en Internet Explorer para ver su representación del sitio.</span><span class="sxs-lookup"><span data-stu-id="00c24-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="00c24-113">Esta vista reduce el tiempo que dedica a depurar sitios dinámicos, donde la inspección de origen no es útil, o a investigar un comportamiento específico de Internet Explorer, donde una herramienta de creación genérica no puede ayudar.</span><span class="sxs-lookup"><span data-stu-id="00c24-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="00c24-114">Habilitación de la experimentación rápida</span><span class="sxs-lookup"><span data-stu-id="00c24-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="00c24-115">Al crear prototipos de un nuevo diseño o correcciones de pruebas en versiones anteriores de Internet Explorer, es probable que edite el origen, guárdelo, actualice la página en el explorador y repita la sesión.</span><span class="sxs-lookup"><span data-stu-id="00c24-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="00c24-116">El Herramientas de desarrollo este escenario al permitirle editar el sitio en el explorador y ver los cambios inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="00c24-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="00c24-117">Optimización del rendimiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="00c24-117">Optimize Application Performance</span></span>

<span data-ttu-id="00c24-118">Para identificar y corregir problemas de rendimiento, es probable que itera al centrarse en un escenario a la vez.</span><span class="sxs-lookup"><span data-stu-id="00c24-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="00c24-119">Mediante el uso del profiler de script en el Herramientas de desarrollo, puede recopilar estadísticas, incluido el tiempo de ejecución y el número de veces que se llama a una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="00c24-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="00c24-120">Puede usar esta información a medida que prueba la aplicación y usa el informe de perfil para identificar y corregir rápidamente los cuellos de botella de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="00c24-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="00c24-121">Para acceder a la Herramientas de desarrollo, presione F12 mientras ve una página web o haga clic **Herramientas de desarrollo** en el **menú** Herramientas.</span><span class="sxs-lookup"><span data-stu-id="00c24-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00c24-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00c24-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c24-123">Herramientas para depurar aplicaciones web y complementos</span><span class="sxs-lookup"><span data-stu-id="00c24-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



