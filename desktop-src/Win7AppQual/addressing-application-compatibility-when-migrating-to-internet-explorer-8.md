---
description: Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088773"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="e5928-103">Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="e5928-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="e5928-104">En esta sección se proporciona información general sobre las pruebas de problemas de compatibilidad de aplicaciones y la corrección de esos problemas en aplicaciones web para Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="e5928-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="e5928-105">En los temas siguientes se describen los cambios en Internet Explorer 8 y las herramientas y tecnologías para garantizar la compatibilidad con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5928-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="e5928-106">Sección</span><span class="sxs-lookup"><span data-stu-id="e5928-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="e5928-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5928-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5928-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="e5928-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="e5928-109">Proporciona información general sobre Internet Explorer 8 consideraciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e5928-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="e5928-110">Descripción del desafío de la compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e5928-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="e5928-111">Proporciona información general sobre Internet Explorer compatibilidad con 8.</span><span class="sxs-lookup"><span data-stu-id="e5928-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="e5928-112">Estándares web y compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e5928-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="e5928-113">Proporciona información general sobre por qué los estándares web son importantes.</span><span class="sxs-lookup"><span data-stu-id="e5928-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="e5928-114">Diseñar actualizaciones que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="e5928-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="e5928-115">Proporciona información general sobre las actualizaciones de diseño que afectan a la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e5928-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="e5928-116">Corrección de problemas de compatibilidad en aplicaciones web y complementos</span><span class="sxs-lookup"><span data-stu-id="e5928-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="e5928-117">Ofrece sugerencias para solucionar problemas de compatibilidad con aplicaciones web y complementos.</span><span class="sxs-lookup"><span data-stu-id="e5928-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="e5928-118">Herramientas para depurar aplicaciones web y complementos</span><span class="sxs-lookup"><span data-stu-id="e5928-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="e5928-119">Enumera las herramientas que están disponibles para depurar aplicaciones web y complementos.</span><span class="sxs-lookup"><span data-stu-id="e5928-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="e5928-120">Apéndice 1: Internet Explorer 6 a Internet Explorer 8 cambios en el explorador</span><span class="sxs-lookup"><span data-stu-id="e5928-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="e5928-121">Muestra los cambios de Microsoft Internet Explorer 6 a Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="e5928-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="e5928-122">Apéndice 2: Escenarios de script de prueba</span><span class="sxs-lookup"><span data-stu-id="e5928-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="e5928-123">Enumera los escenarios recomendados para probar los sitios por razones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e5928-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



