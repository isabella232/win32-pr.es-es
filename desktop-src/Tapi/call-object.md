---
description: El objeto Call representa una conexión de direcciones entre la dirección local y una o varias direcciones.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Objeto Call
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2b37ff30e1e47cc3daf5e3152d5051161535f0f4e6cdcb9d27d5537619e967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870025"
---
# <a name="call-object"></a>Objeto Call

El objeto Call representa la conexión de una dirección entre la dirección local y una o varias direcciones. Todo el control de llamada se realiza a través del objeto Call. [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) son las interfaces que se usan con más frecuencia en el objeto de llamada. Estas interfaces implementan una variedad de operaciones y consultas, como la adquisición de punteros de interfaz para secuencias multimedia o la obtención del identificador de autor de la llamada. Consulte las secciones de información general principales sobre operaciones [de](session-operations-ovr.md) sesión e información [de sesión](session-information-ovr.md) para obtener revisiones de las que admite TAPI.

Un proveedor de servicios multimedia puede implementar [interfaces](provider-specific-interfaces.md)específicas del proveedor , que TAPI agrega en un objeto de llamada. Para obtener información detallada sobre lo que ha implementado un proveedor, consulte la documentación del proveedor de servicios.

Los [ejemplos de código Realizar una llamada](make-a-call.md) y [Recibir](receive-a-call.md) una llamada muestran algunas ilustraciones del uso de un objeto Call.

Vea [Call Object Interfaces (Interfaces de objeto de](call-object-interfaces.md) llamada) para obtener una lista de todas las interfaces asociadas al objeto Call.

 

 



