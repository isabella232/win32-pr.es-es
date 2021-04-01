---
title: Moderador de la actividad del escritorio
description: Moderador de la actividad del escritorio
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- duración de la batería
- en modo de espera conectado
- suspensivo
- limitación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8bb3d7925633d3feca8bb6ed5af191670af681
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794188"
---
# <a name="desktop-activity-moderator"></a>Moderador de la actividad del escritorio

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


> [!Note]  
> La madre solo está presente en equipos cliente de Windows 8 que admiten el modo de espera conectado. El DAM no está presente en las SKU del servidor.

 

  

> [!Note]  
> Las aplicaciones de la tienda Windows compiladas para Windows 8 no se ven afectadas por la madre.

 

  
</dl>

## <a name="description"></a>Descripción

Nuestros clientes están desplazando hacia las plataformas más claras, más pequeñas y más móviles para satisfacer sus necesidades informáticas. Como parte de la transición a los dispositivos móviles, los usuarios están cada vez más preocupados por la duración de la batería de sus dispositivos. El moderador de actividades de escritorio (DAM) es una de las nuevas características de Windows 8 diseñadas para garantizar una larga duración de la batería para dispositivos que admiten el modo de espera conectado.

El modo de espera conectado se produce cuando el dispositivo está encendido, pero la pantalla está desactivada. En este estado de energía, el sistema técnicamente siempre está "activado" (para admitir escenarios clave como correo, VoIP, redes sociales y mensajería instantánea con aplicaciones de la tienda Windows). Es análogo al estado en el que se encuentra un smartphone cuando el usuario presiona el botón de encendido.

Como tal, el software (incluidas las aplicaciones y el software del sistema operativo) debe comportarse correctamente durante el modo de espera conectado. El DAM se creó para suprimir la ejecución de la aplicación de escritorio de forma similar al estado de suspensión (S3 en dispositivos ACPI). Esto lo hace suspendiendo o limitando los procesos de software de escritorio en el sistema tras la entrada en espera conectada. Esto permite a los sistemas que admiten Connected Standby ofrecer un uso minimizado de los recursos y una duración de la batería larga y coherente, al tiempo que permite que las aplicaciones de la tienda Windows entreguen las experiencias conectadas que prometen

## <a name="details"></a>Detalles

La DAM es un controlador de modo kernel que se carga y se inicializa durante el arranque del sistema si el sistema admite el modo de espera conectado. (Esto se determina mediante la evaluación de si el campo AOAC del sistema \_ La \_ estructura de capacidades de energía devuelta por CallNtPowerInformation está establecida en true).

Cuando el DAM está habilitado y se crea el proceso de escritorio, el DAM agrega el proceso a objetos de trabajo administrados por el sistema:

-   Si el proceso se creó en la sesión 0, DAM agrega el proceso a un objeto de trabajo sujeto a **limitación**
-   Si el proceso se ha creado en una sesión interactiva (sesión 1 o superior), DAM agrega el proceso a un objeto de trabajo sujeto a **suspensión** .

> [!Note]  
> En Windows 8, los objetos de trabajo se pueden anidar. Esto significa que el uso de los objetos de trabajo de la madre no interfiere con el uso existente de los objetos de trabajo de la aplicación.

 

Cuando la pantalla está activada, el DAM se desactivará y no afectará a ningún proceso del sistema. Cuando el sistema está en modo de espera conectado, dependiendo de la actividad en el sistema, DAM podría limitar o suspender procesos.

-   Los procesos que están sujetos a la suspensión tienen suspendidos todos los subprocesos (no se permite que se ejecuten en ninguna circunstancia); se mantiene el estado de la aplicación (memoria de proceso)
-   Procesos que están sujetos al ciclo de limitación entre suspendido y sin suspender (una gran mayoría de tiempo se dedica al estado suspendido)
    -   Tenga en cuenta que Windows también puede detectar que se están produciendo actividades críticas y podría no suspender los servicios limitados durante períodos de tiempo más largos durante esta actividad.
    -   Además, tenga en cuenta que, mientras está en modo de espera conectado, es posible que los sensores y redes no estén disponibles, por lo que los procesos limitados deben diseñarse para ser resistentes a condiciones de red deficientes (para la mayoría de los procesos, esto no requiere ningún cambio).

Cuando se contrae o se desactive la suspensión de DAM, el DAM desencadena la entrega de un mensaje de POWERBROADCAST de WM \_ a esos procesos sujetos a la suspensión que ha optado por la entrega de mensajes (a través de correcciones de compatibilidad o llamada de API, que se describe más adelante). Después de un retraso de unos segundos, DAM suspende el proceso.

No hay notificaciones cuando el límite de la DAM está embragado o desactivado. No es necesario modificar los procesos; los procesos continúan funcionando, aunque a una velocidad inferior.

## <a name="manifestation"></a>Manifestación

Los procesos se suelen suspender o limitar durante el estado de espera conectado. Para la mayoría de las aplicaciones suspendidas, esto debe ser muy similar a una transición de S3/reanudación de S3 o de hibernación/reanudación de S4. Manifestaciones puede incluir, pero no se limita a las incoherencias en tiempo de actividad/tiempo de ejecución frente a tiempo de reloj de la pared, incoherencias en el comportamiento del temporizador o cambios drásticos en el estado del sistema operativo antes y después de que se complete la suspensión.

