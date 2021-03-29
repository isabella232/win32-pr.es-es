---
title: Arquitectura de interfaces de servicio Active Directory
description: Muchos servicios de directorio son jerárquicos y, por tanto, se prestan a un modelo jerárquico de objetos. En esta sección se usan representaciones de objetos COM para ilustrar diversas características de ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory arquitectura de interfaces de servicio ADSI
- ADSI ADSI, acerca de, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773032"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="9258a-106">Arquitectura de interfaces de servicio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9258a-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="9258a-107">Muchos servicios de directorio son jerárquicos y, por tanto, se prestan a un modelo jerárquico de objetos.</span><span class="sxs-lookup"><span data-stu-id="9258a-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="9258a-108">En esta sección se usan representaciones de objetos COM para ilustrar diversas características de ADSI.</span><span class="sxs-lookup"><span data-stu-id="9258a-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="9258a-109">En la siguiente ilustración del modelo de objetos, un objeto de sistema de nivel superior contiene un objeto de espacio de nombres para cada proveedor ADSI instalado.</span><span class="sxs-lookup"><span data-stu-id="9258a-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![namespaces (objeto contenedor)](images/ds2top.png)

<span data-ttu-id="9258a-111">Cada uno de los objetos de espacio de nombres es un contenedor que contiene los nodos raíz de nivel superior de cada servidor, dominio, o cualquier otro tipo de objetos del sistema de directorio definidos como raíces en cada servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="9258a-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="9258a-112">ADSI proporciona un conjunto de interfaces y objetos predefinidos para que las aplicaciones cliente puedan interactuar con los servicios de directorio mediante un conjunto uniforme de métodos.</span><span class="sxs-lookup"><span data-stu-id="9258a-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="9258a-113">Sin embargo, es posible que ADSI no proporcione acceso a todas las características de un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="9258a-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="9258a-114">Para usar mejor el conjunto completo de características de cada servicio de directorio, ADSI proporciona un modelo de esquema que los proveedores de servicios de directorio y los proveedores de software de terceros pueden usar para extender las características más allá de las interfaces proporcionadas en ADSI.</span><span class="sxs-lookup"><span data-stu-id="9258a-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="9258a-115">Los objetos contenedores del nodo raíz, que se encuentran dentro de cada objeto de espacio de nombres del proveedor, incluyen un objeto contenedor de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="9258a-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="9258a-116">Este objeto contiene la definición de todas las características de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="9258a-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="9258a-117">Para obtener más información, vea [modelo de esquema ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="9258a-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="9258a-118">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="9258a-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="9258a-119">Active Directory objetos de interfaces de servicio</span><span class="sxs-lookup"><span data-stu-id="9258a-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="9258a-120">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="9258a-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="9258a-121">Proveedor de interfaces de servicio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9258a-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="9258a-122">Modelo de esquema ADSI</span><span class="sxs-lookup"><span data-stu-id="9258a-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




