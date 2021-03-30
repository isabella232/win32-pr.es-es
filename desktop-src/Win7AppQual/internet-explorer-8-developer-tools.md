---
description: .
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Herramientas para desarrolladores de Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a184b513717655ee0a738be6318b4c8f2515ca3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156673"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="07fdd-103">Herramientas para desarrolladores de Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="07fdd-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="07fdd-104">Windows Internet Explorer 8 incluye la característica Herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="07fdd-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="07fdd-105">Esta característica permite depurar Microsoft JScript rápidamente, investigar un comportamiento específico de Windows Internet Explorer o realizar una iteración rápida hasta el prototipo o probar una nueva solución de diseño.</span><span class="sxs-lookup"><span data-stu-id="07fdd-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="07fdd-106">En las secciones siguientes se describen las características importantes del Herramientas de desarrollo en Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="07fdd-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="07fdd-107">Integrado y sencillo de usar</span><span class="sxs-lookup"><span data-stu-id="07fdd-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="07fdd-108">Los Herramientas de desarrollo se incluyen en todas las instalaciones de Internet Explorer 8, de modo que puede depurar problemas en cualquier equipo que ejecute Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="07fdd-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="07fdd-109">Además, las herramientas solo se cargan cuando se necesitan para limitar el modo en que afectan al rendimiento del explorador.</span><span class="sxs-lookup"><span data-stu-id="07fdd-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="07fdd-110">Mediante el Herramientas de desarrollo, puede depurar rápidamente solo el proceso actual de Internet Explorer, en lugar de depurar para todo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="07fdd-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="07fdd-111">Proporcionar una interfaz visual a la plataforma</span><span class="sxs-lookup"><span data-stu-id="07fdd-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="07fdd-112">En lugar de aplicar ingeniería inversa a cómo funciona el sitio web o modificar su sitio para generar información de depuración, el Herramientas de desarrollo le permite buscar en Internet Explorer para ver su representación de su sitio.</span><span class="sxs-lookup"><span data-stu-id="07fdd-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="07fdd-113">Esta vista reduce el tiempo que se emplea en la depuración de sitios dinámicos, en los que la inspección de origen no es útil o en la investigación de un comportamiento específico de Internet Explorer, donde una herramienta de creación genérica no sirve de ayuda.</span><span class="sxs-lookup"><span data-stu-id="07fdd-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="07fdd-114">Habilitar experimentación rápida</span><span class="sxs-lookup"><span data-stu-id="07fdd-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="07fdd-115">Al crear un prototipo de un nuevo diseño o probar correcciones en versiones anteriores de Internet Explorer, es probable que edite el origen, lo guarde, actualice la página en el explorador y repita.</span><span class="sxs-lookup"><span data-stu-id="07fdd-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="07fdd-116">El Herramientas de desarrollo optimizar este escenario permitiéndole editar el sitio en el explorador y ver los cambios inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="07fdd-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="07fdd-117">Optimizar el rendimiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="07fdd-117">Optimize Application Performance</span></span>

<span data-ttu-id="07fdd-118">Para identificar y corregir problemas de rendimiento, es probable que recorra en iteración en un escenario cada vez.</span><span class="sxs-lookup"><span data-stu-id="07fdd-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="07fdd-119">Al usar el generador de perfiles de script en el Herramientas de desarrollo, puede recopilar estadísticas, incluidos el tiempo de ejecución y el número de veces que se llama a una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07fdd-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="07fdd-120">Puede usar esta información al probar la aplicación y usar el informe de perfil para identificar y corregir rápidamente los cuellos de botella de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="07fdd-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="07fdd-121">Para tener acceso al Herramientas de desarrollo, presione F12 mientras está viendo una página web o haga clic en **herramientas de desarrollo** en el menú **herramientas** .</span><span class="sxs-lookup"><span data-stu-id="07fdd-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07fdd-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07fdd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07fdd-123">Herramientas para depurar aplicaciones web y complementos</span><span class="sxs-lookup"><span data-stu-id="07fdd-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



