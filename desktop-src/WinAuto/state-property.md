---
title: Propiedad State
description: La propiedad State describe el estado de un objeto en un momento dado. Todos los objetos admiten la propiedad State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903832"
---
# <a name="state-property"></a>Propiedad State

La propiedad **State** describe el estado de un objeto en un momento dado. Todos los objetos admiten la propiedad **State** .

La propiedad **State** se recupera llamando a [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility proporciona [constantes de estado de objeto](object-state-constants.md), definidas en oleacc. h, que se combinan para identificar el estado de un objeto. Se recomienda que los desarrolladores de servidor utilicen estos valores de estado predefinidos. Si se devuelven valores de estado predefinidos, los clientes utilizan [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar una cadena localizada que describe el estado.

Los gráficos que se animan ocasionalmente deberían tener la propiedad **State** establecida en [**estado \_ \_ animado del sistema**](object-state-constants.md) y la propiedad [**rol**](role-property.md) establecida en [**gráfico de \_ sistema \_ de roles**](object-roles.md).

 

 




