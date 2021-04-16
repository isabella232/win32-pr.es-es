---
description: El objeto Call representa una conexión de direcciones entre la dirección local y una o varias direcciones.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Call (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678571"
---
# <a name="call-object"></a>Call (objeto)

El objeto Call representa la conexión de una dirección entre la dirección local y una o varias direcciones. Todo el control de llamada se realiza a través del objeto Call. [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) y [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) son las interfaces que se usan con más frecuencia en el objeto Call. Estas interfaces implementan una variedad de operaciones y consultas, como la adquisición de punteros de interfaz para flujos multimedia o la obtención del identificador del llamador. Consulte las secciones de información general principales sobre [operaciones de sesión](session-operations-ovr.md) e [información de sesión](session-information-ovr.md) para ver las revisiones de los compatibles con TAPI.

Un proveedor de servicios multimedia puede implementar [interfaces específicas del proveedor](provider-specific-interfaces.md), que se agregan a un objeto de llamada por TAPI. Para obtener información detallada sobre lo que un proveedor ha implementado, consulte la documentación del proveedor de servicios.

En los ejemplos de [creación de una llamada](make-a-call.md) y [recepción de un](receive-a-call.md) código de llamada se muestran algunas ilustraciones del uso de un objeto de llamada.

Vea [llamar a interfaces de objeto](call-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto de llamada.

 

 



