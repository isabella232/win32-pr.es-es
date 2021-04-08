---
description: Al quitar o desconectar una sesión se termina la comunicación. La aplicación tiene la opción de enviar información de usuario de usuario en el momento de la desconexión, si el proveedor de servicios lo admite.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Anular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001030"
---
# <a name="drop"></a>Anular

Al quitar o desconectar una sesión se termina la comunicación. La aplicación tiene la opción de enviar información de usuario de usuario en el momento de la desconexión, si el proveedor de servicios lo admite.

Las razones habituales para quitar una sesión es que un usuario ha solicitado una desconexión o se ha quitado el otro extremo de la sesión. También se puede llamar a una operación Drop cuando TAPI ofrece una sesión a la aplicación. Si el proveedor de servicios lo admite, el efecto es que la aplicación rechaza la llamada.

Al invocar una operación de colocar, las sesiones relacionadas a veces también pueden verse afectadas. Por ejemplo, quitar una llamada de conferencia puede quitar todos los participantes individuales. Los mensajes de cambio de estado se envían a la aplicación para todas las llamadas cuyo estado se ve afectado.

En varias configuraciones puente o de línea de entidad cuando hay varias entidades en la llamada, es posible que una operación de colocar no borre realmente la llamada. Por ejemplo, en una situación de puente, es posible que la llamada no se quite porque el estado de otras estaciones de la llamada puede regir. En su lugar, la llamada simplemente se puede cambiar al estado inactivo mientras está conectado en otras estaciones.

Después de una operación de colocar, el identificador de sesión y la mayoría de los recursos asociados a la sesión seguirán siendo utilizables para la mayoría de las operaciones de consulta. Cuando una aplicación ya no requiere estos recursos, debe [finalizar la sesión](terminate-a-session-ovr.md) para evitar pérdidas de memoria.

**TAPI 2. x:** Vea [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3. x:** Vea [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
