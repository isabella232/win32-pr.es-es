---
description: El editor de control de acceso puede incluir una página de propiedades Propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre un propietario de objetos, vea Propietario de un nuevo objeto y Tomar propiedad del objeto en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propiedades propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b67b3707017aa8073cfdf4f5ca64340eda74a640bc604a0bd382b7cf2ebe122e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907665"
---
# <a name="owner-property-page"></a>Página de propiedades propietario

El editor de control de acceso puede incluir una página de propiedades Propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de un objeto, vea [Propietario de un nuevo](owner-of-a-new-object.md) objeto y Tomar propiedad del objeto en [C++.](taking-object-ownership-in-c--.md)

La **página de** propiedades Propietario se encuentra en la [hoja](advanced-security-property-sheet.md) de propiedades de seguridad avanzada que se muestra cuando el usuario hace clic en el botón Avanzadas de la [página de propiedades de seguridad básica](basic-security-property-page.md).  Para incluir la página de propiedades **Propietario,** establezca las marcas SI ADVANCED y SI EDIT OWNER en la estructura SI OBJECT INFO devuelta por la implementación \_ de \_ \_ [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

 

 
