---
description: Página inicial de la hoja de propiedades mostrada por la función EditSecurity. También puede usar la función CreateSecurityPage para crear una página de propiedades de seguridad básica para insertarla en su propia hoja de propiedades.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Página de propiedades Seguridad básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783712"
---
# <a name="basic-security-property-page"></a>Página de propiedades Seguridad básica

La página de propiedades de seguridad básica es la página de inicio de la hoja de propiedades mostrada por la [**función EditSecurity.**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) También puede usar la función [**CreateSecurityPage para**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crear una página de propiedades de seguridad básica para insertarla en su propia hoja de propiedades.

La página de propiedades muestra una lista de los administradores de confianza [denominados](trustees.md) en las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) de la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) del objeto. La página también contiene una lista de los derechos de acceso admitidos por el objeto . Cuando el usuario selecciona un nombre de la lista de administradores de confianza, las casillas situadas junto a cada derecho de acceso indican los derechos que se permiten o se deniegan para ese administrador de confianza. A continuación, el usuario puede activar o borrar las casillas para modificar los derechos de acceso del administrador de confianza. El usuario también puede agregar o quitar administradores de confianza de la lista.

La página de propiedades de seguridad básica no puede mostrar AEE complejas, como las [ACE](object-specific-aces.md)específicas del objeto o la información de herencia de ACE. Para permitir que el usuario vea o edite dicha información, puede incluir un **botón** Avanzado en la página de seguridad básica. El usuario puede hacer clic en el **botón Avanzadas** para mostrar una hoja de propiedades de [seguridad avanzada](advanced-security-property-sheet.md). Esta hoja de propiedades tiene páginas de propiedades que permiten al usuario editar la lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL) del objeto, cambiar el propietario del objeto o realizar una edición avanzada de la DACL del objeto. Para mostrar el **botón Avanzado,** establezca la marca SI ADVANCED en la estructura SI OBJECT INFO devuelta por la implementación \_ de [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

Puede usar el miembro **pszPageTitle** de la estructura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) para especificar el título de la página de propiedades de seguridad básica. El título predeterminado es **Seguridad.**

 

 
