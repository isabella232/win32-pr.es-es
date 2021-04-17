---
description: Conjunto de hojas de propiedades y páginas de propiedades que permiten al usuario ver y modificar los componentes de un descriptor de seguridad de objetos.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Editor de Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652758"
---
# <a name="access-control-editor"></a>Editor de Access Control

El editor de control de acceso es un conjunto de hojas de propiedades y páginas de propiedades que permiten al usuario ver y modificar los componentes del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto. El editor está formado por dos partes principales:

-   [Página de propiedades de seguridad básica](basic-security-property-page.md) que proporciona una interfaz simple para editar las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) en la lista de [*control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto. Esta página puede incluir un botón **avanzado** opcional que muestra la hoja de propiedades de seguridad avanzada.
-   Una [hoja de propiedades de seguridad avanzada](advanced-security-property-sheet.md) con páginas de propiedades que permiten al usuario editar la [*lista de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL) del objeto, cambiar el propietario del objeto o realizar una edición avanzada de la DACL del objeto.

La función [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crea la página de propiedades de seguridad básica. Después, puede usar la función [**hoja**](/windows/win32/api/prsht/nf-prsht-propertysheeta) o el mensaje de [**PSM de PSM \_**](../controls/psm-addpage.md) para agregar esta página a una hoja de propiedades.

Como alternativa, puede usar la función [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) para mostrar una hoja de propiedades que contenga la página de propiedades de seguridad básica.

Para [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) y [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), el llamador debe pasar un puntero a una implementación de la interfaz [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) . El editor de control de acceso llama a los métodos de esta interfaz para recuperar información de control de acceso sobre el objeto que se está editando y para devolver la entrada del usuario a la aplicación. Los métodos de **ISecurityInformation** tienen los siguientes fines:

-   Para inicializar las páginas de propiedades.

    La implementación del método [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) pasa una estructura [**de \_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) al editor. Esta estructura especifica las páginas de propiedades que desea que muestre el editor y otra información que determina las opciones de edición disponibles para el usuario.

-   Para proporcionar información de seguridad sobre el objeto que se está editando.

    La implementación de [**GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) pasa el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) inicial del objeto al editor. Los métodos [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) y [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) proporcionan información sobre los derechos de acceso del objeto. El método [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) proporciona información sobre cómo los objetos secundarios pueden heredar las entradas ACE del objeto.

-   Para devolver la entrada del usuario a la aplicación.

    Cuando el usuario hace clic en **Aceptar** o **aplicar**, el editor llama al método [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) para devolver un descriptor de seguridad que contiene los cambios del usuario.

 

 
