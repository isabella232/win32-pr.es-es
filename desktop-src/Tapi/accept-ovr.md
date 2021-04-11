---
description: En algunos entornos, no se avisa automáticamente a un usuario de una llamada de oferta, como por ejemplo, por timbre o por un mensaje en la pantalla del equipo.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Aceptar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275314"
---
# <a name="accept"></a>Aceptar

En algunos entornos, no se avisa automáticamente a un usuario de una llamada de oferta, como por ejemplo, por timbre o por un mensaje en la pantalla del equipo. La operación de aceptación inicia el proceso de alertas (que normalmente suenan) y la operación de [respuesta](answer-ovr.md) tiene lugar después. Es posible que la aplicación [Quite](drop-ovr.md) la sesión, la [redirija](redirect-ovr.md) o la acepte.

Si el proveedor de servicios actual lo admite, la aplicación tiene la opción de enviar información de usuario al usuario en el momento de la aceptación. No hay ninguna garantía de que la red entregue esta información a la entidad que realiza la llamada.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).

 

 
