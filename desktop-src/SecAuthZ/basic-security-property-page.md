---
description: Página inicial de la hoja de propiedades que muestra la función EditSecurity. También puede usar la función CreateSecurityPage para crear una página de propiedades de seguridad básica para insertarla en su propia hoja de propiedades.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Página de propiedades seguridad básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f839058d8cd9c9a4c9d1a20dab96620d1e731d23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155268"
---
# <a name="basic-security-property-page"></a>Página de propiedades seguridad básica

La página de propiedades seguridad básica es la página de inicio de la hoja de propiedades que muestra la función [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) . También puede usar la función [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) para crear una página de propiedades de seguridad básica para insertarla en su propia hoja de propiedades.

La página de propiedades muestra una lista de los nombres de [confianza](trustees.md) nombrados en las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto. La página también contiene una lista de los derechos de acceso que admite el objeto. Cuando el usuario selecciona un nombre de la lista de usuarios de confianza, las casillas situadas junto a cada derecho de acceso indican los derechos que se permiten o deniegan para ese administrador de confianza. El usuario puede activar o desactivar las casillas para modificar los derechos de acceso del administrador de confianza. El usuario también puede Agregar o quitar usuarios de confianza de la lista.

La página de propiedades de seguridad básica no puede mostrar ACE complejas, como las [ACE específicas del objeto o la](object-specific-aces.md)información de herencia de ACE. Para permitir al usuario ver o editar esta información, puede incluir un botón **avanzado** en la página seguridad básica. El usuario puede hacer clic en el botón **avanzadas** para mostrar una [hoja de propiedades de seguridad avanzada](advanced-security-property-sheet.md). Esta hoja de propiedades tiene páginas de propiedades que permiten al usuario editar la [*lista de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL) del objeto, cambiar el propietario del objeto o realizar una edición avanzada de la DACL del objeto. Para mostrar el botón **Opciones avanzadas** , establezca la \_ marca si es avanzado en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devuelta por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

Puede usar el miembro **pszPageTitle** de la estructura [**de \_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) para especificar el título de la página de propiedades seguridad básica. El título predeterminado es **seguridad**.

 

 
