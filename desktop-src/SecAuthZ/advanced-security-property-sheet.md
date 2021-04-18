---
description: La hoja de propiedades seguridad avanzada permite al usuario realizar operaciones de edición que no están disponibles en la página de propiedades seguridad básica de un editor de control de acceso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Seguridad avanzada (hoja de propiedades)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649293"
---
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="5ec9d-103">Seguridad avanzada (hoja de propiedades)</span><span class="sxs-lookup"><span data-stu-id="5ec9d-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="5ec9d-104">La hoja de propiedades seguridad avanzada permite al usuario realizar operaciones de edición que no están disponibles en la [Página de propiedades seguridad básica](basic-security-property-page.md) de un editor de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="5ec9d-105">La hoja de propiedades puede incluir las siguientes páginas de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5ec9d-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="5ec9d-106">Una página de propiedades de [permisos](permissions-property-page.md) para la edición avanzada de [*la lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto, como editar [ACE específicas del objeto](object-specific-aces.md) o controlar la herencia de [ACE](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="5ec9d-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="5ec9d-107">Una página de propiedades de [Auditoría](auditing-property-page.md) para ver y editar la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) del objeto.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="5ec9d-108">Una página de propiedades de [propietario](owner-property-page.md) para cambiar el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="5ec9d-109">Para mostrar la hoja de propiedades seguridad avanzada, el usuario puede hacer clic en el botón **avanzadas** de la página de propiedades seguridad básica.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="5ec9d-110">Para mostrar el botón **Opciones avanzadas** , establezca la \_ marca si es avanzado en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devuelta por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="5ec9d-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
