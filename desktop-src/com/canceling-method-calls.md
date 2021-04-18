---
title: Cancelar llamadas a métodos
description: Con la introducción de aplicaciones distribuidas y basadas en Web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714469"
---
# <a name="canceling-method-calls"></a>Cancelar llamadas a métodos

Con la introducción de aplicaciones distribuidas y basadas en Web, algunas llamadas a métodos pueden tardar un tiempo inaceptablemente largo en devolverse. La latencia de la conexión de red puede ser alta, el equipo del servidor puede estar atendiendo a muchos clientes, o el componente del servidor puede estar pasando una gran cantidad de datos, como un archivo multimedia. Los usuarios deben poder cancelar una solicitud que esté tardando mucho tiempo y la aplicación debe ser capaz de controlar las solicitudes de cancelación y continuar con su otro trabajo. En COM, puede usar la interfaz [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar una llamada pendiente que se origina a partir de un contenedor uniproceso.

Cuando se calculan las referencias de una llamada, el proxy crea un objeto CANCEL, que implementa la interfaz [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . El objeto CANCEL está asociado a la llamada y al subproceso en el que está pendiente la llamada.

Para cancelar la llamada pendiente, el cliente pasa una solicitud de cancelación a través del objeto CANCEL, que controla los detalles de la notificación al objeto de servidor de que se ha cancelado la llamada. Si no se devuelve el método llamado, el objeto de servidor, al detectar la solicitud de cancelación, limpia los recursos de programa que ha asignado y notifica a su cliente, devolviendo un valor **HRESULT** adecuado, que canceló la ejecución de la llamada. Si ya se ha devuelto el método llamado, el objeto CANCEL notifica al cliente. En cualquier caso, el subproceso del cliente se desbloquea y puede continuar el procesamiento.

La forma en que el objeto de servidor responde a una solicitud de cancelación es a discreción del implementador del servidor, pero el subproceso que realiza la llamada en el cliente siempre estará desbloqueado y omitirá los resultados que el servidor intente pasar a él. Los objetos CANCEL proporcionan un medio para solicitar que se cancele un método que se está ejecutando actualmente, pero no hay ninguna garantía de que el objeto de servidor detenga el procesamiento de la llamada. Por ejemplo, puede que la llamada ya haya devuelto o que el objeto de servidor no admita objetos de cancelación.

COM proporciona automáticamente una implementación estándar de los objetos de cancelación para objetos de cliente e interfaces que usan el cálculo de referencias estándar. En el caso de los objetos e interfaces que usan el cálculo de referencias personalizado, deberá implementar su propio objeto CANCEL.

En este momento, los objetos CANCEL solo administran llamadas sincrónicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cancelar una llamada asincrónica](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 