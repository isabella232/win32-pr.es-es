---
title: Clientes y servidores COM
description: Un aspecto fundamental de COM es cómo interactúan los clientes y los servidores.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776506"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="72640-103">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="72640-103">COM Clients and Servers</span></span>

<span data-ttu-id="72640-104">Un aspecto fundamental de COM es cómo interactúan los clientes y los servidores.</span><span class="sxs-lookup"><span data-stu-id="72640-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="72640-105">Un *cliente com* es el código u objeto que obtiene un puntero a un servidor com y utiliza sus servicios llamando a los métodos de sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="72640-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="72640-106">Un *servidor com* es cualquier objeto que proporcione servicios a los clientes; Estos servicios están en forma de implementaciones de interfaz COM a las que puede llamar cualquier cliente que pueda obtener un puntero a una de las interfaces en el objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="72640-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="72640-107">Hay dos tipos principales de servidores, *en proceso* y *fuera de proceso*.</span><span class="sxs-lookup"><span data-stu-id="72640-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="72640-108">Los servidores en proceso se implementan en una biblioteca de vínculos dinámicos (DLL) y los servidores fuera de proceso se implementan en un archivo ejecutable (EXE).</span><span class="sxs-lookup"><span data-stu-id="72640-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="72640-109">Los servidores fuera de proceso pueden residir en el equipo local o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="72640-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="72640-110">Además, COM proporciona un mecanismo que permite a un servidor en proceso (un archivo DLL) ejecutarse en un proceso EXE suplente para aprovechar la ventaja de poder ejecutar el proceso en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="72640-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="72640-111">Para obtener más información, vea [suplentes de dll](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="72640-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="72640-112">Ahora se han ampliado el modelo de programación COM y las construcciones para que los clientes y servidores COM puedan trabajar juntos en la red, no solo dentro de un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="72640-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="72640-113">Esto permite a las aplicaciones existentes interactuar con nuevas aplicaciones y entre sí entre redes con la administración adecuada y se pueden escribir nuevas aplicaciones para aprovechar las características de red.</span><span class="sxs-lookup"><span data-stu-id="72640-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="72640-114">No es necesario que las aplicaciones cliente COM sepan cómo se empaquetan los objetos de servidor, si se empaquetan como objetos en proceso (en archivos dll) o como objetos locales o remotos (en exe).</span><span class="sxs-lookup"><span data-stu-id="72640-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="72640-115">COM distribuido permite agregar objetos como aplicaciones de servicio, sincronizando COM con las completas capacidades administrativas y de integración del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="72640-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="72640-116">En esta documentación, el acrónimo COM se usa en preferencia a DCOM.</span><span class="sxs-lookup"><span data-stu-id="72640-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="72640-117">Esto se debe a que DCOM no es independiente; simplemente es COM con una conexión más larga.</span><span class="sxs-lookup"><span data-stu-id="72640-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="72640-118">En los casos en los que lo que se describe es específicamente una operación remota, se usa el término *com distribuido* .</span><span class="sxs-lookup"><span data-stu-id="72640-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="72640-119">COM está diseñado para que sea posible agregar la compatibilidad con la transparencia de ubicación que se extiende a través de una red.</span><span class="sxs-lookup"><span data-stu-id="72640-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="72640-120">Permite que las aplicaciones escritas para equipos individuales se ejecuten a través de una red y proporciona características que amplían estas capacidades y se agregan a la seguridad necesaria en una red.</span><span class="sxs-lookup"><span data-stu-id="72640-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="72640-121">(Para obtener más información, vea [seguridad en com](security-in-com.md)).</span><span class="sxs-lookup"><span data-stu-id="72640-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="72640-122">COM especifica un mecanismo por el que pueden usar el código de clase muchas aplicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="72640-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="72640-123">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="72640-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="72640-124">Obtener un puntero a un objeto</span><span class="sxs-lookup"><span data-stu-id="72640-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="72640-125">Crear un objeto a través de un objeto de clase</span><span class="sxs-lookup"><span data-stu-id="72640-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="72640-126">Responsabilidades del servidor COM</span><span class="sxs-lookup"><span data-stu-id="72640-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="72640-127">Estado del objeto persistente</span><span class="sxs-lookup"><span data-stu-id="72640-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="72640-128">Proporcionar información de clase</span><span class="sxs-lookup"><span data-stu-id="72640-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="72640-129">Comunicación entre objetos</span><span class="sxs-lookup"><span data-stu-id="72640-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="72640-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72640-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72640-131">Sincronización de llamadas</span><span class="sxs-lookup"><span data-stu-id="72640-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="72640-132">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="72640-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




