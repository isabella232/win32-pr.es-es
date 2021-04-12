---
description: Uso de la interfaz de usuario multilingüe
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso de la interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279494"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="aa38e-103">Uso de la interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="aa38e-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="aa38e-104">En esta sección se describe cómo usar la funcionalidad de la interfaz de usuario multilingüe (MUI) para diseñar e implementar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aa38e-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="aa38e-105">A continuación se muestran aspectos de la tecnología de MUI que entrarán en juego en la mayoría de las fases del ciclo de vida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa38e-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="aa38e-106">Desarrollo de aplicaciones, incluida la preparación de recursos, la configuración de las preferencias de idioma de la aplicación, la búsqueda y carga de recursos</span><span class="sxs-lookup"><span data-stu-id="aa38e-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="aa38e-107">Compilar y localizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="aa38e-107">Building and localizing the application</span></span>
-   <span data-ttu-id="aa38e-108">Implementación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="aa38e-108">Deploying the application</span></span>

<span data-ttu-id="aa38e-109">Estas son algunas preguntas a tener en cuenta al diseñar e implementar una aplicación de MUI.</span><span class="sxs-lookup"><span data-stu-id="aa38e-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="aa38e-110">¿Cuáles son las versiones de Windows compatibles con la aplicación?</span><span class="sxs-lookup"><span data-stu-id="aa38e-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="aa38e-111">¿En qué idiomas se localizará la aplicación?</span><span class="sxs-lookup"><span data-stu-id="aa38e-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="aa38e-112">¿La configuración de idioma de la aplicación siempre sigue la configuración de idioma para el sistema operativo o si el usuario de la aplicación puede establecer idiomas específicos?</span><span class="sxs-lookup"><span data-stu-id="aa38e-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="aa38e-113">¿Qué tipo de recursos de interfaz de usuario usa la aplicación y dónde se almacenan?</span><span class="sxs-lookup"><span data-stu-id="aa38e-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="aa38e-114">Esta sección incluye los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa38e-114">This section includes the following topics.</span></span> <span data-ttu-id="aa38e-115">Las descripciones suponen una aplicación de MUI destinada a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aa38e-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="aa38e-116">Los recursos de esta aplicación son recursos de Win32, con recursos específicos del lenguaje y código ejecutable que residen en archivos PE de Win32 independientes.</span><span class="sxs-lookup"><span data-stu-id="aa38e-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="aa38e-117">Las consideraciones especiales para la compatibilidad con los sistemas operativos anteriores a Windows Vista o para distintos tipos de recursos se agregan según corresponda.</span><span class="sxs-lookup"><span data-stu-id="aa38e-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="aa38e-118">Preparación de recursos</span><span class="sxs-lookup"><span data-stu-id="aa38e-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="aa38e-119">Configuración de las preferencias de idioma de la aplicación</span><span class="sxs-lookup"><span data-stu-id="aa38e-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="aa38e-120">Ubicar recursos PE de Win32</span><span class="sxs-lookup"><span data-stu-id="aa38e-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="aa38e-121">Ubicar recursos de PE que no son de Win32</span><span class="sxs-lookup"><span data-stu-id="aa38e-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="aa38e-122">Localizar recursos y compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="aa38e-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="aa38e-123">MUI: ejemplo de la aplicación de configuración del sistema</span><span class="sxs-lookup"><span data-stu-id="aa38e-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="aa38e-124">MUI: ejemplo de configuración de Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="aa38e-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="aa38e-125">MUI: ejemplo de configuración de Application-Specific (anterior a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="aa38e-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



