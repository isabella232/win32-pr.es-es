---
title: Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla
description: Para localizar los elementos secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden presionar puntos de prueba en la pantalla.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656277"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="62b70-103">Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla</span><span class="sxs-lookup"><span data-stu-id="62b70-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="62b70-104">Para localizar los elementos secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden presionar puntos de prueba en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="62b70-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="62b70-105">Hay dos métodos disponibles:</span><span class="sxs-lookup"><span data-stu-id="62b70-105">Two methods are available:</span></span>

-   [<span data-ttu-id="62b70-106">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="62b70-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="62b70-107">**IAccessible:: accLocation**</span><span class="sxs-lookup"><span data-stu-id="62b70-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="62b70-108">Usar IAccessible:: accHitTest</span><span class="sxs-lookup"><span data-stu-id="62b70-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="62b70-109">Para identificar si un punto está dentro de un objeto, dentro de su elemento secundario o ninguno de los clientes, llame al método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) del objeto primario, pasando las coordenadas de pantalla del punto al que se va a realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="62b70-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="62b70-110">En la lista siguiente se describen algunos escenarios típicos:</span><span class="sxs-lookup"><span data-stu-id="62b70-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="62b70-111">Si los elementos secundarios del objeto se superponen en un punto especificado, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera el elemento secundario de nivel superior que aparece visualmente para ocupar el espacio.</span><span class="sxs-lookup"><span data-stu-id="62b70-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="62b70-112">Si una ventana cubre un elemento secundario, o si el elemento primario recorta el elemento secundario, la prueba de posicionamiento del punto de cobertura recupera el elemento secundario aunque no esté visible.</span><span class="sxs-lookup"><span data-stu-id="62b70-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="62b70-113">Si el elemento secundario que se encuentra en el punto especificado es un objeto accesible, en lugar de un elemento secundario, el método devuelve la interfaz [**IDispatch**](idispatch-interface.md) del elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="62b70-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="62b70-114">Usar IAccessible:: accLocation</span><span class="sxs-lookup"><span data-stu-id="62b70-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="62b70-115">Para obtener la ubicación de la pantalla de un objeto o de uno de los elementos secundarios del objeto, los clientes llaman a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span><span class="sxs-lookup"><span data-stu-id="62b70-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="62b70-116">Este método devuelve las coordenadas del rectángulo delimitador del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="62b70-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="62b70-117">Si el objeto no tiene la forma de un rectángulo, el método devuelve las coordenadas del rectángulo más pequeño que abarca todo el objeto.</span><span class="sxs-lookup"><span data-stu-id="62b70-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="62b70-118">La ilustración siguiente muestra la relación entre la región de un objeto no rectangular y su rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="62b70-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![Ilustración que muestra la región de un objeto no rectangular (un círculo) y su rectángulo delimitador.](images/region.gif)

> [!Note]  
> <span data-ttu-id="62b70-120">[**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) es más preciso que [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , ya que permite que los clientes determinen la ubicación de los objetos píxel a píxel en lugar de con rectángulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="62b70-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="62b70-121">Esta precisión es útil, por ejemplo, cuando una aplicación está recopilando información realizando un seguimiento de la ubicación del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="62b70-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




