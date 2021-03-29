---
title: Responsabilidades del servidor COM
description: Responsabilidades del servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421461"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="be23c-103">Responsabilidades del servidor COM</span><span class="sxs-lookup"><span data-stu-id="be23c-103">COM Server Responsibilities</span></span>

<span data-ttu-id="be23c-104">Una de las formas más importantes de que un cliente obtenga un puntero a un objeto es que el cliente pida que se inicie un servidor y que se cree y active una instancia del objeto proporcionado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="be23c-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="be23c-105">Es responsabilidad del servidor asegurarse de que esto se produce correctamente.</span><span class="sxs-lookup"><span data-stu-id="be23c-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="be23c-106">Hay varias partes importantes para esto.</span><span class="sxs-lookup"><span data-stu-id="be23c-106">There are several important parts to this.</span></span>

<span data-ttu-id="be23c-107">El servidor debe implementar código para un objeto de clase a través de una implementación de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .</span><span class="sxs-lookup"><span data-stu-id="be23c-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="be23c-108">El servidor debe registrar su CLSID en el registro del sistema en el equipo en el que reside y, además, tiene la opción de publicar su ubicación de equipo en otros sistemas de una red para que los clientes puedan llamarla sin necesidad de que el cliente conozca la ubicación del servidor.</span><span class="sxs-lookup"><span data-stu-id="be23c-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="be23c-109">El servidor es responsable principalmente de la seguridad; es decir, en la mayor parte, el servidor determina si proporcionará un puntero a uno de sus objetos a un cliente.</span><span class="sxs-lookup"><span data-stu-id="be23c-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="be23c-110">Los servidores en proceso deben implementar y exportar ciertas funciones que permiten al proceso del cliente crear instancias de ellas.</span><span class="sxs-lookup"><span data-stu-id="be23c-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="be23c-111">En los temas siguientes se detallan las responsabilidades del servidor COM:</span><span class="sxs-lookup"><span data-stu-id="be23c-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="be23c-112">Implementación de IClassFactory</span><span class="sxs-lookup"><span data-stu-id="be23c-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="be23c-113">Licencias y IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="be23c-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="be23c-114">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="be23c-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="be23c-115">Aplicaciones auxiliares de implementación de servidor fuera de proceso</span><span class="sxs-lookup"><span data-stu-id="be23c-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="be23c-116">Creación y optimización de GUID</span><span class="sxs-lookup"><span data-stu-id="be23c-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="be23c-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be23c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be23c-118">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="be23c-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 