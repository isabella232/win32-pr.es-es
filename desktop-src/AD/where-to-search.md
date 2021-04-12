---
title: Decidir dónde buscar
description: En este tema se explican las diferentes búsquedas que se pueden realizar en Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidir dónde buscar en AD
- Active Directory AD, buscar, decidir dónde buscar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358794"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="3ffd4-105">Decidir dónde buscar</span><span class="sxs-lookup"><span data-stu-id="3ffd4-105">Deciding Where to Search</span></span>

<span data-ttu-id="3ffd4-106">En este tema se explican las diferentes búsquedas que se pueden realizar en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="3ffd4-107">Todas las búsquedas se realizan en uno de los siguientes contextos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="3ffd4-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="3ffd4-108">Dominio, incluidas las particiones de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3ffd4-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="3ffd4-109">Contenedor de esquema</span><span class="sxs-lookup"><span data-stu-id="3ffd4-109">Schema container</span></span>
-   <span data-ttu-id="3ffd4-110">Contenedor de configuración</span><span class="sxs-lookup"><span data-stu-id="3ffd4-110">Configuration container</span></span>
-   <span data-ttu-id="3ffd4-111">Catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffd4-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="3ffd4-112">Buscar un dominio</span><span class="sxs-lookup"><span data-stu-id="3ffd4-112">Searching a Domain</span></span>

<span data-ttu-id="3ffd4-113">Los dominios contienen la mayoría de los objetos muy utilizados, como usuarios, contactos, grupos, unidades organizativas, equipos, etc.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="3ffd4-114">La mayoría de las consultas buscarán en un dominio.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-114">Most queries will search a domain.</span></span> <span data-ttu-id="3ffd4-115">Para obtener más información acerca de la búsqueda de un dominio, vea Buscar en el [contenido del dominio](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="3ffd4-116">Buscar en el contenedor de esquemas</span><span class="sxs-lookup"><span data-stu-id="3ffd4-116">Searching the Schema Container</span></span>

<span data-ttu-id="3ffd4-117">El contenedor de esquemas contiene los objetos [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) y [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que proporcionan la definición formal de cada clase y atributo que puede existir en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="3ffd4-118">Para buscar objetos en el contenedor de esquemas, enlace al contenedor de esquemas en cualquier controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="3ffd4-119">El contenedor de esquema está disponible en todos los controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="3ffd4-120">El nombre distintivo del contenedor de esquema se obtiene del atributo **schemaNamingContext** de RootDSE.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="3ffd4-121">Para obtener más información acerca de rootDSE y el atributo **schemaNamingContext** , vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="3ffd4-122">Para obtener más información sobre cómo leer el esquema o el contenedor de esquemas abstractos, vea [instrucciones para enlazar con el esquema](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="3ffd4-123">Buscar en el contenedor de configuración</span><span class="sxs-lookup"><span data-stu-id="3ffd4-123">Searching the Configuration Container</span></span>

<span data-ttu-id="3ffd4-124">El contenedor de configuración contiene información de configuración, como sitios, servicios y especificadores de presentación, para todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="3ffd4-125">Para buscar objetos en el contenedor de configuración, enlace al contenedor de configuración en cualquier controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="3ffd4-126">El contenedor de configuración está disponible en todos los controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="3ffd4-127">El nombre distintivo del contenedor de configuración se obtiene del atributo **configurationNamingContext** de RootDSE.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="3ffd4-128">Para obtener más información sobre rootDSE y el atributo **configurationNamingContext** , vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="3ffd4-129">Buscar en el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ffd4-129">Searching the Global Catalog</span></span>

<span data-ttu-id="3ffd4-130">El catálogo global contiene una réplica de cada objeto en Active Directory Domain Services, pero solo con un número pequeño de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="3ffd4-131">Los atributos del catálogo global son los que se usan con más frecuencia en las operaciones de búsqueda, como el nombre y los apellidos de un usuario, los nombres de inicio de sesión, etc.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="3ffd4-132">Para obtener más información acerca de la búsqueda en el catálogo global, vea [Buscar en el catálogo global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 