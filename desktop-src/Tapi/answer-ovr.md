---
description: La operación de respuesta es una respuesta típica de las aplicaciones a una sesión de comunicaciones ofrecida. Si se realiza correctamente, esta operación hace que una sesión pase al estado conectado.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545654"
---
# <a name="answer"></a>Respuesta

La operación de respuesta es la respuesta típica de una aplicación a una sesión de comunicaciones ofrecida. Si se realiza correctamente, esta operación hace que una sesión pase al estado conectado.

En algunos entornos de telefonía (como RDSI), en los que la alerta de usuario es independiente de la oferta de llamada, la aplicación tiene la opción de [Aceptar](accept-ovr.md) una llamada antes de responder o rechazar ([quitar](drop-ovr.md)) o [redirigir](redirect-ovr.md) la llamada de *oferta* .

Si se realiza una operación de respuesta para una nueva sesión cuando una sesión ya está activa, el efecto que tiene en la sesión activa existente depende de las capacidades del proveedor de servicios. La primera llamada puede no verse afectada, se puede quitar automáticamente o puede colocarse automáticamente en espera. TAPI enviará las notificaciones de eventos adecuadas relativas a ambas llamadas.

En una situación de puente, si una llamada está conectada pero en el estado activo, se puede combinar con la operación de respuesta.

La aplicación tiene la opción de enviar información de usuario al usuario en el momento de la respuesta, si el proveedor de servicios lo admite.

**TAPI 2. x:** Vea [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).

**TAPI 3. x:** Vea [**ITBasicCallControl:: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).

 

 
