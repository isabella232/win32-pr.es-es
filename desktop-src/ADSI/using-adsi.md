---
title: Uso de interfaces de servicio Active Directory
description: Active Directory interfaces de servicio (ADSI) proporciona el medio para que las aplicaciones cliente de servicios de directorio utilicen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporcione una implementación de ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Usar interfaces de servicio de Active Directory ADSI
- ADSI ADSI, usar
- Interfaces de servicio de Active Directory ADSI, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903019"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="2ff6a-106">Uso de interfaces de servicio Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ff6a-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="2ff6a-107">Active Directory interfaces de servicio (ADSI) proporciona el medio para que las aplicaciones cliente de servicios de directorio utilicen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporcione una implementación de ADSI.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="2ff6a-108">Los clientes ADSI usan las interfaces de servicio Active Directory bien definidas en lugar de las llamadas API específicas de la red para obtener acceso más sencillo a los servicios de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="2ff6a-109">Active Directory interfaces de servicio se ajustan al modelo de objetos componentes (COM) y son compatibles con las características COM estándar.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="2ff6a-110">ADSI proporciona interfaces que son compatibles con la automatización para controladores enlazados a nombres como Java, Microsoft Visual Basic Development System y Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2ff6a-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="2ff6a-111">ADSI también puede proporcionar una interfaz que puede optimizar el rendimiento de las interfaces que no son compatibles con la automatización, para usarlas con entornos de lenguaje como C y C++.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="2ff6a-112">ADSI también proporciona las interfaces que no son de automatización, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) y [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), para admitir las consultas y la administración de objetos de directorio.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="2ff6a-113">Además, ADSI proporciona su propio proveedor de OLE DB, por lo que cualquier cliente que ya use OLE DB, incluidos los que usan Objetos de datos ActiveX, puede consultar directamente los servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="2ff6a-114">Las aplicaciones web que usan páginas de Active Server también pueden programar el acceso a los servicios de directorio a través de ADSI.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="2ff6a-115">Los clientes ADSI pueden detectar mediante programación todos los proveedores ADSI en un sitio y utilizar las mismas interfaces para comunicarse con cada espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="2ff6a-116">A medida que se instalan proveedores adicionales, los clientes ADSI pueden comunicarse, sin volver a compilar, también con los nuevos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="2ff6a-117">Esta guía de programación describe cómo funciona ADSI y proporciona información para realizar tareas específicas en ADSI.</span><span class="sxs-lookup"><span data-stu-id="2ff6a-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="2ff6a-118">Se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ff6a-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="2ff6a-119">Enlazar a un objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="2ff6a-120">Crear y eliminar objetos</span><span class="sxs-lookup"><span data-stu-id="2ff6a-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="2ff6a-121">Obtener acceso a los datos y manipularlos con ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="2ff6a-122">Usar el esquema ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="2ff6a-123">Colecciones y grupos</span><span class="sxs-lookup"><span data-stu-id="2ff6a-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="2ff6a-124">Enumerar objetos ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="2ff6a-125">Buscar Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ff6a-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="2ff6a-126">Modelo de seguridad ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="2ff6a-127">Extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="2ff6a-128">Usar ADSI con Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff6a-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="2ff6a-129">Interfaces de la utilidad ADSI</span><span class="sxs-lookup"><span data-stu-id="2ff6a-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="2ff6a-130">Programar ADSI con Java/COM</span><span class="sxs-lookup"><span data-stu-id="2ff6a-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




