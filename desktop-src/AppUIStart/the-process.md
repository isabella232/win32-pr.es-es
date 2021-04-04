---
title: Información general sobre el desarrollo de la interfaz de usuario
description: En esta sección se describen las tres fases del diseño de la interfaz de usuario y se presentan las tareas que normalmente están asociadas a cada fase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2020
ms.locfileid: "104077231"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="b355f-103">Información general sobre el proceso de desarrollo de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="b355f-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="b355f-104">En esta sección se describen las tres fases del diseño de la interfaz de usuario y se presentan las tareas que normalmente están asociadas a cada fase.</span><span class="sxs-lookup"><span data-stu-id="b355f-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="b355f-105">La interfaz de usuario de la aplicación y la experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="b355f-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="b355f-106">Para empezar, se deben aclarar los términos "interfaz de usuario" y "experiencia del usuario".</span><span class="sxs-lookup"><span data-stu-id="b355f-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="b355f-107">La interfaz de usuario de una aplicación normalmente implica los objetos que un usuario ve e interactúa directamente en su pantalla.</span><span class="sxs-lookup"><span data-stu-id="b355f-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="b355f-108">Por ejemplo, estos objetos incluyen el espacio del documento, menús, cuadros de diálogo, iconos, imágenes y animaciones.</span><span class="sxs-lookup"><span data-stu-id="b355f-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="b355f-109">Sin embargo, la interfaz de usuario de una aplicación es solo un aspecto de la experiencia global del usuario.</span><span class="sxs-lookup"><span data-stu-id="b355f-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="b355f-110">Otros aspectos de la experiencia del usuario que no son visibles para el usuario, pero que son esenciales para una aplicación y son fundamentales para su uso, incluyen el tiempo de inicio, la latencia, el control de errores y las tareas automatizadas que se completan sin la interacción directa del usuario.</span><span class="sxs-lookup"><span data-stu-id="b355f-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="b355f-111">En general, una interfaz de usuario requiere una acción por parte de un usuario para llevar a cabo una tarea, mientras que una excelente experiencia del usuario se puede lograr sin ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b355f-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="b355f-112">Desarrollo de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="b355f-112">User Interface Development</span></span>

<span data-ttu-id="b355f-113">Proporcionar una experiencia de usuario correcta requiere un enfoque equilibrado a lo largo del ciclo de vida de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b355f-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="b355f-114">Para garantizar este equilibrio, no solo debe centrarse en implementar la funcionalidad necesaria para completar una tarea, sino también en cómo se expone la tarea a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b355f-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="b355f-115">Recuerde que la interfaz de usuario no solo debe ser funcional, sino que también debe ser utilizable.</span><span class="sxs-lookup"><span data-stu-id="b355f-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="b355f-116">A continuación se describen las fases típicas del proceso de dvelopment de la interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="b355f-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="b355f-117">Diseño</span><span class="sxs-lookup"><span data-stu-id="b355f-117">Designing</span></span>

-   <span data-ttu-id="b355f-118">Requisitos funcionales: Determine los requisitos iniciales y los objetivos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b355f-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="b355f-119">Análisis de usuarios: Identifique los escenarios de usuario y comprenda las necesidades y expectativas de los usuarios de cada escenario.</span><span class="sxs-lookup"><span data-stu-id="b355f-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="b355f-120">Diseño conceptual: modelo de la empresa subyacente que debe admitir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b355f-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="b355f-121">Diseño lógico: permite diseñar el proceso y el flujo de información de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b355f-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="b355f-122">Diseño físico: decida cómo se implementará el diseño lógico en plataformas físicas específicas.</span><span class="sxs-lookup"><span data-stu-id="b355f-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="b355f-123">Implementar</span><span class="sxs-lookup"><span data-stu-id="b355f-123">Implementing</span></span>

-   <span data-ttu-id="b355f-124">Prototipo: desarrolle bocetos de pantalla interactivos o de papel que se centren en la interfaz y no incluyan elementos de diseño visuales que distraigan.</span><span class="sxs-lookup"><span data-stu-id="b355f-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="b355f-125">Construcción: compile la aplicación y prepárese para las solicitudes de cambio de diseño.</span><span class="sxs-lookup"><span data-stu-id="b355f-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="b355f-126">Prueba</span><span class="sxs-lookup"><span data-stu-id="b355f-126">Testing</span></span>

-   <span data-ttu-id="b355f-127">Pruebas de facilidad de uso: Pruebe la aplicación con varios usuarios y escenarios.</span><span class="sxs-lookup"><span data-stu-id="b355f-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="b355f-128">Pruebas de accesibilidad: Pruebe la aplicación con tecnologías accesibles y herramientas de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="b355f-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




