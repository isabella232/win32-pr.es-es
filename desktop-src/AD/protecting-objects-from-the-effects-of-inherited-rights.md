---
title: Protección de objetos a partir de los efectos de los derechos heredados
description: Como se describe en el tema herencia y delegación de la administración, las ACE se pueden establecer en un objeto contenedor, como organizationalUnit, domainDNS, contenedor, etc., y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protección de objetos a partir de los efectos de AD de derechos heredados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077505"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="5b875-104">Protección de objetos a partir de los efectos de los derechos heredados</span><span class="sxs-lookup"><span data-stu-id="5b875-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="5b875-105">Como se describe en el tema [herencia y delegación de la administración](inheritance-and-delegation-of-administration.md), las ACE se pueden establecer en un objeto contenedor, como **organizationalUnit**, **domainDNS**, **contenedor**, etc., y propagarse a objetos secundarios en función de las marcas ACE establecidas en esas ACE.</span><span class="sxs-lookup"><span data-stu-id="5b875-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="5b875-106">Si tiene un objeto seguro o un objeto cuyas ACE desea controlar explícitamente, como una unidad organizativa privada o un usuario especial, puede evitar que las ACE se propaguen al objeto por su contenedor primario o sus predecesoras del contenedor principal.</span><span class="sxs-lookup"><span data-stu-id="5b875-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="5b875-107">Use la propiedad [**IADsSecurityDescriptor. control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar si el objeto hereda DACL y SACL de su contenedor primario.</span><span class="sxs-lookup"><span data-stu-id="5b875-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="5b875-108">La propiedad [**IADsSecurityDescriptor. control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) se puede usar para proteger un objeto de los efectos de las ACE heredadas.</span><span class="sxs-lookup"><span data-stu-id="5b875-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="5b875-109">Las marcas siguientes obligan a que el control de acceso se establezca explícitamente en el objeto e impidan que un usuario modifique el control de acceso al objeto mediante el establecimiento de ACE heredables en el contenedor primario del objeto o de sus predecesores principales.</span><span class="sxs-lookup"><span data-stu-id="5b875-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="5b875-110">Marca</span><span class="sxs-lookup"><span data-stu-id="5b875-110">Flag</span></span>                               | <span data-ttu-id="5b875-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b875-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b875-112">**DACL de SE \_ \_ protegió**</span><span class="sxs-lookup"><span data-stu-id="5b875-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="5b875-113">Impide que se apliquen las ACE establecidas en la DACL del contenedor principal y los objetos situados por encima del contenedor primario en la jerarquía de directorios a la DACL de objeto.</span><span class="sxs-lookup"><span data-stu-id="5b875-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="5b875-114">**SE \_ \_ protegió SACL**</span><span class="sxs-lookup"><span data-stu-id="5b875-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="5b875-115">Impide que se apliquen las ACE establecidas en la SACL del contenedor principal y los objetos situados por encima del contenedor primario en la jerarquía de directorios a la SACL del objeto.</span><span class="sxs-lookup"><span data-stu-id="5b875-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="5b875-116">Tenga en cuenta que la marca de **DACL de se \_ \_** debe presentar para establecer que la **\_ DACL \_ protegida** y la **SACL de se \_ \_** presente deben estar presentes para establecer la **\_ SACL \_ protegida**.</span><span class="sxs-lookup"><span data-stu-id="5b875-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 

