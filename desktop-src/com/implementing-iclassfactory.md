---
title: Implementación de IClassFactory
description: Implementación de IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421441"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="9ecf3-103">Implementación de IClassFactory</span><span class="sxs-lookup"><span data-stu-id="9ecf3-103">Implementing IClassFactory</span></span>

<span data-ttu-id="9ecf3-104">Cuando un cliente usa un CLSID para solicitar la creación de una instancia de objeto, el primer paso es la creación de un objeto de clase, un objeto intermedio que contiene una implementación de los métodos de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .</span><span class="sxs-lookup"><span data-stu-id="9ecf3-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="9ecf3-105">Aunque COM proporciona varias funciones de creación de instancias, el primer paso en la implementación de estas funciones es la creación de un objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="9ecf3-106">Como resultado, todos los servidores deben implementar los métodos de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , que contiene dos métodos:</span><span class="sxs-lookup"><span data-stu-id="9ecf3-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="9ecf3-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="9ecf3-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="9ecf3-108">Este método debe crear una instancia no inicializada del objeto y devolver un puntero a una interfaz solicitada en el objeto.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="9ecf3-109">[**Lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="9ecf3-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="9ecf3-110">Este método solo incrementa el recuento de referencias en el objeto de clase para asegurarse de que el servidor permanece en la memoria y no se apaga antes de que el cliente esté listo para que lo haga.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="9ecf3-111">Para permitir que un servidor sea responsable de sus propias licencias, COM define [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), que hereda su definición de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="9ecf3-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="9ecf3-112">Por lo tanto, un servidor que implementa **IClassFactory2** debe implementar los métodos de **IClassFactory**, por definición.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="9ecf3-113">COM también proporciona funciones auxiliares para implementar servidores fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="9ecf3-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="9ecf3-114">Para obtener más información, vea [aplicaciones auxiliares de implementación de servidor fuera de proceso](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="9ecf3-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ecf3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ecf3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ecf3-116">Responsabilidades del servidor COM</span><span class="sxs-lookup"><span data-stu-id="9ecf3-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="9ecf3-117">Licencias y IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="9ecf3-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 