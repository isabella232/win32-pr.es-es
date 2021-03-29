---
title: Objetos e interfaces COM
description: Objetos e interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773321"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="e9356-103">Objetos e interfaces COM</span><span class="sxs-lookup"><span data-stu-id="e9356-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="e9356-104">COM es una tecnología que permite a los objetos interactuar a través de los límites de equipos y procesos tan fácilmente como dentro de un único proceso.</span><span class="sxs-lookup"><span data-stu-id="e9356-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="e9356-105">COM lo habilita especificando que la única manera de manipular los datos asociados a un objeto es a través de una *interfaz* en el objeto.</span><span class="sxs-lookup"><span data-stu-id="e9356-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="e9356-106">Cuando este término se usa en esta documentación, hace referencia a una implementación en el código de una interfaz compatible con binario COM que está asociada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="e9356-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="e9356-107">COM utiliza la *interfaz* de Word en un sentido diferente del que se usa normalmente en la programación de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="e9356-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="e9356-108">Una interfaz de C++ hace referencia a todas las funciones que admite una clase y a la que los clientes de un objeto pueden llamar para interactuar con ella.</span><span class="sxs-lookup"><span data-stu-id="e9356-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="e9356-109">Una interfaz COM hace referencia a un grupo predefinido de funciones relacionadas que implementa una clase COM, pero una interfaz concreta no representa necesariamente todas las funciones que admite la clase.</span><span class="sxs-lookup"><span data-stu-id="e9356-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="e9356-110">La referencia a un objeto que *implementa* una interfaz significa que el objeto utiliza código que implementa cada método de la interfaz y proporciona punteros com compatibles con binario a esas funciones a la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="e9356-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="e9356-111">COM hace que estas funciones estén disponibles para cualquier cliente que solicite un puntero a la interfaz, tanto si el cliente está dentro o fuera del proceso que implementa esas funciones.</span><span class="sxs-lookup"><span data-stu-id="e9356-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="e9356-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9356-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e9356-113">Interfaces e implementaciones de interfaz</span><span class="sxs-lookup"><span data-stu-id="e9356-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   <span data-ttu-id="e9356-114">[Interface Pointers and Interfaces](interface-pointers-and-interfaces.md) (Punteros de interfaz e interfaces)</span><span class="sxs-lookup"><span data-stu-id="e9356-114">[Interface Pointers and Interfaces](interface-pointers-and-interfaces.md)</span></span>
-   [<span data-ttu-id="e9356-115">IUnknown y herencia de interfaz</span><span class="sxs-lookup"><span data-stu-id="e9356-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="e9356-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9356-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9356-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e9356-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




