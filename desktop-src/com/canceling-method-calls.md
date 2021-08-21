---
title: Cancelación de llamadas a métodos
description: Con la introducción de aplicaciones distribuidas y basadas en web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ea089f257527dfd31d7120170c8749a2d1b4d60ba006843c7ff5d43403b352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311089"
---
# <a name="canceling-method-calls"></a>Cancelación de llamadas a métodos

Con la introducción de aplicaciones distribuidas y basadas en web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse. La latencia de la conexión de red puede ser alta, la máquina del servidor puede atender a muchos clientes o el componente de servidor puede estar pasando una gran cantidad de datos, como un archivo multimedia. Los usuarios deben poder cancelar una solicitud que está tardando demasiado tiempo y la aplicación debe ser capaz de controlar las solicitudes de cancelación y continuar con su otro trabajo. En COM, puede usar la interfaz [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar una llamada pendiente que se origina desde un apartamento de un solo subproceso.

Cuando se serializa una llamada, el proxy crea un objeto cancel, que implementa la [**interfaz ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) El objeto cancel está asociado a la llamada y al subproceso en el que la llamada está pendiente.

Para cancelar la llamada pendiente, el cliente pasa una solicitud de cancelación a través del objeto cancel, que controla los detalles de notificar al objeto de servidor que la llamada se ha cancelado. Si no se ha devuelto el método al que se llama, el objeto de servidor, al detectar la solicitud de cancelación, limpia los recursos del programa que ha asignado y notifica a su cliente, devolviendo un valor **HRESULT** adecuado, que canceló la ejecución de la llamada. Si el método al que se llama ya ha devuelto, el objeto cancel notifica al cliente. En cualquier caso, el subproceso de cliente se desbloquea y puede continuar el procesamiento.

La forma en que el objeto de servidor responde a una solicitud de cancelación está a discreción del implementador del servidor, pero el subproceso de llamada en el cliente siempre se desbloqueará y omitirá los resultados que el servidor intente pasarle. Los objetos Cancel proporcionan un medio para solicitar que se cancele un método que se está ejecutando actualmente, pero no hay ninguna garantía de que el objeto de servidor deje de procesar la llamada. Por ejemplo, es posible que la llamada ya haya devuelto o que el objeto de servidor no admita objetos de cancelación.

COM proporciona automáticamente una implementación estándar de objetos de cancelación para objetos de cliente e interfaces que usan la serialización estándar. En el caso de los objetos e interfaces que usan la serialización personalizada, deberá implementar su propio objeto cancel.

En este momento, los objetos cancel controlan solo las llamadas sincrónicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cancelación de una llamada asincrónica](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 