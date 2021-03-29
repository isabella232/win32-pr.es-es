---
title: Restricciones en la extensión de esquema
description: Con el fin de reducir la posibilidad de que los cambios de esquema en una aplicación interrumpan otras aplicaciones y mantengan la coherencia del esquema, Active Directory Domain Services aplicar restricciones en el tipo de cambios de esquema que puede realizar una aplicación o un usuario.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773104"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="04fd8-103">Restricciones en la extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="04fd8-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="04fd8-104">Con el fin de reducir la posibilidad de que los cambios de esquema en una aplicación interrumpan otras aplicaciones y mantengan la coherencia del esquema, Active Directory Domain Services aplicar restricciones en el tipo de cambios de esquema que puede realizar una aplicación o un usuario.</span><span class="sxs-lookup"><span data-stu-id="04fd8-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="04fd8-105">Las restricciones solo se imponen en la modificación de objetos de esquema existentes.</span><span class="sxs-lookup"><span data-stu-id="04fd8-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="04fd8-106">El esquema se clasifica en dos categorías.</span><span class="sxs-lookup"><span data-stu-id="04fd8-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="04fd8-107">Los objetos de esquema que se incluyen con Windows 2000 en el esquema base pertenecen a la categoría 1.</span><span class="sxs-lookup"><span data-stu-id="04fd8-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="04fd8-108">Los objetos de esquema agregados posteriormente por otras aplicaciones o usuarios a través de la extensión de esquema dinámico pertenecen a la categoría 2.</span><span class="sxs-lookup"><span data-stu-id="04fd8-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="04fd8-109">La categoría de un objeto de esquema se puede determinar mediante el bit 0x10 establecido en el atributo **systemFlags** en el objeto **ClassSchema** .</span><span class="sxs-lookup"><span data-stu-id="04fd8-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="04fd8-110">Este bit solo se establece en objetos de categoría 1 y no se puede modificar ni se puede establecer en ningún objeto de categoría 2.</span><span class="sxs-lookup"><span data-stu-id="04fd8-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="04fd8-111">El atributo **systemFlags** lo usa internamente Active Directory Domain Services para identificar características especiales de los objetos de "infraestructura" del esquema base.</span><span class="sxs-lookup"><span data-stu-id="04fd8-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="04fd8-112">Además de identificar objetos de categoría 1, **systemFlags** controla si un objeto se puede quitar, eliminar o cambiar de nombre.</span><span class="sxs-lookup"><span data-stu-id="04fd8-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="04fd8-113">Estas operaciones se impiden para los objetos de los que Windows 2000 depende para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="04fd8-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="04fd8-114">En cualquier objeto de esquema, categoría 1 o 2, Active Directory Domain Services imponen las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="04fd8-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="04fd8-115">No se puede Agregar un nuevo **mustContain** a una clase (directamente o a través de la herencia agregando una clase auxiliar).</span><span class="sxs-lookup"><span data-stu-id="04fd8-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="04fd8-116">No se puede eliminar ningún **mustContain** de la clase (directamente o a través de la herencia).</span><span class="sxs-lookup"><span data-stu-id="04fd8-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="04fd8-117">Además, se imponen las siguientes restricciones adicionales en los objetos de esquema de categoría 1:</span><span class="sxs-lookup"><span data-stu-id="04fd8-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="04fd8-118">No se pueden cambiar los siguientes atributos de un atributo de categoría 1:</span><span class="sxs-lookup"><span data-stu-id="04fd8-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="04fd8-119">**rangeLower** y **rangeUpper** (intervalo de valores).</span><span class="sxs-lookup"><span data-stu-id="04fd8-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="04fd8-120">**attributeSecurityGuid** (determina a qué conjunto de propiedades pertenece el atributo, si existe).</span><span class="sxs-lookup"><span data-stu-id="04fd8-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="04fd8-121">No se puede cambiar el **defaultObjectCategory** de una clase de categoría 1.</span><span class="sxs-lookup"><span data-stu-id="04fd8-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="04fd8-122">No se puede cambiar el **objectCategory** de ninguna instancia de una clase de categoría 1.</span><span class="sxs-lookup"><span data-stu-id="04fd8-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="04fd8-123">No se puede convertir una clase o atributo de categoría 1 en inactivo.</span><span class="sxs-lookup"><span data-stu-id="04fd8-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="04fd8-124">No se puede cambiar el **lDAPDisplayName** de una clase o atributo de categoría 1.</span><span class="sxs-lookup"><span data-stu-id="04fd8-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="04fd8-125">No se puede cambiar el nombre de una clase o atributo de categoría 1.</span><span class="sxs-lookup"><span data-stu-id="04fd8-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