La suspensión y la limitación se producen como una unidad (todos los procesos que se pueden suspender se suspenden y no se suspenden en el unísono, y todos los procesos que se pueden limitar se limitan y no se limitan al unísono), por lo que la comunicación entre dos procesos suspendidos o dos procesos limitados no plantea ningún problema.

El software que se basa en la comunicación entre procesos puede necesitar una consideración especial:

-   **Comunicación entre procesos en la sesión 0 (limitado) y sesión 1 + (suspendido)** : algunos ejemplos incluyen iconos de bandeja o componentes de interfaz de usuario que representan el estado actual del servicio.
-   **Comunicación entre componentes en modo de usuario (sesión 0 o 1) y controladores (que no están limitados ni suspendidos)** : algunos ejemplos incluyen servicios que funcionan en nombre de un controlador

En estos casos, si la comunicación entre procesos no se controla correctamente, las aplicaciones pueden aparecer bloqueadas o no responden (aunque es posible que el usuario no vea este impacto directamente, ya que la pantalla se apagará cuando esté en modo de espera conectado). Sin embargo, en la mayoría de los casos, los servicios y los controladores ya deben estar desarrollados para ser sólidos contra problemas de comunicación entre procesos.

Los proveedores que crean software para, o que dependen de, deben tener en cuenta cómo la suspensión del proceso afecta a las duraciones de conexión y los protocolos de enlace. Además, dado que es posible que la conectividad de red no esté disponible en el modo de espera conectado, los desarrolladores de procesos creados en la sesión 0 deben tener en cuenta especialmente el modo en que las conexiones de red intermitentes afectan al proceso.

## <a name="solution"></a>Solución

Las aplicaciones de la tienda Windows no se ven afectadas por la madre. Si la aplicación de escritorio se ve afectada por la madre, puede solicitar notificaciones antes de que se lleve a cabo la suspensión (por ejemplo, para guardar el estado o cerrar las conexiones de red) mediante uno de estos métodos:

-   Si la aplicación tiene una ventana (HWND) y desea controlar estas notificaciones a través del procedimiento de ventana, llame a [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) para registrar estos mensajes (o [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) para anular el registro). Puede usar \_ \_ \_ el identificador de la ventana de notificación del dispositivo en el parámetro flags y pasar el HWND de la ventana en como parámetro de destinatario. El mensaje recibido es el mensaje de POWERBROADCAST de WM \_ .
-   Si la aplicación no tiene una ventana (HWND) o desea una devolución de llamada directa, llame a [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) para registrar estos mensajes (o [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) para anular el registro). Debe usar \_ \_ la devolución de llamada de notificación de dispositivo en el parámetro flags y pasar un valor de tipo PDEVICE \_ Notify \_ subscribe \_ Parameters en el parámetro Recipient.
-   Si no se puede volver a compilar la aplicación, puede optar por recibir estos mensajes de WM \_ POWERBROADCAST a través del [Kit de herramientas de AppCompat](../win7appqual/application-compatibility-toolkit--act-.md) (mediante la corrección de compatibilidad de PromoteDAM).

El mensaje Suspend es WM \_ POWERBROADCAST con wParam = PBT \_ APMSUSPEND; este mensaje se transmite simultáneamente a todos los procesos que se hayan incorporado en el sistema. La aplicación debe realizar cualquier trabajo en la ruta de acceso de suspensión de forma rápida y eficaz. El tiempo de espera después de la notificación de difusión es global, no por proceso, por lo que es posible que el proceso esté intentando tener recursos del sistema si el trabajo necesario en esta ruta de acceso es amplio.

El mensaje de reanudación es WM \_ POWERBROADCAST con wParam = PBT \_ APMRESUME; este mensaje se difundirá simultáneamente a todos los procesos que se hayan incorporado después de reanudarse. No se garantiza el tiempo relativo de entrega a la salida del sistema desde el modo de espera conectado.

En el caso de las aplicaciones relacionadas con la cámara, cuando se lleva a cabo la transición del estado de energía, durante la notificación de suspensión, las aplicaciones deben liberar todas las referencias a la cámara (todos los objetos de canalización de captura deben cerrarse y eliminarse).  Para evitar una posible purga de la batería, en Windows 10 RS3 + Systems, el servicio del servidor de trama de la cámara de Windows cerrará todas las sesiones de captura si la aplicación no controla correctamente la notificación de suspensión.  El efecto secundario de esto es que cuando el sistema sale del estado en espera o S3/S4, la canalización de captura de la aplicación ya no está en un estado de funcionamiento.

## <a name="tests"></a>Pruebas

Pruebe el software en las transiciones de modo de espera conectadas.

## <a name="resources"></a>Recursos

-   [Soluciones de duración de batería móvil para Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [\_capacidades de energía del sistema \_](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [CallNtPowerInformation función)](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Objetos de trabajo](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Kit de herramientas AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 