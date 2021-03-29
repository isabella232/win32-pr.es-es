---
title: Plataforma de sensor
description: Windows 7 ha cambiado la forma en que los desarrolladores usan sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077989"
---
# <a name="sensor-platform"></a><span data-ttu-id="6dda2-103">Plataforma de sensor</span><span class="sxs-lookup"><span data-stu-id="6dda2-103">Sensor Platform</span></span>

<span data-ttu-id="6dda2-104">Windows 7 ha cambiado la forma en que los desarrolladores usan sensores.</span><span class="sxs-lookup"><span data-stu-id="6dda2-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="6dda2-105">Incluye compatibilidad nativa con sensores, ampliada por una nueva plataforma de desarrollo para trabajar con sensores, incluidos sensores de ubicación, como dispositivos de sistemas de posicionamiento global (GPS).</span><span class="sxs-lookup"><span data-stu-id="6dda2-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="6dda2-106">Basado en la plataforma de sensores, las API de *Ubicación de Windows* son una nueva característica de Windows 7 que permite a los desarrolladores de aplicaciones tener acceso a la información de ubicación física del usuario.</span><span class="sxs-lookup"><span data-stu-id="6dda2-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="6dda2-107">Las API de *Ubicación de Windows* pueden abstraer el hardware, admitir simultáneamente varias aplicaciones y cambiar sin problemas entre distintas tecnologías, lo que alivia al desarrollador de la aplicación de la carga de administrar estas restricciones.</span><span class="sxs-lookup"><span data-stu-id="6dda2-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="6dda2-108">Los programadores pueden usar las API de *Ubicación* a través del lenguaje de programación C++ (los programadores familiarizados con el modelo de objetos componentes (com)) o el uso de objetos com en lenguajes de scripting, como Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="6dda2-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="6dda2-109">La compatibilidad con scripting proporciona un acceso fácil a los datos de ubicación de proyectos como gadgets.</span><span class="sxs-lookup"><span data-stu-id="6dda2-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="6dda2-110">Windows 7 proporciona una plataforma sólida y fácil de usar para el uso de dispositivos de sensor, como un sensor de luz ambiente o un medidor de temperatura, para crear un reconocimiento medioambiental en aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="6dda2-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="6dda2-111">Los equipos pueden usar sensores integrados en el equipo, conectados a través de conexiones cableadas o inalámbricas, o conectados a través de una red o *Internet*.</span><span class="sxs-lookup"><span data-stu-id="6dda2-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="6dda2-112">Las API de *sensor* y *Ubicación* proporcionan una manera estándar de detectar sensores y obtener acceso mediante programación a los datos proporcionados por los sensores.</span><span class="sxs-lookup"><span data-stu-id="6dda2-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="6dda2-113">El panel de control *del sensor* permite a los usuarios habilitar o deshabilitar sensores, controlar el acceso a los sensores que pueden exponer datos confidenciales, ver las propiedades del sensor y cambiar las descripciones de los sensores.</span><span class="sxs-lookup"><span data-stu-id="6dda2-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="6dda2-114">La [extensión de clase de sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) es una parte fundamental del modelo de desarrollo de controladores para la plataforma de sensor.</span><span class="sxs-lookup"><span data-stu-id="6dda2-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="6dda2-115">Proporciona los mecanismos siguientes, que se usan al escribir un controlador de sensor del [marco de trabajo de controladores de modo de usuario (UMDF)](https://developer.microsoft.com/windows/hardware) :</span><span class="sxs-lookup"><span data-stu-id="6dda2-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="6dda2-116">Integración con la plataforma de sensores</span><span class="sxs-lookup"><span data-stu-id="6dda2-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="6dda2-117">Cumplimiento de seguridad</span><span class="sxs-lookup"><span data-stu-id="6dda2-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dda2-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6dda2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dda2-119">API de sensor</span><span class="sxs-lookup"><span data-stu-id="6dda2-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>