---
title: Clases estructurales, abstractas y auxiliares
description: El atributo objectClassCategory de un objeto classSchema puede tener un valor, como se muestra en la tabla siguiente, que indica si la clase es estructural, abstracta o auxiliar.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- AD de clases estructurales, abstractas y auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075098"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="b4bc3-104">Clases estructurales, abstractas y auxiliares</span><span class="sxs-lookup"><span data-stu-id="b4bc3-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="b4bc3-105">El atributo **objectClassCategory** de un objeto **ClassSchema** puede tener un valor, como se muestra en la tabla siguiente, que indica si la clase es estructural, abstracta o auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="b4bc3-106">Value</span><span class="sxs-lookup"><span data-stu-id="b4bc3-106">Value</span></span> | <span data-ttu-id="b4bc3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4bc3-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bc3-108">1</span><span class="sxs-lookup"><span data-stu-id="b4bc3-108">1</span></span>     | <span data-ttu-id="b4bc3-109">Clase estructural, que es el único tipo de clase que puede tener instancias en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="b4bc3-110">Una clase estructural puede ser una subclase de una clase abstracta o estructural.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="b4bc3-111">Una clase estructural puede incluir cualquier número de clases auxiliares en su definición.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="b4bc3-112">2</span><span class="sxs-lookup"><span data-stu-id="b4bc3-112">2</span></span>     | <span data-ttu-id="b4bc3-113">Una clase abstracta, que es una plantilla que se usa para derivar nuevas clases abstractas, auxiliares y estructurales.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="b4bc3-114">Una clase abstracta solo puede ser una subclase de una clase abstracta.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="b4bc3-115">No se pueden crear instancias de clases abstractas en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="b4bc3-116">Una clase abstracta puede incluir cualquier número de clases auxiliares en su definición.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b4bc3-117">3</span><span class="sxs-lookup"><span data-stu-id="b4bc3-117">3</span></span>     | <span data-ttu-id="b4bc3-118">Una clase auxiliar, que se puede incluir en la definición de una clase estructural, abstracta o auxiliar, en cuyo caso los valores **mustContain**, **systemMustContain**, **mayContain** y **systemMayContain** de la clase auxiliar se agregan a los de la clase.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="b4bc3-119">Una clase auxiliar puede ser una subclase de una clase abstracta o auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="b4bc3-120">No se puede crear una instancia de las clases auxiliares en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="b4bc3-121">Una clase auxiliar puede incluir cualquier número de clases auxiliares en su definición.</span><span class="sxs-lookup"><span data-stu-id="b4bc3-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="b4bc3-122">No confunda el **objectClassCategory** con una categoría de [objeto](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="b4bc3-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




