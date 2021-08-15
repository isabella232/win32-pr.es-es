---
description: La hoja de propiedades de seguridad avanzada permite al usuario realizar operaciones de edición que no están disponibles en la página de propiedades de seguridad básica de un editor de control de acceso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Hoja de propiedades de seguridad avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808eaefaa481e828504eb55b3ecc3b70d487c03af82b296c3b8bc02da2b354d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914355"
---
# <a name="advanced-security-property-sheet"></a>Hoja de propiedades de seguridad avanzada

La hoja de propiedades de seguridad avanzada permite al usuario realizar operaciones de edición que no están disponibles en la página de propiedades de seguridad básica [de](basic-security-property-page.md) un editor de control de acceso. La hoja de propiedades puede incluir las siguientes páginas de propiedades:

-   Página [de propiedades](permissions-property-page.md) Permisos para la edición avanzada de la lista de [](object-specific-aces.md) [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) del objeto, como la edición de ACE específicas del objeto o el control de la [herencia ace.](ace-inheritance.md)
-   Página [de propiedades Auditoría](auditing-property-page.md) para ver y editar la lista de control de acceso [*del*](/windows/desktop/SecGloss/s-gly) sistema (SACL) del objeto.
-   Página [de](owner-property-page.md) propiedades Propietario para cambiar el propietario del objeto.

El usuario puede mostrar la hoja de propiedades de seguridad avanzada haciendo clic en el **botón** Avanzadas de la página de propiedades de seguridad básica. Para mostrar el **botón Avanzado,** establezca la marca SI ADVANCED en la estructura SI OBJECT INFO devuelta por la implementación \_ de [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

 

 
