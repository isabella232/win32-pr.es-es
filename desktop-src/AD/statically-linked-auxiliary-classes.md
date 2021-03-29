---
title: Clases auxiliares vinculadas estáticamente
description: Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo auxiliaryClass o systemAuxiliaryClass de la definición de classSchema de una clase de objeto en el esquema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Clases auxiliares vinculadas estáticamente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773074"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="0526d-104">Clases auxiliares vinculadas estáticamente</span><span class="sxs-lookup"><span data-stu-id="0526d-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="0526d-105">Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo **auxiliaryClass** o **systemAuxiliaryClass** de la definición de **ClassSchema** de una clase de objeto en el esquema.</span><span class="sxs-lookup"><span data-stu-id="0526d-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="0526d-106">Esto significa que la clase auxiliar forma parte de cada instancia de la clase a la que está asociada.</span><span class="sxs-lookup"><span data-stu-id="0526d-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="0526d-107">Una clase auxiliar puede vincularse estáticamente a una clase de objeto cuando se define la clase, es decir, cuando su objeto **ClassSchema** se agrega al contenedor de esquemas.</span><span class="sxs-lookup"><span data-stu-id="0526d-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="0526d-108">Esta es la única vez que se puede usar el **systemAuxiliaryClass** ; una vez creado el objeto **ClassSchema** , no se puede modificar su atributo **systemAuxiliaryClass** .</span><span class="sxs-lookup"><span data-stu-id="0526d-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="0526d-109">Una clase auxiliar vinculada estáticamente en este momento puede tener atributos obligatorios (**mustHave**) y/o opcionales (**mayHave**).</span><span class="sxs-lookup"><span data-stu-id="0526d-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="0526d-110">Un usuario con privilegios que tenga los permisos necesarios para extender el esquema puede Agregar o quitar clases auxiliares del atributo **systemAuxiliaryClass** de un objeto **ClassSchema** existente.</span><span class="sxs-lookup"><span data-stu-id="0526d-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="0526d-111">Al hacerlo, se agrega o se quita la clase auxiliar de cada instancia existente de la clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="0526d-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="0526d-112">Una clase auxiliar vinculada estáticamente en este momento puede tener atributos opcionales, pero no puede tener atributos obligatorios.</span><span class="sxs-lookup"><span data-stu-id="0526d-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="0526d-113">Esto se debe a que puede haber instancias existentes de la clase de objeto, en cuyo caso agregar un nuevo atributo obligatorio crearía problemas.</span><span class="sxs-lookup"><span data-stu-id="0526d-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="0526d-114">Posteriormente, un usuario con privilegios puede quitar una clase auxiliar del atributo **auxiliaryClass** de un objeto **ClassSchema** .</span><span class="sxs-lookup"><span data-stu-id="0526d-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




