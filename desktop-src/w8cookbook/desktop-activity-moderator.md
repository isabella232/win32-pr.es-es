---
title: Moderador de la actividad del escritorio
description: Moderador de la actividad del escritorio
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- duración de la batería
- espera conectada
- Suspensión
- limitación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b465bbb377a06fdad50d04d5fcf788cb2e687fdf5db852125e4143fd971773d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815425"
---
# <a name="desktop-activity-moderator"></a>Moderador de la actividad del escritorio

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


> [!Note]  
> EL SISTEMA DE CONSUMO solo está presente en Windows 8 equipos cliente que admiten el modo de espera conectado. EL SISTEMA DE ACCESO no está presente en las SKU del servidor.

 

  

> [!Note]  
> Windows Las aplicaciones de la tienda Windows 8 no se verán afectadas por el SISTEMA DE SEGURIDAD.

 

  
</dl>

## <a name="description"></a>Descripción

Nuestros clientes se desplazan hacia plataformas más ligeras, más pequeñas y móviles para satisfacer sus necesidades informáticas. Como parte del cambio a los dispositivos móviles, los usuarios se han preocupar cada vez más por la duración de la batería de sus dispositivos. Desktop Activity Moderator (DAM) es una de las nuevas características de Windows 8 diseñadas para garantizar una duración de la batería coherente y larga para los dispositivos que admiten el modo de espera conectado.

El modo de espera conectado se produce cuando el dispositivo está encendido, pero la pantalla está apagada. En este estado de energía, el sistema está técnicamente siempre "encendido" (para admitir escenarios clave como correo, VoIP, redes sociales y mensajería instantánea con aplicaciones de Windows Store). Es análogo al estado en el que se encuentra un teléfono inteligente cuando el usuario presiona el botón de encendido.

Por lo tanto, el software (incluidas las aplicaciones y el software del sistema operativo) debe comportarse correctamente durante el modo de espera conectado. La clase DAM se creó para suprimir la ejecución de aplicaciones de escritorio de forma similar al estado de suspensión (S3 en dispositivos ACPI). Para ello, suspende o limita los procesos de software de escritorio en todo el sistema tras la entrada en espera conectada. Esto permite a los sistemas que admiten el modo de espera conectado ofrecer un uso mínimo de los recursos y una duración de la batería larga y coherente, al tiempo que permite que las aplicaciones de Windows Store proporcionen las experiencias conectadas que ofrecen.

## <a name="details"></a>Detalles

EL SISTEMA DE CARGA es un controlador en modo kernel que se carga e inicializa en el arranque del sistema si el sistema admite el modo de espera conectado. (Esto se determina mediante la evaluación de si el campo AOAC del sistema \_ La \_ estructura POWER CAPABILITIES devuelta por CallNtPowerInformation se establece en TRUE).

Cuando se habilita EL SISTEMA DE ACCESO Y se crea el proceso de escritorio, el SISTEMA AGREGA el proceso a los objetos de trabajo administrados por el sistema:

-   Si el proceso se creó en la sesión 0, LAN agrega el proceso a un objeto de trabajo sujeto a **limitación**
-   Si el proceso se creó en una sesión interactiva (sesión 1 o superior), LAN agrega el proceso a un objeto de trabajo sujeto a **suspensión.**

> [!Note]  
> Por Windows 8, los objetos de trabajo se pueden anidar. Esto significa que el uso de objetos de trabajo por parte de LAN no interfiere con el uso existente de objetos de trabajo de una aplicación.

 

Cuando la pantalla está en pantalla, el sistema DESA se desactiva y no afecta a ningún proceso del sistema. Cuando el sistema está en modo de espera conectado, en función de la actividad del sistema, LAN podría limitar o suspender los procesos.

-   Los procesos que están sujetos a suspensión tienen todos sus subprocesos suspendidos (no pueden ejecutarse en ninguna circunstancia); Se mantiene el estado de la aplicación (memoria de proceso)
-   Procesos que están sujetos a un ciclo de limitación entre suspendidos y sin suspensión (una gran mayoría del tiempo se dedica al estado suspendido)
    -   Tenga en cuenta Windows que también pueden detectar que se están produciendo actividades críticas y podrían no tener en cuenta los servicios con limitaciones durante períodos de tiempo más largos durante esta actividad.
    -   Además, tenga en cuenta que mientras están en espera conectada, es posible que los sensores y las redes no estén disponibles, por lo que los procesos con limitación deben diseñarse para ser resistentes a condiciones de red deficientes (para la mayoría de los procesos, esto no requiere ningún cambio).

Cuando se activa o desactiva la suspensión de LA SUSPENSIÓN, LAN desencadena la entrega de un mensaje WM POWERBROADCAST a los procesos sujetos a suspensión que han participado en la entrega de mensajes (a través de la llamada API o la corrección de compatibilidad, que se describe más \_ adelante). Después de unos segundos de retraso, LAN suspende el proceso.

No hay notificaciones cuando se activa o se desasombre la limitación de LAN. Los procesos no deben ser modificados; los procesos siguen funcionando, aunque a una velocidad más lenta.

## <a name="manifestation"></a>Manifestación

