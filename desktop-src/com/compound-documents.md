---
title: Documentos compuestos
description: Los documentos compuestos OLE permiten a los usuarios que trabajan en una sola aplicación manipular los datos escritos en varios formatos y se derivan de varios orígenes.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149677"
---
# <a name="compound-documents"></a><span data-ttu-id="52645-103">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="52645-103">Compound Documents</span></span>

<span data-ttu-id="52645-104">Los documentos compuestos OLE permiten a los usuarios que trabajan en una sola aplicación manipular los datos escritos en varios formatos y se derivan de varios orígenes.</span><span class="sxs-lookup"><span data-stu-id="52645-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="52645-105">Por ejemplo, un usuario podría insertar en un documento de procesamiento de texto un gráfico creado en una segunda aplicación y un objeto de sonido creado en una tercera aplicación.</span><span class="sxs-lookup"><span data-stu-id="52645-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="52645-106">La activación del gráfico hace que la segunda aplicación cargue su interfaz de usuario, o al menos esa parte que contenga las herramientas necesarias para editar el objeto.</span><span class="sxs-lookup"><span data-stu-id="52645-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="52645-107">Al activar el objeto de sonido, la tercera aplicación lo reproduce.</span><span class="sxs-lookup"><span data-stu-id="52645-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="52645-108">En ambos casos, un usuario puede manipular los datos de orígenes externos desde dentro del contexto de un solo documento.</span><span class="sxs-lookup"><span data-stu-id="52645-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="52645-109">La tecnología de documentos compuestos de OLE se sitúa en una base compuesta por COM, almacenamiento estructurado y transferencia de datos uniforme.</span><span class="sxs-lookup"><span data-stu-id="52645-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="52645-110">Como se resume a continuación, cada una de estas tecnologías principales desempeña un papel fundamental en los documentos compuestos OLE:</span><span class="sxs-lookup"><span data-stu-id="52645-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="52645-111"><span id="COM"></span><span id="com"></span>COM</span><span class="sxs-lookup"><span data-stu-id="52645-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="52645-112">Un objeto de documento compuesto es esencialmente un objeto COM que se puede incrustar o vincular a un documento existente.</span><span class="sxs-lookup"><span data-stu-id="52645-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="52645-113">Como objeto COM, un objeto de documento compuesto expone la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , a través de la cual los clientes pueden obtener punteros a sus otras interfaces, incluidas varias, como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)y [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), que proporcionan características especiales exclusivas de los objetos de documento compuestos.</span><span class="sxs-lookup"><span data-stu-id="52645-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="52645-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="52645-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="52645-115">Un objeto de documento compuesto debe implementar las interfaces [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) o, opcionalmente, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para administrar su propio almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="52645-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="52645-116">Un contenedor que se usa para crear documentos compuestos debe proporcionar la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , a través de la cual los objetos almacenan y recuperan datos.</span><span class="sxs-lookup"><span data-stu-id="52645-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="52645-117">Los contenedores casi siempre proporcionan instancias de **IStorage** obtenidas de la implementación de archivos compuestos de OLE.</span><span class="sxs-lookup"><span data-stu-id="52645-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="52645-118">Los contenedores también deben usar las interfaces **IPersistStorage** y/o **IPersistStream** de un objeto.</span><span class="sxs-lookup"><span data-stu-id="52645-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="52645-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferencia de datos uniformes</span><span class="sxs-lookup"><span data-stu-id="52645-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="52645-120">Las aplicaciones que admiten documentos compuestos deben implementar [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , ya que los objetos incrustados y los objetos vinculados comienzan como datos transferidos mediante formatos de Portapapeles OLE especiales, en lugar de formatos de Portapapeles de Microsoft Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="52645-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="52645-121">En otras palabras, el formato de los datos como un objeto incrustado o vinculado es simplemente una opción más proporcionada por el modelo de transferencia de datos uniforme de OLE.</span><span class="sxs-lookup"><span data-stu-id="52645-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="52645-122">La tecnología de documentos compuestos de OLE beneficia a los desarrolladores de software y a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="52645-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="52645-123">En lugar de sentirse obligado a CRAM cada característica imaginable en una sola aplicación, los desarrolladores de software ahora son gratis, si lo desean, para desarrollar aplicaciones más pequeñas y más centradas que se basan en otras aplicaciones para proporcionar características adicionales.</span><span class="sxs-lookup"><span data-stu-id="52645-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="52645-124">En los casos en los que un desarrollador de software decide proporcionar una aplicación con funcionalidades más allá de sus características principales, el desarrollador puede implementar estos servicios adicionales como archivos dll independientes, que se cargan en la memoria solo cuando se requieren sus servicios.</span><span class="sxs-lookup"><span data-stu-id="52645-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="52645-125">Los usuarios se benefician del software más pequeño, más rápido y más sencillo que pueden combinar y hacer coincidir según sea necesario, manipulando todos los componentes necesarios de dentro de un único documento maestro.</span><span class="sxs-lookup"><span data-stu-id="52645-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="52645-126">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="52645-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="52645-127">Contenedores y servidores</span><span class="sxs-lookup"><span data-stu-id="52645-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="52645-128">Vinculación e incrustación</span><span class="sxs-lookup"><span data-stu-id="52645-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="52645-129">Controladores de objetos</span><span class="sxs-lookup"><span data-stu-id="52645-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="52645-130">Servidores en proceso</span><span class="sxs-lookup"><span data-stu-id="52645-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="52645-131">Objetos y monikers vinculados</span><span class="sxs-lookup"><span data-stu-id="52645-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="52645-132">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="52645-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="52645-133">Interfaces de documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="52645-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="52645-134">Estados de objeto</span><span class="sxs-lookup"><span data-stu-id="52645-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="52645-135">Implementación de la activación de In-Place</span><span class="sxs-lookup"><span data-stu-id="52645-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="52645-136">Crear objetos vinculados e incrustados a partir de datos existentes</span><span class="sxs-lookup"><span data-stu-id="52645-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="52645-137">Ver almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="52645-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="52645-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52645-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52645-139">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="52645-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="52645-140">Almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="52645-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 