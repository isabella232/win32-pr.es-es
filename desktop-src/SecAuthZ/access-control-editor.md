---
description: Conjunto de hojas de propiedades y páginas de propiedades que permiten al usuario ver y modificar los componentes de un descriptor de seguridad de objetos.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Access Control Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073763"
---
# <a name="access-control-editor"></a>Access Control Editor

El editor de control de acceso es un conjunto de hojas de propiedades y páginas de propiedades que permiten al usuario ver y modificar los componentes del descriptor de seguridad [*de un objeto*](/windows/desktop/SecGloss/s-gly). El editor consta de dos partes principales:

-   Página [de propiedades](basic-security-property-page.md) de seguridad básica que proporciona una interfaz sencilla para editar las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) en la lista de control de acceso discrecional (DACL) [*de*](/windows/desktop/SecGloss/d-gly) un objeto. Esta página puede incluir un botón Opciones **avanzadas** opcional que muestra la hoja de propiedades de seguridad avanzada.
-   Hoja [de](advanced-security-property-sheet.md) propiedades de seguridad avanzada con páginas de propiedades que permiten al usuario editar la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL) del objeto, cambiar el propietario del objeto o realizar una edición avanzada de la DACL del objeto.

La [**función CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crea la página de propiedades de seguridad básica. A continuación, puede usar la [**función PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) o el mensaje [**\_ ADDPAGE de PSM**](../controls/psm-addpage.md) para agregar esta página a una hoja de propiedades.

Como alternativa, puede usar la función [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) para mostrar una hoja de propiedades que contiene la página de propiedades de seguridad básica.

Para [**CreateSecurityPage y**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), el autor de la llamada debe pasar un puntero a una implementación de la [**interfaz ISecurityInformation.**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) El editor de control de acceso llama a los métodos de esta interfaz para recuperar información de control de acceso sobre el objeto que se está editando y para devolver la entrada del usuario a la aplicación. Los **métodos ISecurityInformation** tienen los siguientes fines:

-   Para inicializar las páginas de propiedades.

    La implementación del método [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) pasa una [**estructura SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) al editor. Esta estructura especifica las páginas de propiedades que desea que muestre el editor y otra información que determina las opciones de edición disponibles para el usuario.

-   Para proporcionar información de seguridad sobre el objeto que se está editando.

    La [**implementación de GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) pasa el descriptor de seguridad [*inicial del objeto*](/windows/desktop/SecGloss/s-gly) al editor. Los [**métodos GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) [**y MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) proporcionan información sobre los derechos de acceso del objeto. El [**método GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) proporciona información sobre cómo los objetos secundarios pueden heredar las ACE del objeto.

-   Para volver a pasar la entrada del usuario a la aplicación.

    Cuando el usuario hace clic en **Aceptar** o **Aplicar,** el editor llama al método [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) para devolver un descriptor de seguridad que contiene los cambios del usuario.

 

 
