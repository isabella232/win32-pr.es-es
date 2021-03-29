---
description: El editor de control de acceso puede incluir una página de propiedades de auditoría que permite al usuario ver y editar las entradas de control de acceso (ACE) en una lista de control de acceso del sistema (SACL) de objetos. Para obtener más información acerca de las SACL, consulte listas de Access Control (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Página de propiedades de auditoría
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277725"
---
# <a name="auditing-property-page"></a><span data-ttu-id="1348e-104">Página de propiedades de auditoría</span><span class="sxs-lookup"><span data-stu-id="1348e-104">Auditing Property Page</span></span>

<span data-ttu-id="1348e-105">El editor de control de acceso puede incluir una página de propiedades de **Auditoría** que permite al usuario ver y editar las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) en la lista de control de [*acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="1348e-105">The access control editor can include an **Auditing** property page that enables the user to view and edit the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in an object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1348e-106">Para obtener más información acerca de las SACL, consulte [listas de Access Control](access-control-lists.md) (ACL).</span><span class="sxs-lookup"><span data-stu-id="1348e-106">For more information about SACLs, see [Access Control Lists](access-control-lists.md) (ACLs).</span></span>

<span data-ttu-id="1348e-107">**Para ver la página de propiedades de auditoría**</span><span class="sxs-lookup"><span data-stu-id="1348e-107">**To view the Auditing property page**</span></span>

-   <span data-ttu-id="1348e-108">En la [Página de propiedades seguridad básica](basic-security-property-page.md), haga clic en **Opciones avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="1348e-108">On the [basic security property page](basic-security-property-page.md), click **Advanced**.</span></span> <span data-ttu-id="1348e-109">La página de propiedades **Auditoría** está en la [hoja de propiedades seguridad avanzada](advanced-security-property-sheet.md).</span><span class="sxs-lookup"><span data-stu-id="1348e-109">The **Auditing** property page is in the [advanced security property sheet](advanced-security-property-sheet.md).</span></span>

<span data-ttu-id="1348e-110">Para incluir la página de propiedades de **Auditoría** , establezca las marcas **si está \_ Avanzado** y **Si edita las \_ \_ auditorías** en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devuelta por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="1348e-110">To include the **Auditing** property page, set the **SI\_ADVANCED** and **SI\_EDIT\_AUDITS** flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
