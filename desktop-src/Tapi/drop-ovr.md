---
description: Al quitar o desconectar una sesión se finaliza la comunicación. La aplicación tiene la opción de enviar información de usuario-usuario en el momento de la desconexión, si el proveedor de servicios la admite.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Anular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821b9778ff59f0c515c7d7d00c1d3709cfdafdc36b6b0f113bceab312ff419b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945608"
---
# <a name="drop"></a>Anular

Al quitar o desconectar una sesión se finaliza la comunicación. La aplicación tiene la opción de enviar información de usuario-usuario en el momento de la desconexión, si el proveedor de servicios la admite.

Las razones habituales para quitar una sesión son que un usuario ha solicitado una desconexión o que se ha eliminado el otro extremo de la sesión. También se puede llamar a una operación de colocación cuando TAPI ofrece una sesión a la aplicación. Si el proveedor de servicios lo admite, el efecto es que la aplicación rechaza la llamada.

Al invocar una operación de colocación, las sesiones relacionadas a veces también pueden verse afectadas. Por ejemplo, quitar una llamada de conferencia puede quitar todos los participantes individuales. Los mensajes de cambio de estado se envían a la aplicación para todas las llamadas cuyo estado se ve afectado.

En varias configuraciones de puente o de línea de entidad cuando hay varias partes en la llamada, es posible que una operación de colocación no borre realmente la llamada. Por ejemplo, en una situación de puente, es posible que la llamada no se descarta porque el estado de otras estaciones de la llamada puede regir. En su lugar, la llamada puede cambiarse simplemente al estado inactivo mientras permanece conectada en otras estaciones.

Después de una operación de colocación, el identificador de sesión y la mayoría de los recursos asociados a la sesión seguirán siendo utilizables para la mayoría de las operaciones de consulta. Cuando una aplicación ya no requiere estos recursos, debe [finalizar la sesión](terminate-a-session-ovr.md) para evitar pérdidas de memoria.

**TAPI 2.x:** Vea [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).

**TAPI 3.x:** Vea [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
