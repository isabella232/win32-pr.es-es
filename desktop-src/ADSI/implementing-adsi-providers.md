---
title: Implementar Active Directory proveedores de interfaces de servicio
description: Active Directory interfaces de servicio (ADSI) son interfaces COM que contienen objetos de servicio de directorio para exponerlas a los clientes de servicios de directorio. Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementar Active Directory proveedores de interfaces de servicio ADSI
- Implementación de los proveedores ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772949"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="e53dd-106">Implementar Active Directory proveedores de interfaces de servicio</span><span class="sxs-lookup"><span data-stu-id="e53dd-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="e53dd-107">Active Directory interfaces de servicio (ADSI) son interfaces COM que contienen objetos de servicio de directorio para exponerlas a los clientes de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="e53dd-108">Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente ADSI.</span><span class="sxs-lookup"><span data-stu-id="e53dd-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="e53dd-109">Al igual que con cualquier implementación COM, puede escribir un proveedor ADSI en muchos idiomas.</span><span class="sxs-lookup"><span data-stu-id="e53dd-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="e53dd-110">Las interfaces COM ADSI se definen como interfaces duales que permiten la resolución de nombres en tiempo de ejecución y en tiempo de compilación, y se pueden llamar mediante lenguajes compatibles con automatización como Visual Basic, Visual Basic Scripting Edition y también los lenguajes más conscientes del rendimiento y la eficacia, como C y C++.</span><span class="sxs-lookup"><span data-stu-id="e53dd-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="e53dd-111">Los clientes ADSI también incluyen aplicaciones web que usan Active Server páginas y complementos de administración a través de Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="e53dd-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="e53dd-112">Dado que ADSI proporciona su propio proveedor de OLE DB, la implementación de las características de búsqueda definidas por [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) también permite que los clientes ADSI consulten datos en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="e53dd-113">Todos los objetos de servicio de directorio se pueden representar mediante un objeto ADSI genérico compatible con [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="e53dd-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="e53dd-114">ADSI proporciona los bloques de creación necesarios para representar las características y los servicios de cualquier servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="e53dd-115">Además, las meta-interfaces ADSI representan objetos comunes utilizados por los administradores de directorios.</span><span class="sxs-lookup"><span data-stu-id="e53dd-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="e53dd-116">Las propiedades de las metainterfaces se asignan a las propiedades que admite el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="e53dd-117">Los clientes ADSI que programan en las interfaces de servicio Active Directory obtienen acceso a su servicio de directorio en cuanto se instala el proveedor y se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="e53dd-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="e53dd-118">Si el servicio de directorio admite una representación de esquema, la compatibilidad con las interfaces de administración de esquemas hace que el espacio de nombres sea accesible directamente para los exploradores del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="e53dd-119">Al publicar las características a través del esquema, los clientes pueden consultar el servicio de directorio en línea y aprovechar los servicios que ofrece.</span><span class="sxs-lookup"><span data-stu-id="e53dd-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="e53dd-120">Debido a la disponibilidad del esquema en línea y a la ventaja de la interfaz COM, puede seguir haciendo que las nuevas características estén disponibles para el software cliente mientras se admiten las versiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e53dd-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




