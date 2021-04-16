---
description: El estado de la sesión o la llamada indica el estado actual de una sesión, como &\# 0034; oferta&\# 0034; o &\# 0034; conectado. &\# 0034; El control adecuado de la información de estado es fundamental para el correcto funcionamiento de la mayoría de las aplicaciones TAPI.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: Estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688619"
---
# <a name="state"></a>Estado

El estado de la sesión o la llamada indica el estado actual de una sesión, como "oferta" o "conectado". El control adecuado de la información de estado es fundamental para el correcto funcionamiento de la mayoría de las aplicaciones TAPI. Por ejemplo, la operación de respuesta solo se puede realizar en una sesión ofrecida, pero se producirá un error en una transferencia si la sesión está en ese estado.

El estado de una sesión cambia como resultado de los eventos. Los eventos pueden ser solicitados o no solicitados. Los *eventos solicitados* están causados por la aplicación que controla la sesión, por ejemplo, cuando invoca una operación de sesión de TAPI. Los *eventos no solicitados* están causados por el conmutador, la red telefónica, el usuario que presiona los botones del teléfono local o las acciones de la parte remota.

Cada vez que un proveedor de servicios detecta un cambio de estado de sesión, informa del cambio en TAPI y TAPI emite una notificación de eventos a todas las aplicaciones de propietario y supervisión. La aplicación debe reaccionar a estas notificaciones adecuadamente. Consulte la notificación de eventos en [inicialización de TAPI](tapi-initialization.md) para obtener información sobre cómo controlar los eventos que se notifican a una aplicación.

Una aplicación siempre debe procesar las notificaciones de eventos de estado. Es posible que las transiciones de estado válidas para una configuración física no sean válidas para otra. Por ejemplo, considere una línea que termina físicamente tanto en el equipo como en un conjunto de teléfonos independiente, creando una configuración de línea de entidad entre el equipo y el conjunto de teléfonos. Es posible que una aplicación que se ejecuta en el equipo no conozca las actividades de juego de teléfono. Es decir, la línea puede estar en uso sin que el proveedor de servicios lo sepa. Una aplicación que intente realizar una llamada saliente tendrá éxito en la asignación de una apariencia de llamada desde TAPI, pero esto provocará el uso compartido de la llamada activa en la línea. Enviar ciegamente una cadena de marcado DTMF sin comprobar primero si un tono de marcado no puede dar lugar a un comportamiento previsto (o educado).

Una aplicación no debe suponer una progresión rígida de un estado a otro. Los eventos de estado llegan y se reenvían de forma asincrónica y es posible que las notificaciones no se reciban en un orden predecible. Por lo tanto, se deben ver las notificaciones de estado de llamada para indicar a la aplicación el nuevo estado de la llamada en lugar de notificar las transiciones entre dos Estados.

Todos los proveedores de servicios de telefonía deben proporcionar esta información.

* * TAPI 2. x: * *[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**línea \_ CALLSTATE**](./line-callstate.md) Message, [LINECALLSTATE \_ constantes](./linecallstate--constants.md)

**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL \_ CALLID** miembro de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) Notification, enumerador de [**\_ Estado de llamada**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state)

 

 
