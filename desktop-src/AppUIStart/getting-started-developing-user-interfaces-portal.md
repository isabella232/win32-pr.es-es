---
title: Introducción al desarrollo de la interfaz de usuario para aplicaciones Windows
description: .
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c3d1a182aef6354901f0fa71f94b39ecdc58f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792982"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="367fc-103">Introducción desarrollar interfaces de usuario para aplicaciones Windows</span><span class="sxs-lookup"><span data-stu-id="367fc-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="367fc-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="367fc-104">Purpose</span></span>

<span data-ttu-id="367fc-105">En las secciones siguientes se ofrecen instrucciones generales para los programadores que diseñan, implementan y prueban la interfaz de usuario de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="367fc-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="367fc-106">Además de los principios básicos de diseño de la interfaz de usuario, se proporcionan numerosas recomendaciones y sugerencias que ayudarán a los desarrolladores a proporcionar una experiencia de usuario tan sencilla, eficaz y agradable como sea posible.</span><span class="sxs-lookup"><span data-stu-id="367fc-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="367fc-107">Estas instrucciones no pretenden ser completas y están sujetas a la funcionalidad y el ámbito específicos de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="367fc-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="367fc-108">Para obtener instrucciones más completas, consulte las directrices de interacción de la [experiencia del usuario de Windows](../uxguide/guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="367fc-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="367fc-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="367fc-109">In this section</span></span>



| <span data-ttu-id="367fc-110">Tema</span><span class="sxs-lookup"><span data-stu-id="367fc-110">Topic</span></span>                                                                            | <span data-ttu-id="367fc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="367fc-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="367fc-112">Información general sobre el proceso de desarrollo de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="367fc-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="367fc-113">En esta sección se describen las tres fases del diseño de la interfaz de usuario y se presentan las tareas que normalmente están asociadas a cada fase.</span><span class="sxs-lookup"><span data-stu-id="367fc-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="367fc-114">Diseñar una interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="367fc-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="367fc-115">En esta sección se describen detalladamente algunas de las tareas asociadas al diseño de una interfaz de usuario para una aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="367fc-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="367fc-116">Implementar una interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="367fc-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="367fc-117">En esta sección se describen algunas de las tareas asociadas con la implementación de una interfaz de usuario para una aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="367fc-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="367fc-118">Probar una interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="367fc-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="367fc-119">En esta sección se describen detalladamente algunas de las tareas asociadas a la prueba de una interfaz de usuario para una aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="367fc-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="367fc-120">Consideraciones de seguridad: interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="367fc-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="367fc-121">En este tema se proporciona información sobre las consideraciones de seguridad en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="367fc-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="367fc-122">Otros recursos</span><span class="sxs-lookup"><span data-stu-id="367fc-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="367fc-123">Esta sección contiene una lista de libros y recursos recomendados relacionados con el diseño de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="367fc-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="367fc-124">(Estos libros y recursos pueden no estar disponibles en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="367fc-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 

