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
# <a name="advanced-security-property-sheet"></a>Seguridad avanzada (hoja de propiedades)

La hoja de propiedades seguridad avanzada permite al usuario realizar operaciones de edición que no están disponibles en la [Página de propiedades seguridad básica](basic-security-property-page.md) de un editor de control de acceso. La hoja de propiedades puede incluir las siguientes páginas de propiedades:

-   Una página de propiedades de [permisos](permissions-property-page.md) para la edición avanzada de [*la lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto, como editar [ACE específicas del objeto](object-specific-aces.md) o controlar la herencia de [ACE](ace-inheritance.md).
-   Una página de propiedades de [Auditoría](auditing-property-page.md) para ver y editar la [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) del objeto.
-   Una página de propiedades de [propietario](owner-property-page.md) para cambiar el propietario del objeto.

Para mostrar la hoja de propiedades seguridad avanzada, el usuario puede hacer clic en el botón **avanzadas** de la página de propiedades seguridad básica. Para mostrar el botón **Opciones avanzadas** , establezca la \_ marca si es avanzado en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devuelta por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
