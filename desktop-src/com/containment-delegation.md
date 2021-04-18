---
title: Contención/delegación
description: El mecanismo más común para la reutilización de objetos en COM es la contención o delegación.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357692"
---
# <a name="containmentdelegation"></a><span data-ttu-id="44646-103">Contención/delegación</span><span class="sxs-lookup"><span data-stu-id="44646-103">Containment/Delegation</span></span>

<span data-ttu-id="44646-104">El mecanismo más común para la reutilización de objetos en COM es la *contención o delegación*.</span><span class="sxs-lookup"><span data-stu-id="44646-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="44646-105">Este tipo de reutilización es un concepto conocido que se encuentra en la mayoría de los lenguajes y sistemas orientados a objetos.</span><span class="sxs-lookup"><span data-stu-id="44646-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="44646-106">El objeto externo, que necesita hacer uso del objeto interno, actúa como cliente de objeto para el objeto interno.</span><span class="sxs-lookup"><span data-stu-id="44646-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="44646-107">El objeto externo "contiene" el objeto interno y, cuando el objeto externo requiere los servicios del objeto interno, el objeto externo delega explícitamente la implementación a los métodos del objeto interno.</span><span class="sxs-lookup"><span data-stu-id="44646-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="44646-108">Es decir, el objeto externo utiliza los servicios del objeto interno para implementarse a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="44646-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="44646-109">No es necesario que los objetos externos e internos admitan las mismas interfaces, aunque ciertamente es razonable contener un objeto que implementa una interfaz que el objeto externo no e implementar los métodos del objeto externo simplemente como llamadas a los métodos correspondientes en el objeto interno.</span><span class="sxs-lookup"><span data-stu-id="44646-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="44646-110">Sin embargo, cuando la complejidad de los objetos externos e internos difiere en gran medida, el objeto externo puede implementar algunos de los métodos de sus interfaces mediante la delegación de llamadas a métodos de interfaz implementados en el objeto interno.</span><span class="sxs-lookup"><span data-stu-id="44646-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="44646-111">Es fácil implementar la contención para un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="44646-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="44646-112">El objeto externo crea los objetos internos que necesita usar como cualquier otro cliente.</span><span class="sxs-lookup"><span data-stu-id="44646-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="44646-113">Esto no es nada nuevo: el proceso es como un objeto de C++ que contiene un objeto de cadena de C++ que usa para realizar determinadas funciones de cadena, incluso si el objeto externo no se considera un objeto de cadena por su derecho.</span><span class="sxs-lookup"><span data-stu-id="44646-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="44646-114">A continuación, con su puntero al objeto interno, una llamada a un método en el objeto externo genera una llamada a un método de objeto interno.</span><span class="sxs-lookup"><span data-stu-id="44646-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44646-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44646-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44646-116">Agregación</span><span class="sxs-lookup"><span data-stu-id="44646-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




