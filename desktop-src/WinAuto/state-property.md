---
title: Propiedad State
description: La propiedad State describe el estado de un objeto en un momento dado. Todos los objetos admiten la propiedad State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070618"
---
# <a name="state-property"></a>Propiedad State

La **propiedad State** describe el estado de un objeto en un momento dado. Todos los objetos admiten la **propiedad** State.

La **propiedad State** se recupera mediante una llamada a [**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility proporciona constantes de estado de objeto , [definidas](object-state-constants.md)en oleacc.h, que se combinan para identificar el estado de un objeto. Se recomienda que los desarrolladores de servidores usen estos valores de estado predefinidos. Si se devuelven valores de estado predefinidos, los clientes usan [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar una cadena localizada que describe el estado.

Los gráficos que se animan en ocasiones deben tener la propiedad **State** establecida en [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md) y la [**propiedad Role**](role-property.md) establecida en ROLE SYSTEM [**\_ \_ GRAPHIC**](object-roles.md).

 

 




