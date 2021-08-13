---
title: Propiedad State
description: La propiedad State describe el estado de un objeto en un momento dado. Todos los objetos admiten la propiedad State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e174e938dd6252852ded6de957a54f6f94264aa811bd5bb76094af7bbba61f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564423"
---
# <a name="state-property"></a>Propiedad State

La **propiedad State** describe el estado de un objeto en un momento dado. Todos los objetos admiten la **propiedad State.**

La **propiedad State** se recupera mediante una llamada a [**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility proporciona constantes de estado de objeto , [definidas](object-state-constants.md)en oleacc.h, que se combinan para identificar el estado de un objeto. Se recomienda que los desarrolladores de servidores usen estos valores de estado predefinidos. Si se devuelven valores de estado predefinidos, los clientes usan [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar una cadena localizada que describe el estado.

Los gráficos que se animan ocasionalmente deben tener la propiedad **State** establecida en [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md) y la [**propiedad Role**](role-property.md) establecida en ROLE SYSTEM [**\_ \_ GRAPHIC**](object-roles.md).

 

 




