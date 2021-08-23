---
title: Propiedad Role
description: La propiedad Role describe el elemento de la interfaz de usuario de un objeto. Todos los objetos admiten la propiedad Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2881b301537e9a25dabb260b84bc889cef4e4a6f9f6a5a2c8fab540d78daf8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133728"
---
# <a name="role-property"></a>Propiedad Role

La **propiedad Role** describe el elemento de la interfaz de usuario de un objeto. Todos los objetos admiten la **propiedad Role.**

En muchos casos, el rol del objeto es obvio. Por ejemplo, las ventanas tienen el [**rol ROLE \_ SYSTEM \_ WINDOW**](object-roles.md) y los botones de inserción tienen el [**rol ROLE SYSTEM \_ \_ PUSHBUTTON.**](object-roles.md)

La **propiedad Role** se recupera llamando a [**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identificar el rol de un objeto

Microsoft Active Accessibility proporciona constantes de rol , [definidas](object-roles.md)en oleacc.h, que identifican roles de objeto comunes. Se recomienda que los desarrolladores de servidores usen estos valores de rol predefinidos. Si se devuelve una constante de rol predefinida, los clientes usan la [**función GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar una cadena localizada que describe el rol.

Para los controles de animación, como el control de animación que se muestra al copiar archivos, use [**ROLE \_ SYSTEM \_ ANIMATION**](object-roles.md). Los gráficos que se animan en ocasiones se describen como [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md) con la [**propiedad State**](state-property.md) establecida en STATE SYSTEM [**\_ \_ ANIMATED**](object-state-constants.md).

Tenga en cuenta que algunos roles no son fáciles de describir. Por ejemplo, la vista de iconos grandes de una carpeta permite la organización arbitraria de iconos, por lo que su rol se podría describir como [**ROLE \_ SYSTEM \_ GROUPING**](object-roles.md). O bien, un control que proporciona elementos en filas y columnas fijas podría tener el [**rol ROLE \_ SYSTEM \_ TABLE.**](object-roles.md) Puesto que un rol se usa para comunicar el modelo de uso a un usuario final, es importante usar el rol adecuado. Por ejemplo, si el control actúa como un botón, use [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md).

 

 




