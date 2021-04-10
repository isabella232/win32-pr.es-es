---
title: La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"
description: La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269331"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="4c45a-103">La interfaz de usuario perimetral se suprime en escenarios "in-in-in" e "inercia"</span><span class="sxs-lookup"><span data-stu-id="4c45a-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="4c45a-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="4c45a-104">Platform</span></span>

<dl> <span data-ttu-id="4c45a-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4c45a-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="4c45a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c45a-106">Description</span></span>

<span data-ttu-id="4c45a-107">Hay algunos casos en los que los usuarios pueden invocar involuntariamente la interfaz de usuario perimetral (accesos, barra de aplicaciones, conmutación de aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="4c45a-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="4c45a-108">Hemos introducido una característica que permite a los desarrolladores diseñar su interfaz de usuario para toda la pantalla sin necesidad de prestaciones (por ejemplo, bordes) para evitar que el usuario golpee accidentalmente los bordes.</span><span class="sxs-lookup"><span data-stu-id="4c45a-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="4c45a-109">Hay dos casos en los que es posible que se produzcan con más frecuencia los deslizantes de la arista involuntaria:</span><span class="sxs-lookup"><span data-stu-id="4c45a-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="4c45a-110">En el movimiento panorámico rápido, la velocidad y el imprecisión de la interacción pueden ocasionar ocasionalmente que entren en el borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4c45a-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="4c45a-111">Si los usuarios salen y vuelven a entrar rápidamente en el área de la pantalla mientras escriben entradas manuscritas con el dedo, por ejemplo, en una aplicación de pintura, este comportamiento en espera puede desencadenar erróneamente la interfaz de usuario perimetral e interrumpir la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="4c45a-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="4c45a-112">Para mejorar la experiencia del usuario y del desarrollador, la interfaz de usuario perimetral ahora se suprimirá en dos instancias específicas:</span><span class="sxs-lookup"><span data-stu-id="4c45a-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="4c45a-113">Cuando un usuario está en movimiento panorámico en una aplicación que admite la inercia DManip y desliza el dedo fuera de la pantalla mientras se está produciendo la inercia, la interfaz de usuario perimetral no se invocará dentro de una ventana de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="4c45a-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="4c45a-114">En los dispositivos certificados, cuando un usuario se desliza rápidamente desde la pantalla hacia fuera de la pantalla y viceversa, dentro de determinados parámetros, no se invocará la interfaz de usuario perimetral.</span><span class="sxs-lookup"><span data-stu-id="4c45a-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="4c45a-115">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="4c45a-115">Manifestations</span></span>

<span data-ttu-id="4c45a-116">Los usuarios que se deslizan rápidamente con el borde mientras se usa una aplicación verán una disminución en la invocación del perímetro involuntaria.</span><span class="sxs-lookup"><span data-stu-id="4c45a-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="4c45a-117">Solución</span><span class="sxs-lookup"><span data-stu-id="4c45a-117">Solution</span></span>

<span data-ttu-id="4c45a-118">Los desarrolladores deben tener en cuenta estos factores y deben poder usar la pantalla completa sin temor de que los usuarios desencadenen accidentalmente la interfaz de usuario perimetral mientras interactúan con la aplicación a lo largo del perímetro.</span><span class="sxs-lookup"><span data-stu-id="4c45a-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




