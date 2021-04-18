---
title: Reutilizar objetos
description: Reutilizar objetos
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2020
ms.locfileid: "104533081"
---
# <a name="reusing-objects"></a><span data-ttu-id="16189-103">Reutilizar objetos</span><span class="sxs-lookup"><span data-stu-id="16189-103">Reusing Objects</span></span>

<span data-ttu-id="16189-104">Un objetivo importante de cualquier modelo de objetos es permitir que los autores de objetos reutilicen y extiendan objetos proporcionados por otros como partes de sus propias implementaciones.</span><span class="sxs-lookup"><span data-stu-id="16189-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="16189-105">Una manera de hacer esto en Microsoft Visual C++ y en otros lenguajes es mediante la *herencia de implementación*, que permite que un objeto herede ("subclase") algunas de sus funciones de otro objeto y reemplace otras funciones.</span><span class="sxs-lookup"><span data-stu-id="16189-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="16189-106">El problema de la interacción de objetos en todo el sistema mediante la herencia de implementación tradicional es que el contrato (la interfaz) entre los objetos de una jerarquía de implementación no está claramente definido.</span><span class="sxs-lookup"><span data-stu-id="16189-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="16189-107">De hecho, es implícito y ambiguo.</span><span class="sxs-lookup"><span data-stu-id="16189-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="16189-108">Cuando el objeto primario o secundario cambia su implementación, el comportamiento de los componentes relacionados podría quedar indefinido o implementado sin problemas.</span><span class="sxs-lookup"><span data-stu-id="16189-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="16189-109">En una sola aplicación, donde la implementación puede ser administrada por un único equipo de ingeniería que actualice todos los componentes al mismo tiempo, no siempre es una preocupación importante.</span><span class="sxs-lookup"><span data-stu-id="16189-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="16189-110">En un entorno en el que los componentes de un equipo se crean a través de la reutilización en caja negra de otros componentes creados por otros equipos, este tipo de inestabilidad se arriesga a reutilizar.</span><span class="sxs-lookup"><span data-stu-id="16189-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="16189-111">Además, la herencia de implementación normalmente solo funciona dentro de los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="16189-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="16189-112">Esto hace que la herencia de implementación tradicional no sea práctica para sistemas grandes y en constante evolución compuestos por componentes de software creados por muchos equipos de ingeniería.</span><span class="sxs-lookup"><span data-stu-id="16189-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="16189-113">La clave para crear componentes reutilizables es poder tratar el objeto como un cuadro opaco.</span><span class="sxs-lookup"><span data-stu-id="16189-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="16189-114">Esto significa que el fragmento de código que intenta volver a usar otro objeto no sabe nada y no necesita saber nada sobre la estructura interna o la implementación del componente que se está usando.</span><span class="sxs-lookup"><span data-stu-id="16189-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="16189-115">En otras palabras, el código que intenta volver a usar un componente depende del comportamiento del objeto y no de su implementación exacta.</span><span class="sxs-lookup"><span data-stu-id="16189-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="16189-116">Para lograr una reutilización en negro, COM adopta otros mecanismos de reusabilidad establecidos, como la *contención/delegación* y la *agregación*.</span><span class="sxs-lookup"><span data-stu-id="16189-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="16189-117">Para mayor comodidad, el objeto que se va a reutilizar se denomina *objeto interno* y el objeto que utiliza ese objeto interno es el *objeto externo*.</span><span class="sxs-lookup"><span data-stu-id="16189-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="16189-118">Es importante recordar en ambos mecanismos cómo aparece el objeto externo a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="16189-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="16189-119">En lo que respecta a los clientes, ambos objetos implementan las interfaces en las que el cliente puede obtener un puntero.</span><span class="sxs-lookup"><span data-stu-id="16189-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="16189-120">El cliente trata el objeto externo como un cuadro opaco y, por lo tanto, no tiene que preocuparse por la estructura interna de los objectâ externos, por lo que el cliente solo le preocupa el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="16189-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="16189-121">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="16189-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="16189-122">Contención/delegación</span><span class="sxs-lookup"><span data-stu-id="16189-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="16189-123">Agregación</span><span class="sxs-lookup"><span data-stu-id="16189-123">Aggregation</span></span>](aggregation.md)

 

 




