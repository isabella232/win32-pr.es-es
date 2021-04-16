---
title: Extender el esquema
description: El esquema del servicio de directorio de Active Directory define los atributos y las clases que se usan en Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, esquema, extender el esquema
- esquema AD, extensión del esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656340"
---
# <a name="extending-the-schema"></a><span data-ttu-id="60845-105">Extender el esquema</span><span class="sxs-lookup"><span data-stu-id="60845-105">Extending the Schema</span></span>

<span data-ttu-id="60845-106">El esquema del servicio de directorio de Active Directory define los atributos y las clases que se usan en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="60845-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="60845-107">El esquema base incluido en el sistema contiene un conjunto completo de definiciones de clase, como **User**, **Computer** y **organizationalUnit**, y definiciones de atributos, como **userPrincipalName**, **telephoneNumber** y **objectSid**.</span><span class="sxs-lookup"><span data-stu-id="60845-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="60845-108">El conjunto existente de clases y atributos será suficiente para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="60845-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="60845-109">Sin embargo, el esquema es extensible, lo que significa que puede definir nuevas clases y atributos.</span><span class="sxs-lookup"><span data-stu-id="60845-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="60845-110">En esta sección se describe cómo extender el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60845-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="60845-111">Cuándo extender el esquema</span><span class="sxs-lookup"><span data-stu-id="60845-111">When to Extend the Schema</span></span>

<span data-ttu-id="60845-112">Si las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, debe extender el esquema.</span><span class="sxs-lookup"><span data-stu-id="60845-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="60845-113">Es importante tener en cuenta que las adiciones de esquema son permanentes; puede deshabilitar clases y atributos, pero nunca puede quitarlos del esquema.</span><span class="sxs-lookup"><span data-stu-id="60845-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="60845-114">Tenga esto en cuenta al probar el código.</span><span class="sxs-lookup"><span data-stu-id="60845-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="60845-115">También tenga en cuenta el tamaño de los datos que desea almacenar.</span><span class="sxs-lookup"><span data-stu-id="60845-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="60845-116">Microsoft recomienda que ningún valor de atributo supere los 500 kilobytes, incluida la suma de los atributos multivalor.</span><span class="sxs-lookup"><span data-stu-id="60845-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="60845-117">Además, los objetos no deben tener un tamaño superior a 1 megabyte.</span><span class="sxs-lookup"><span data-stu-id="60845-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="60845-118">Considere también el número de instancias de los datos; Si agrega un nuevo atributo a la clase de [**usuario**](/windows/desktop/ADSchema/c-user) en un sistema que tiene 100.000 usuarios, puede usar un espacio considerable.</span><span class="sxs-lookup"><span data-stu-id="60845-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="60845-119">Los temas de esta sección incluyen:</span><span class="sxs-lookup"><span data-stu-id="60845-119">Topics in this section include:</span></span>

-   <span data-ttu-id="60845-120">Cómo enlazar con el contenedor de esquema y leer las propiedades de las clases y atributos existentes.</span><span class="sxs-lookup"><span data-stu-id="60845-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="60845-121">Cómo y cuándo extender el esquema definiendo nuevos atributos y clases.</span><span class="sxs-lookup"><span data-stu-id="60845-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="60845-122">Cómo instalar extensiones de esquema mediante LDIFDE, CSVDE o mediante programación con ADSI.</span><span class="sxs-lookup"><span data-stu-id="60845-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="60845-123">Para obtener más información y una información general sobre el esquema de Active Directory, incluida la información sobre la implementación del esquema, las definiciones de clase y las definiciones de atributo, vea [Active Directory esquema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="60845-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="60845-124">Para obtener más información, incluidas las páginas de referencia de las clases de esquema predefinidas, los atributos y las sintaxis de atributo, vea la referencia de esquemas de Active Directory en la [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60845-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 