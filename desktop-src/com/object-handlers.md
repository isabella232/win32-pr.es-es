---
title: Controladores de objetos
description: Controladores de objetos
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903224"
---
# <a name="object-handlers"></a><span data-ttu-id="b5951-103">Controladores de objetos</span><span class="sxs-lookup"><span data-stu-id="b5951-103">Object Handlers</span></span>

<span data-ttu-id="b5951-104">Si una aplicación de servidor OLE es un servidor local, lo que significa que se ejecuta en su propio espacio de proceso, la comunicación entre el contenedor y el servidor debe realizarse a través de los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="b5951-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="b5951-105">Dado que este proceso es costoso, OLE se basa en un objeto suplente cargado en el espacio de proceso del contenedor para que actúe en nombre de una aplicación de servidor local.</span><span class="sxs-lookup"><span data-stu-id="b5951-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="b5951-106">Este objeto suplente, conocido como *controlador de objetos*, solicita a los servicios las solicitudes que no requieren la atención de la aplicación de servidor, como las solicitudes de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b5951-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="b5951-107">Cuando un contenedor solicita algo que el controlador de objetos no puede proporcionar, el controlador se comunica con la aplicación de servidor mediante el mecanismo de comunicación fuera de proceso de COM.</span><span class="sxs-lookup"><span data-stu-id="b5951-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="b5951-108">Un controlador de objetos es único para una clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="b5951-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="b5951-109">Cuando se crea una instancia de un controlador para una clase, no se puede utilizar para otro.</span><span class="sxs-lookup"><span data-stu-id="b5951-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="b5951-110">Cuando se usa para un documento compuesto, el controlador de objetos implementa las estructuras de datos del contenedor cuando se tiene acceso remoto a los objetos de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="b5951-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="b5951-111">OLE proporciona un controlador de objetos predeterminado que pueden usar las aplicaciones de servidor locales.</span><span class="sxs-lookup"><span data-stu-id="b5951-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="b5951-112">En el caso de las aplicaciones que requieren comportamientos especiales, los desarrolladores pueden implementar un controlador personalizado que reemplace el controlador predeterminado o lo use para proporcionar determinados comportamientos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b5951-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="b5951-113">Un controlador de objetos es un archivo DLL que contiene varios componentes que interactúan.</span><span class="sxs-lookup"><span data-stu-id="b5951-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="b5951-114">Estos componentes incluyen piezas de comunicación remota para administrar la comunicación entre el controlador y su aplicación de servidor, una memoria caché para almacenar los datos de un objeto, junto con información sobre cómo deben aplicarse formato y mostrar los datos, y un objeto de control que coordina las actividades de los demás componentes del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b5951-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="b5951-115">Además, si un objeto es un vínculo, el archivo DLL también incluye un componente de vinculación, o un *objeto vinculado*, que realiza un seguimiento del nombre y la ubicación del origen del vínculo.</span><span class="sxs-lookup"><span data-stu-id="b5951-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="b5951-116">La *memoria caché* contiene datos e información de presentación suficientes para que el controlador muestre un objeto cargado pero no en ejecución en su contenedor.</span><span class="sxs-lookup"><span data-stu-id="b5951-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="b5951-117">OLE proporciona una implementación de la memoria caché utilizada por el controlador de objetos predeterminado de OLE y el objeto de vínculo.</span><span class="sxs-lookup"><span data-stu-id="b5951-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="b5951-118">La memoria caché almacena los datos en formatos necesarios para que el controlador de objetos satisfaga las solicitudes de dibujo del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b5951-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="b5951-119">Cuando los datos de un objeto cambian, el objeto envía una notificación a la memoria caché para que se pueda producir una actualización.</span><span class="sxs-lookup"><span data-stu-id="b5951-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="b5951-120">Para obtener más información sobre la memoria caché, vea [ver el almacenamiento en caché](view-caching.md).</span><span class="sxs-lookup"><span data-stu-id="b5951-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="b5951-121">Para obtener más información, consulte el siguiente tema:</span><span class="sxs-lookup"><span data-stu-id="b5951-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="b5951-122">Controlador predeterminado y controladores personalizados</span><span class="sxs-lookup"><span data-stu-id="b5951-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="b5951-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5951-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5951-124">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="b5951-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




