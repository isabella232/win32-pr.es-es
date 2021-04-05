---
description: Siempre que el sistema determine que hay una actividad de usuario o de aplicación, no entrará en modo de suspensión.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Criterios de suspensión del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813779"
---
# <a name="system-sleep-criteria"></a>Criterios de suspensión del sistema

Siempre que el sistema determine que hay una actividad de usuario o de aplicación, no entrará en modo de suspensión. El sistema puede detectar ciertas actividades, como la entrada de usuario o las comunicaciones de red. Sin embargo, hay otras actividades que el sistema no puede detectar. Por ejemplo, una aplicación de presentación requiere que la pantalla se muestre. Sin embargo, puede parecer que la aplicación está inactiva durante la presentación, lo que hace que el sistema desactive la pantalla.

Para notificar al sistema que la aplicación está ocupada, utilice la función [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) . Esta función evita que el sistema entre en suspensión o apaga la pantalla mientras la aplicación se está ejecutando.

Las aplicaciones de presentación y multimedia deben llamar a la función [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con la **\_ pantalla es \_ necesaria** para que el sistema sepa que no debe poner el dispositivo de pantalla en modo de suspensión. Las aplicaciones de control de eventos, como las herramientas para administrar los faxes entrantes, deben llamar a **SetThreadExecutionState** con el **\_ sistema es \_ necesario**, controlar el evento y, a continuación, borrar la marca para que el sistema pueda volver a entrar en modo de suspensión. Tenga en cuenta que la mayoría de las aplicaciones de productividad no necesitan usar **SetThreadExecutionState** porque el sistema normalmente puede determinar la actividad mediante la entrada del usuario.

Para mantener el tiempo transcurrido desde la última entrada del usuario, el sistema utiliza un temporizador de inactividad de pantalla y un temporizador de inactividad del sistema. El sistema compara los temporizadores de inactividad con los valores configurados en el plan de energía. Si el valor del temporizador de inactividad de la pantalla es mayor que el valor de tiempo de espera de la presentación y ningún subproceso solicitó la presentación mediante una llamada a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con la **presentación de es \_ \_ necesaria**, el sistema apaga la pantalla. Del mismo modo, si el temporizador inactivo del sistema es mayor que el valor de tiempo de espera del sistema y ninguna aplicación ha solicitado el sistema mediante una llamada a **SetThreadExecutionState** con el **\_ sistema es \_ necesario**, el sistema entra en suspensión.

El sistema mantiene un recuento de las aplicaciones que han llamado a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate). El sistema realiza un seguimiento de cada subproceso que llama a **SetThreadExecutionState** y ajusta el contador en consecuencia. Si este contador llega a cero y no se ha producido ninguna acción del usuario, el sistema entra en suspensión.

Si la alimentación es baja, una aplicación puede solicitar la intervención del usuario o solicitar que el sistema se suspenda. Puede suspender el funcionamiento del sistema mediante la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Si el sistema se reactiva automáticamente ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)), ninguno de los temporizadores es relevante. Para obtener más información, consulte [eventos de reactivación del sistema](system-wake-up-events.md).

## <a name="entering-sleep"></a>Entrar en suspensión

Cuando el sistema entra en suspensión, conserva automáticamente el estado de todo el sistema y de todas las aplicaciones. Por lo tanto, la mayoría de las aplicaciones no tienen que realizar ninguna acción especial. Las aplicaciones que necesitan realizar acciones específicas antes de las transiciones del sistema se pueden registrar para los eventos de energía.

Cuando el sistema envía un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) , cada aplicación tiene dos segundos para realizar las acciones necesarias antes de que el sistema inicie la transición al modo de suspensión. Las aplicaciones deben limitar la acción que se lleva a cabo en respuesta a este evento para asegurarse de que completan todas las operaciones en el tiempo asignado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> </dl>

 

 



