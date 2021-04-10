---
description: El editor de control de acceso puede incluir una página de propiedades de propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de los objetos, vea propietario de un nuevo objeto y tomar posesión de objetos en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propiedades propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156776"
---
# <a name="owner-property-page"></a>Página de propiedades propietario

El editor de control de acceso puede incluir una página de propiedades de propietario que permite al usuario cambiar el propietario de un objeto. Para obtener más información sobre el propietario de un objeto, vea [propietario de un nuevo objeto](owner-of-a-new-object.md) y [tomar posesión de objetos en C++](taking-object-ownership-in-c--.md).

La página de propiedades **propietario** está en la [hoja de propiedades seguridad avanzada](advanced-security-property-sheet.md) que se muestra cuando el usuario hace clic en el botón **avanzadas** de la [Página de propiedades seguridad básica](basic-security-property-page.md). Para incluir la página de propiedades del **propietario** , establezca las \_ marcas si y \_ Editar \_ propietario en la estructura de [**\_ \_ información del objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devueltos por la implementación de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
