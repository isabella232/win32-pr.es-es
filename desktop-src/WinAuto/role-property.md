---
title: Role (propiedad)
description: La propiedad role describe el elemento de la interfaz de usuario de un objeto. Todos los objetos admiten la propiedad role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704588"
---
# <a name="role-property"></a>Role (propiedad)

La propiedad **role** describe el elemento de la interfaz de usuario de un objeto. Todos los objetos admiten la propiedad **role** .

En muchos casos, el rol del objeto es obvio. Por ejemplo, las ventanas tienen el rol de [**\_ \_ ventana del sistema de rol**](object-roles.md) y los botones de la función de pulsador del [**\_ sistema \_ de rol**](object-roles.md) .

La propiedad **role** se recupera llamando a [**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identificar el rol de un objeto

Microsoft Active Accessibility proporciona [constantes de rol](object-roles.md), definidas en oleacc. h, que identifican roles de objeto comunes. Se recomienda que los desarrolladores de servidores utilicen estos valores de roles predefinidos. Si se devuelve una constante de rol predefinida, los clientes utilizan la función [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar una cadena localizada que describe el rol.

En el caso de los controles de animación, como el control de animación que se muestra al copiar archivos, use la [**\_ \_ animación del sistema de roles**](object-roles.md). Los gráficos que se animan ocasionalmente se describen como un [**\_ \_ gráfico de sistema de roles**](object-roles.md) con la propiedad [**State**](state-property.md) establecida en [**Estado de \_ sistema \_ animado**](object-state-constants.md).

Tenga en cuenta que algunos roles no son fáciles de describir. Por ejemplo, la vista de iconos grandes de una carpeta permite la organización arbitraria de iconos, por lo que su rol podría describirse como [**\_ \_ agrupación del sistema de roles**](object-roles.md). O bien, un control que proporciona elementos en filas y columnas fijas podría tener el rol de [**\_ \_ tabla del sistema de rol**](object-roles.md) . Puesto que un rol se usa para comunicar el modelo de uso a un usuario final, es importante usar el rol adecuado. Por ejemplo, si el control actúa como un botón, use [**\_ \_ PUSHBUTTON del sistema de roles**](object-roles.md).

 

 




