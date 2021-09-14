---
description: El editor de control de acceso puede incluir una página de propiedades Propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de un objeto, vea Propietario de un nuevo objeto y Tomar posesión de objetos en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propiedades propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265471"
---
# <a name="owner-property-page"></a>Página de propiedades propietario

El editor de control de acceso puede incluir una página de propiedades Propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de un objeto, vea [Propietario de un nuevo](owner-of-a-new-object.md) objeto y Tomar [posesión del objeto en C++.](taking-object-ownership-in-c--.md)

La **página de** propiedades Propietario se encuentra en la [hoja](advanced-security-property-sheet.md) de propiedades de seguridad avanzada que se muestra cuando el usuario hace clic en el botón Avanzadas de la [página de propiedades de seguridad básica](basic-security-property-page.md).  Para incluir la **página de** propiedades Propietario, establezca las marcas SI ADVANCED y SI EDIT OWNER en la estructura SI OBJECT INFO devuelta por la implementación \_ de \_ \_ [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)

 

 
