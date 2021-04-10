---
description: El editor de control de acceso puede incluir una página de propiedades de propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de los objetos, vea propietario de un nuevo objeto y tomar posesión de objetos en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propiedades propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156776"
---
# <a name="owner-property-page"></a><span data-ttu-id="57806-104">Página de propiedades propietario</span><span class="sxs-lookup"><span data-stu-id="57806-104">Owner Property Page</span></span>

<span data-ttu-id="57806-105">El editor de control de acceso puede incluir una página de propiedades de propietario que permite al usuario cambiar el propietario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="57806-105">The access control editor can include an Owner property page that enables the user to change an object's owner.</span></span> <span data-ttu-id="57806-106">Para obtener más información sobre el propietario de un objeto, vea [propietario de un nuevo objeto](owner-of-a-new-object.md) y [tomar posesión de objetos en C++](taking-object-ownership-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="57806-106">For more information about an object's owner, see [Owner of a New Object](owner-of-a-new-object.md) and [Taking Object Ownership in C++](taking-object-ownership-in-c--.md).</span></span>

<span data-ttu-id="57806-107">La página de propiedades **propietario** está en la [hoja de propiedades seguridad avanzada](advanced-security-property-sheet.md) que se muestra cuando el usuario hace clic en el botón **avanzadas** de la [Página de propiedades seguridad básica](basic-security-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="57806-107">The **Owner** property page is in the [advanced security property sheet](advanced-security-property-sheet.md) displayed when the user clicks the **Advanced** button on the [basic security property page](basic-security-property-page.md).</span></span> <span data-ttu-id="57806-108">Para incluir la página de propiedades del **propietario** , establezca las \_ marcas si y \_ Editar \_ propietario en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devueltos por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="57806-108">To include the **Owner** property page, set the SI\_ADVANCED and SI\_EDIT\_OWNER flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
