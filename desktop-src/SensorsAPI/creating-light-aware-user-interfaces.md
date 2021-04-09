---
description: En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Crear interfaces de usuario Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002467"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="29267-103">Crear interfaces de usuario Light-Aware</span><span class="sxs-lookup"><span data-stu-id="29267-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="29267-104">En esta sección se trata el uso de datos del sensor de luz ambiente y cómo se pueden optimizar las características de la interfaz de usuario y el contenido del programa para muchas condiciones de iluminación.</span><span class="sxs-lookup"><span data-stu-id="29267-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="29267-105">Los sensores de luz ambiente exponen los datos que se pueden usar para determinar diversos aspectos de las condiciones de iluminación en las que se encuentra el sensor.</span><span class="sxs-lookup"><span data-stu-id="29267-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="29267-106">Los sensores de luz ambiente pueden exponer el brillo general de un entorno (luminancia) y otros aspectos de la luz circundante, como la cromaticidad o la temperatura de color.</span><span class="sxs-lookup"><span data-stu-id="29267-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="29267-107">Los equipos pueden ser más útiles de varias maneras cuando el sistema responde a las condiciones de iluminación.</span><span class="sxs-lookup"><span data-stu-id="29267-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="29267-108">Esto incluye controlar el brillo de la pantalla del equipo (una característica nueva y totalmente compatible en Windows 7), ajustar automáticamente el nivel de iluminación de los teclados iluminados e incluso controlar la luminosidad de otras luces (como la iluminación del botón, las luces de actividad, etc.).</span><span class="sxs-lookup"><span data-stu-id="29267-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="29267-109">Los programas de usuario final también pueden beneficiarse de los sensores ligeros.</span><span class="sxs-lookup"><span data-stu-id="29267-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="29267-110">Los programas pueden aplicar un tema adecuado para una condición de iluminación determinada, como un tema de exterior específico y un tema de interior.</span><span class="sxs-lookup"><span data-stu-id="29267-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="29267-111">Quizás el aspecto más importante de la integración del sensor de luz con los programas es la legibilidad y las optimizaciones de legibilidad basadas en condiciones de iluminación.</span><span class="sxs-lookup"><span data-stu-id="29267-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="29267-112">La API de sensor permite crear dichos programas.</span><span class="sxs-lookup"><span data-stu-id="29267-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="29267-113">Considere el siguiente escenario:</span><span class="sxs-lookup"><span data-stu-id="29267-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="29267-114">Escenario: uso del portátil para navegar a un restaurante</span><span class="sxs-lookup"><span data-stu-id="29267-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="29267-115">Supongamos que desea utilizar su equipo para ayudarle a desplazarse a un restaurante nuevo.</span><span class="sxs-lookup"><span data-stu-id="29267-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="29267-116">Comience en su casa, busque la dirección del restaurante y planee la ruta.</span><span class="sxs-lookup"><span data-stu-id="29267-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="29267-117">En la siguiente captura de pantalla se muestra cómo el programa de navegación podría optimizar su interfaz de usuario para mostrar información detallada en condiciones de iluminación interior.</span><span class="sxs-lookup"><span data-stu-id="29267-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![interfaz de usuario diseñada para la iluminación interior.](images/nav-normal.png)

<span data-ttu-id="29267-119">Cuando se desplaza fuera de su coche, tiene una luz solar directa, lo que dificulta la lectura de la pantalla del portátil.</span><span class="sxs-lookup"><span data-stu-id="29267-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="29267-120">En la captura de pantalla siguiente se muestra cómo el programa puede modificar su interfaz de usuario para maximizar la legibilidad y la legibilidad en la luz directa.</span><span class="sxs-lookup"><span data-stu-id="29267-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="29267-121">En esta vista, gran parte de los detalles se han omitido y el contraste está maximizado.</span><span class="sxs-lookup"><span data-stu-id="29267-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![interfaz de usuario diseñada para condiciones de iluminación directa.](images/nav-contrast.png)

<span data-ttu-id="29267-123">A medida que se acerque al restaurante, los enfoques de la noche y se oscurecerán.</span><span class="sxs-lookup"><span data-stu-id="29267-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="29267-124">En la siguiente captura de pantalla, la interfaz de usuario del programa de navegación se ha optimizado para la visualización con poca luz.</span><span class="sxs-lookup"><span data-stu-id="29267-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="29267-125">Al usar los colores más oscuros en general, esta interfaz de usuario es fácil de mirar en el coche oscuro.</span><span class="sxs-lookup"><span data-stu-id="29267-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![interfaz de usuario diseñada para visualización con poca luz.](images/nav-lowlight.png)

<span data-ttu-id="29267-127">En el resto de esta sección, explorará algunas cosas que puede hacer para optimizar los programas para diversas condiciones de iluminación y cómo puede usar la API de sensor para ayudar a habilitar la interfaz de usuario de reconocimiento ligero.</span><span class="sxs-lookup"><span data-stu-id="29267-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29267-128">En esta sección</span><span class="sxs-lookup"><span data-stu-id="29267-128">In This Section</span></span>

-   [<span data-ttu-id="29267-129">Aspectos básicos de las interfaces de usuario de Light-Aware</span><span class="sxs-lookup"><span data-stu-id="29267-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="29267-130">Ejemplos de interfaces de usuario Light-Aware</span><span class="sxs-lookup"><span data-stu-id="29267-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="29267-131">Optimización de la experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="29267-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="29267-132">Descripción e interpretación de los valores de Lux</span><span class="sxs-lookup"><span data-stu-id="29267-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="29267-133">Uso de datos del sensor de luz</span><span class="sxs-lookup"><span data-stu-id="29267-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



