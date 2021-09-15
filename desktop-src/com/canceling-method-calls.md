---
title: Cancelación de llamadas a métodos
description: Con la introducción de aplicaciones distribuidas y basadas en web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466981"
---
# <a name="canceling-method-calls"></a>Cancelación de llamadas a métodos

Con la introducción de aplicaciones distribuidas y basadas en web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse. La latencia de la conexión de red puede ser alta, la máquina del servidor puede atender a muchos clientes o el componente de servidor puede estar pasando una gran cantidad de datos, como un archivo multimedia. Los usuarios deben poder cancelar una solicitud que está tardando demasiado tiempo y la aplicación debe ser capaz de controlar las solicitudes de cancelación y continuar con su otro trabajo. En COM, puede usar la interfaz [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar una llamada pendiente que se origina en un apartamento de un solo subproceso.

Cuando se serializa una llamada, el proxy crea un objeto cancel, que implementa la [**interfaz ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) El objeto cancel está asociado a la llamada y al subproceso en el que la llamada está pendiente.

Para cancelar la llamada pendiente, el cliente pasa una solicitud de cancelación a través del objeto de cancelación, que controla los detalles de notificar al objeto de servidor que la llamada se ha cancelado. Si el método al que se llama no ha devuelto, el objeto de servidor, al detectar la solicitud de cancelación, limpia los recursos del programa que ha asignado y notifica a su cliente, devolviendo un valor **HRESULT** adecuado, que canceló la ejecución de la llamada. Si el método al que se llama ya ha devuelto, el objeto cancel notifica al cliente. En cualquier caso, el subproceso de cliente se desbloquea y puede continuar el procesamiento.

La forma en que el objeto de servidor responde a una solicitud de cancelación está a discreción del implementador del servidor, pero el subproceso que realiza la llamada en el cliente siempre se desbloqueará y omitirá los resultados que el servidor intente pasar a él. Los objetos cancel proporcionan un medio para solicitar que se cancele un método actualmente en ejecución, pero no hay ninguna garantía de que el objeto de servidor deje de procesar la llamada. Por ejemplo, es posible que la llamada ya se haya devuelto o que el objeto de servidor no admita objetos de cancelación.

COM proporciona automáticamente una implementación estándar de objetos de cancelación para objetos de cliente e interfaces que usan serialización estándar. Para los objetos e interfaces que usan la serialización personalizada, deberá implementar su propio objeto de cancelación.

En este momento, los objetos de cancelación solo controlan llamadas sincrónicas.

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

 

 