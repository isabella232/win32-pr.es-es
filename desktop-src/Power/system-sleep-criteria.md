---
description: Siempre que el sistema determine que hay actividad de usuario o aplicación, no entrará en suspensión.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Criterios de suspensión del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b93b0eb1a55d156a9d75b51ef826c85eabd28b29789cf50bb7f0fd7b5fee90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032825"
---
# <a name="system-sleep-criteria"></a>Criterios de suspensión del sistema

Siempre que el sistema determine que hay actividad de usuario o aplicación, no entrará en suspensión. El sistema puede detectar ciertas actividades, como la entrada del usuario o las comunicaciones de red. Sin embargo, hay otras actividades que el sistema no puede detectar. Por ejemplo, una aplicación de presentación requiere la pantalla para mostrarse. Sin embargo, puede parecer que la aplicación está inactiva durante la presentación, lo que hace que el sistema apague la pantalla.

Para notificar al sistema que la aplicación está ocupada, use la [**función SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) Esta función impide que el sistema entre en suspensión o apague la pantalla mientras se ejecuta la aplicación.

Las aplicaciones multimedia y de presentación deben llamar a la función [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con **ES DISPLAY \_ \_ REQUIRED** para que el sistema sepa que no debe poner el dispositivo de presentación en suspensión. Las aplicaciones de control de eventos, como las herramientas para administrar faxes entrantes, deben llamar a **SetThreadExecutionState** con **ES SYSTEM \_ \_ REQUIRED,** controlar el evento y, a continuación, borrar la marca para que el sistema pueda volver a suspensión. Tenga en cuenta que la mayoría de las aplicaciones de productividad no necesitan usar **SetThreadExecutionState** porque el sistema normalmente puede determinar la actividad por entrada del usuario.

Para mantener el tiempo desde la última entrada del usuario, el sistema usa un temporizador de inactividad para mostrar y un temporizador de inactividad del sistema. El sistema compara los temporizadores inactivos con los valores configurados en el plan de energía. Si el valor del temporizador de inactividad de presentación es mayor que el valor de tiempo de espera de presentación y ningún subproceso ha solicitado la presentación mediante una llamada a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) con **ES DISPLAY \_ \_ REQUIRED**, el sistema apaga la pantalla. Del mismo modo, si el temporizador de inactividad del sistema es mayor que el valor de tiempo de espera del sistema y ninguna aplicación ha solicitado el sistema mediante una llamada a **SetThreadExecutionState** con **ES SYSTEM \_ \_ REQUIRED**, el sistema entra en suspensión.

El sistema mantiene un recuento de aplicaciones que han llamado [**a SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate). El sistema realiza un seguimiento de cada subproceso que **llama a SetThreadExecutionState** y ajusta el contador en consecuencia. Si este contador alcanza cero y no ha habido ninguna entrada de usuario, el sistema entra en suspensión.

Si la energía es baja, una aplicación puede solicitar la intervención del usuario o solicitar que el sistema se suspenda. Puede suspender la operación del sistema mediante la [**función SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

Si el sistema se activa automáticamente[(PBT \_ APMRESUMEAUTOMATIC),](pbt-apmresumeautomatic.md)ninguno de los temporizadores es relevante. Para obtener más información, vea [Eventos de reactivación del sistema.](system-wake-up-events.md)

## <a name="entering-sleep"></a>Entrar en suspensión

Cuando el sistema entra en suspensión, conservará automáticamente el estado de todo el sistema y de todas las aplicaciones. Por lo tanto, la mayoría de las aplicaciones no necesitan realizar ninguna acción especial. Las aplicaciones que necesitan realizar acciones específicas antes de que las transiciones del sistema puedan registrarse para eventos de energía.

Cuando el sistema envía un evento [ \_ PBT APMSUSPEND,](pbt-apmsuspend.md) cada aplicación tiene dos segundos para realizar las acciones necesarias antes de que el sistema inicie la transición a suspensión. Las aplicaciones deben limitar la acción que llevan a cabo en respuesta a este evento para asegurarse de que completan todas las operaciones en el tiempo asignado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> </dl>

 

 



