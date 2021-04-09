---
title: Access Control y creación de objetos
description: El servidor de Active Directory no podrá crear un objeto secundario si el autor de la llamada no tiene el \_ derecho \_ ad \_ Create DS secundario \_ para ese tipo de objeto en el contenedor primario.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Access Control y creación de objetos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149153"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="696f2-104">Access Control y creación de objetos</span><span class="sxs-lookup"><span data-stu-id="696f2-104">Access Control and Object Creation</span></span>

<span data-ttu-id="696f2-105">El servidor de Active Directory no podrá crear un objeto secundario si el autor de la llamada no tiene **el \_ derecho \_ ad \_ Create \_ DS secundario** para ese tipo de objeto en el contenedor primario.</span><span class="sxs-lookup"><span data-stu-id="696f2-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="696f2-106">Para determinar los tipos de objetos secundarios que el autor de la llamada puede crear en un objeto de directorio, lea el atributo **allowedChildClassesEffective** del objeto.</span><span class="sxs-lookup"><span data-stu-id="696f2-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="696f2-107">Cuando se usa el método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para crear un objeto secundario, el objeto no se hace persistente hasta que se llama a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) en el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="696f2-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="696f2-108">Entre las llamadas a **Create** y **SetInfo** , el subproceso de creación puede colocar valores en cualquiera de las propiedades del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="696f2-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="696f2-109">Después de la llamada a **SetInfo** , el subproceso de creación no tiene necesariamente los derechos de acceso para establecer las propiedades del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="696f2-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="696f2-110">Para asegurarse de que el autor de la llamada tenga estos derechos, especifique un descriptor de seguridad explícito durante la creación.</span><span class="sxs-lookup"><span data-stu-id="696f2-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="696f2-111">La DACL debe tener una ACE que proporcione al llamador los derechos de acceso necesarios en el objeto.</span><span class="sxs-lookup"><span data-stu-id="696f2-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="696f2-112">Para obtener más información sobre el control de acceso y la creación de objetos, vea [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="696f2-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 