Los procesos a menudo se suspenden o limitan durante el estado de espera conectado. Para la mayoría de las aplicaciones suspendidas, esto debe ser muy similar a una transición de suspensión/ reanudación de S3 o hibernación/reanudación de S4. Entre las expresiones se incluyen, entre otras, incoherencias en tiempo de actividad/tiempo de ejecución frente a tiempo de reloj, incoherencias en el comportamiento del temporizador o cambios drásticos en el estado del sistema operativo antes y después de que se complete la suspensión.

La suspensión y la limitación se produce como una unidad (todos los procesos suspendibles se suspenden y no se suspenden al unísono, y todos los procesos que se pueden limitar se limitan y no se limitan al unísono), por lo que la comunicación entre dos procesos suspendidos o dos procesos con limitaciones no supone un problema.

El software que se basa en la comunicación entre procesos puede necesitar una consideración especial:

-   **Comunicación entre los procesos de la sesión 0 (limitada)** y la sesión 1+ (suspendida): algunos ejemplos incluyen iconos de bandeja o componentes de interfaz de usuario que representan el estado actual del servicio.
-   Comunicación entre componentes en modo de usuario **(sesión 0 o 1)** y controladores (que no están limitadas ni suspendidas): algunos ejemplos incluyen servicios que funcionan en nombre de un controlador.

En estos casos, si la comunicación entre procesos no se controla correctamente, las aplicaciones pueden aparecer como desaprobadas o no responder (aunque es posible que el usuario no vea este impacto directamente, ya que la pantalla estará desactivada cuando esté en espera conectada). Sin embargo, en la mayoría de los casos, los servicios y los controladores ya deben desarrollarse para ser sólidos frente a problemas de comunicación entre procesos.

Los proveedores que crean software para la web o que dependen de este deben considerar cómo afecta la suspensión del proceso a la duración de la conexión y los protocolos de enlace. Además, dado que es posible que la conectividad de red no esté disponible en modo de espera conectada, los desarrolladores de procesos creados en la sesión 0 deben ser especialmente conscientes de cómo afectan las conexiones de red intermitentes al proceso.

## <a name="solution"></a>Solución

Windows Las aplicaciones de la tienda no se verán afectadas por el SISTEMA DE SEGURIDAD. Si la aplicación de escritorio se ve afectada por el sistema DESA, puede solicitar notificaciones antes de que se desasocie la suspensión (por ejemplo, para guardar el estado o cerrar las conexiones de red) mediante uno de estos métodos:

-   Si la aplicación tiene una ventana (HWND) y desea controlar estas notificaciones a través del procedimiento de ventana, llame a [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) para registrarse para estos mensajes (o [UnregisterSuspendResumeNotification para](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) anular el registro). Puede usar DEVICE NOTIFY WINDOW HANDLE en el parámetro Flags y pasar el HWND de la ventana \_ \_ como parámetro \_ Recipient. El mensaje recibido es el mensaje \_ WM POWERBROADCAST.
-   Si la aplicación no tiene una ventana (HWND) o desea una devolución de llamada directa, llame a [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) para registrarse para estos mensajes (o [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) para anular el registro). Debe usar DEVICE NOTIFY CALLBACK en el parámetro Flags y pasar un valor de \_ \_ tipo PDEVICE NOTIFY SUBSCRIBE \_ PARAMETERS en el parámetro \_ \_ Recipient.
-   Si no se puede volver a compilar la aplicación, puede optar por recibir estos mensajes DE WM POWERBROADCAST a través del kit de herramientas \_ [de AppCompat](../win7appqual/application-compatibility-toolkit--act-.md) (mediante la corrección de compatibilidad (shim) promote SHIM.

El mensaje de suspensión es WM \_ POWERBROADCAST con wParam=PBT APMSUSPEND; este mensaje se difunde simultáneamente a todos los procesos que participaron en el \_ sistema. La aplicación debe realizar cualquier trabajo en la ruta de acceso de suspensión de forma rápida y eficaz. El tiempo de espera después de la notificación de difusión es global, no por proceso, por lo que el proceso podría estar contendiendo por los recursos del sistema si el trabajo necesario en esta ruta es amplio.

El mensaje de reanudación es WM \_ POWERBROADCAST con wParam=PBT APMRESUME; este mensaje se difunde simultáneamente a todos los procesos que participaron después de una \_ reanudación. No se garantiza el tiempo relativo de entrega a la salida del sistema del modo de espera conectado.

En el caso de las aplicaciones relacionadas con la cámara, cuando se realiza la transición de estado de energía, durante la notificación de suspensión, las aplicaciones deben liberar todas las referencias a la cámara (todos los objetos de canalización de captura deben apagarse y eliminarse).  Para evitar una posible purga de batería, en los sistemas Windows 10 RS3+ Cámara de Windows el servicio Frame Server cerrará todas las sesiones de captura si la aplicación no controla correctamente la notificación de suspensión.  El efecto secundario de esto es que cuando el sistema sale del estado de espera o S3/S4, la canalización de captura de la aplicación ya no está en estado de funcionamiento.

## <a name="tests"></a>Pruebas

Pruebe el software en las transiciones en espera conectadas.

## <a name="resources"></a>Recursos

-   [Soluciones de duración de la batería móvil para Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [FUNCIONALIDADES \_ DE ENERGÍA \_ DEL SISTEMA](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [Función CallNtPowerInformation](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Objetos de trabajo](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Kit de herramientas de AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 