---
description: En este tema se describe cómo se deben usar los enlaces.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Información general sobre enlaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10754f7275ce06c17b668e04c7792e6296a854fbe14a6ebc9544fbb70c73e9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201230"
---
# <a name="hooks-overview"></a>Información general sobre enlaces

Un *enlace* es un mecanismo por el que una aplicación puede interceptar eventos, como mensajes, acciones del mouse y pulsaciones de teclas. Una función que intercepta un tipo determinado de evento se conoce como procedimiento *de enlace*. Un procedimiento de enlace puede actuar en cada evento que recibe y, a continuación, modificar o descartar el evento.

En el ejemplo siguiente se usa para los enlaces:

-   Supervisión de mensajes con fines de depuración
-   Proporcionar compatibilidad para la grabación y reproducción de macros
-   Proporcionar soporte técnico para una clave de ayuda (F1)
-   Simulación de entrada de mouse y teclado
-   Implementación de una aplicación de entrenamiento basado en equipos (CBT)

> [!Note]  
> Los enlaces tienden a ralentizar el sistema porque aumentan la cantidad de procesamiento que el sistema debe realizar para cada mensaje. Debe instalar un enlace solo cuando sea necesario y quitarlo lo antes posible.

 

En esta sección se describe lo siguiente:

-   [Cadenas de enlace](#hook-chains)
-   [Procedimientos de enlace](#hook-procedures)
-   [Tipos de enlace](#hook-types)
    -   [WH \_ CALLWNDPROC y WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [DEPURACIÓN \_ DE WH](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
    -   [TECLADO \_ WH](#wh_keyboard)
    -   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
    -   [WH \_ MOUSE](#wh_mouse)
    -   [WH \_ MSGFILTER y WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [SHELL \_ DE WH](#wh_shell)

## <a name="hook-chains"></a>Cadenas de enlace

El sistema admite muchos tipos diferentes de enlaces; cada tipo proporciona acceso a un aspecto diferente de su mecanismo de control de mensajes. Por ejemplo, una aplicación puede usar el enlace [WH \_ MOUSE](#wh_mouse) para supervisar el tráfico de mensajes para los mensajes del mouse.

El sistema mantiene una cadena de enlace independiente para cada tipo de enlace. Una *cadena de enlace* es una lista de punteros a funciones de devolución de llamada especiales definidas por la aplicación denominadas *procedimientos de enlace*. Cuando se produce un mensaje que está asociado a un tipo determinado de enlace, el sistema pasa el mensaje a cada procedimiento de enlace al que se hace referencia en la cadena de enlace, uno después del otro. La acción que puede realizar un procedimiento de enlace depende del tipo de enlace implicado. Los procedimientos de enlace para algunos tipos de enlaces solo pueden supervisar mensajes; otros usuarios pueden modificar los mensajes o detener su progreso a través de la cadena, lo que les impide alcanzar el siguiente procedimiento de enlace o la ventana de destino.

## <a name="hook-procedures"></a>Procedimientos de enlace

Para aprovechar un tipo determinado de enlace, el desarrollador proporciona un procedimiento de enlace y usa la función [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) para instalarlo en la cadena asociada al enlace. Un procedimiento de enlace debe tener la sintaxis siguiente:

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc es* un marcador de posición para un nombre definido por la aplicación.

El *parámetro nCode* es un código de enlace que el procedimiento de enlace usa para determinar la acción que se va a realizar. El valor del código de enlace depende del tipo del enlace; cada tipo tiene su propio conjunto de características de códigos de enlace. Los valores de los *parámetros wParam* y *lParam* dependen del código de enlace, pero normalmente contienen información sobre un mensaje enviado o publicado.

La [**función SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) siempre instala un procedimiento de enlace al principio de una cadena de enlace. Cuando se produce un evento supervisado por un tipo determinado de enlace, el sistema llama al procedimiento al principio de la cadena de enlace asociada al enlace. Cada procedimiento de enlace de la cadena determina si se debe pasar el evento al procedimiento siguiente. Un procedimiento de enlace pasa un evento al siguiente procedimiento llamando a la [**función CallNextHookEx.**](/windows/win32/api/winuser/nf-winuser-callnexthookex)

Tenga en cuenta que los procedimientos de enlace para algunos tipos de enlaces solo pueden supervisar los mensajes. el sistema pasa mensajes a cada procedimiento de enlace, independientemente de si un procedimiento determinado llama a [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).

Un *enlace global supervisa* los mensajes de todos los subprocesos del mismo escritorio que el subproceso que realiza la llamada. Un *enlace específico del subproceso* supervisa los mensajes solo para un subproceso individual. Se puede llamar a un procedimiento de enlace global en el contexto de cualquier aplicación en el mismo escritorio que el subproceso de llamada, por lo que el procedimiento debe estar en un módulo DLL independiente. Solo se llama a un procedimiento de enlace específico del subproceso en el contexto del subproceso asociado. Si una aplicación instala un procedimiento de enlace para uno de sus propios subprocesos, el procedimiento de enlace puede estar en el mismo módulo que el resto del código de la aplicación o en un archivo DLL. Si la aplicación instala un procedimiento de enlace para un subproceso de una aplicación diferente, el procedimiento debe estar en un archivo DLL. Para obtener información, vea [Bibliotecas de vínculos dinámicos](../dlls/dynamic-link-libraries.md).

> [!Note]  
> Debe usar enlaces globales solo con fines de depuración; De lo contrario, debe evitarlos. Los enlaces globales dañan el rendimiento del sistema y provocan conflictos con otras aplicaciones que implementan el mismo tipo de enlace global.

 

## <a name="hook-types"></a>Tipos de enlace

Cada tipo de enlace permite a una aplicación supervisar un aspecto diferente del mecanismo de control de mensajes del sistema. En las secciones siguientes se describen los enlaces disponibles.

-   [WH \_ CALLWNDPROC y WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [DEPURACIÓN \_ DE WH](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
-   [TECLADO \_ WH](#wh_keyboard)
-   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
-   [WH \_ MOUSE](#wh_mouse)
-   [WH \_ MSGFILTER y WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [SHELL \_ DE WH](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC y WH \_ CALLWNDPROCRET

Los **enlaces WH \_ CALLWNDPROC** y **WH \_ CALLWNDPROCRET** permiten supervisar los mensajes enviados a los procedimientos de ventana. El sistema llama a un procedimiento de enlace **WH \_ CALLWNDPROC** antes de pasar el mensaje al procedimiento de la ventana receptora y llama al procedimiento de enlace **WH \_ CALLWNDPROCRET** después de que el procedimiento de ventana haya procesado el mensaje.

El **enlace \_ WH CALLWNDPROCRET** pasa un puntero a una [**estructura CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) al procedimiento de enlace. La estructura contiene el valor devuelto del procedimiento de ventana que procesó el mensaje, así como los parámetros de mensaje asociados al mensaje. La subclases de la ventana no funciona para los mensajes establecidos entre procesos.

Para obtener más información, vea las funciones de devolución de llamada [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) [*y CallWndRetProc.*](/windows/win32/api/winuser/nc-winuser-hookproc)

### <a name="wh_cbt"></a>WH \_ CBT

El sistema llama a un procedimiento de enlace **\_ CBT** de WH antes de activar, crear, destruir, minimizar, maximizar, mover o ajustar el tamaño de una ventana; antes de completar un comando del sistema; antes de quitar un evento de mouse o teclado de la cola de mensajes del sistema; antes de establecer el foco de entrada; o antes de sincronizar con la cola de mensajes del sistema. El valor que devuelve el procedimiento de enlace determina si el sistema permite o impide una de estas operaciones. El **enlace \_ CBT** de WH está pensado principalmente para aplicaciones de entrenamiento basado en equipos (CBT).

Para obtener más información, vea la función de devolución de [*llamada CBTProc.*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))

Para obtener información, vea [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>DEPURACIÓN \_ DE WH

El sistema llama a un procedimiento **de \_ enlace WH DEBUG** antes de llamar a los procedimientos de enlace asociados a cualquier otro enlace del sistema. Puede usar este enlace para determinar si se permite que el sistema llame a procedimientos de enlace asociados a otros tipos de enlaces.

Para obtener más información, vea la [*función de devolución de llamada DebugProc.*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

El **enlace \_ FOREGROUNDIDLE** de WH permite realizar tareas de prioridad baja durante los momentos en que su subproceso en primer plano está inactivo. El sistema llama a un procedimiento de enlace **\_ DE WH FOREGROUNDIDLE** cuando el subproceso en primer plano de la aplicación está a punto de estar inactivo.

Para obtener más información, vea la función [*de devolución de llamada ForegroundIdleProc.*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85))

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

El **enlace \_ GETMESSAGE de WH** permite a una aplicación supervisar los mensajes que la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) va a devolver. Puede usar el enlace **WH \_ GETMESSAGE** para supervisar la entrada del mouse y el teclado y otros mensajes publicados en la cola de mensajes.

Para obtener más información, vea la función de devolución de [*llamada GetMsgProc.*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

El **enlace \_ JOURNALPLAYBACK de WH** permite a una aplicación insertar mensajes en la cola de mensajes del sistema. Puede usar este enlace para reproducir una serie de eventos de mouse y teclado registrados anteriormente mediante [WH \_ JOURNALRECORD](#wh_journalrecord). La entrada normal del mouse y el teclado está deshabilitada siempre que se instale un enlace **\_ WH JOURNALPLAYBACK.** Un **enlace \_ WH JOURNALPLAYBACK** es un enlace global, no se puede usar como un enlace específico del subproceso.

El **enlace \_ JOURNALPLAYBACK de WH** devuelve un valor de tiempo de espera. Este valor indica al sistema cuántos milisegundos hay que esperar antes de procesar el mensaje actual desde el enlace de reproducción. Esto permite que el enlace controle el tiempo de los eventos que reproduce.

Para obtener más información, vea la [*función de devolución de llamada JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

El **enlace \_ JOURNALRECORD de WH** permite supervisar y registrar eventos de entrada. Normalmente, este enlace se usa para registrar una secuencia de eventos de mouse y teclado para reproducir más adelante mediante [WH \_ JOURNALPLAYBACK](#wh_journalplayback). El **enlace \_ JOURNALRECORD de WH** es un enlace global, no se puede usar como un enlace específico del subproceso.

Para obtener más información, vea la [*función de devolución de llamada JournalRecordProc.*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))

### <a name="wh_keyboard_ll"></a>WH \_ KEYBOARD \_ LL

El **enlace WH KEYBOARD \_ \_ LL** permite supervisar los eventos de entrada de teclado que se va a publicar en una cola de entrada de subprocesos.

Para obtener más información, vea la función de devolución de llamada [*LowLevelKeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85))

### <a name="wh_keyboard"></a>WH \_ KEYBOARD

El **enlace \_ WH KEYBOARD** permite a una aplicación supervisar el tráfico de mensajes para los mensajes WM [**\_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) a punto de ser devueltos por la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) Puede usar el enlace **WH \_ KEYBOARD** para supervisar la entrada de teclado publicada en una cola de mensajes.

Para obtener más información, vea la función de devolución de [*llamada KeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85))

### <a name="wh_mouse_ll"></a>WH \_ MOUSE \_ LL

El **enlace WH MOUSE \_ \_ LL** le permite supervisar los eventos de entrada del mouse a punto de publicarse en una cola de entrada de subprocesos.

Para obtener más información, vea la [*función de devolución de llamada LowLevelMouseProc.*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85))

### <a name="wh_mouse"></a>WH \_ MOUSE

El **enlace \_ WH MOUSE** permite supervisar los mensajes del mouse a punto de ser devueltos por la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) Puede usar el enlace **WH \_ MOUSE** para supervisar la entrada del mouse publicada en una cola de mensajes.

Para obtener más información, vea la función de devolución de [*llamada MouseProc.*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ MSGFILTER y WH \_ SYSMSGFILTER

Los enlaces **\_ WH MSGFILTER** y **WH \_ SYSMSGFILTER** permiten supervisar los mensajes a punto de ser procesados por un menú, una barra de desplazamiento, un cuadro de mensaje o un cuadro de diálogo, y detectar cuándo se va a activar una ventana diferente como resultado de que el usuario presione la combinación de teclas ALT+TAB o ALT+ESC. El **enlace \_ MSGFILTER de WH** solo puede supervisar los mensajes pasados a un menú, barra de desplazamiento, cuadro de mensaje o cuadro de diálogo creado por la aplicación que instaló el procedimiento de enlace. El **enlace \_ SYSMSGFILTER de WH** supervisa estos mensajes para todas las aplicaciones.

Los **enlaces \_ WH MSGFILTER** y **WH \_ SYSMSGFILTER** permiten realizar el filtrado de mensajes durante bucles modales equivalentes al filtrado realizado en el bucle de mensajes principal. Por ejemplo, una aplicación a menudo examina un nuevo mensaje en el bucle main entre el momento en que recupera el mensaje de la cola y el momento en que envía el mensaje, realizando un procesamiento especial según corresponda. Sin embargo, durante un bucle modal, el sistema recupera y envía mensajes sin permitir que una aplicación filtre los mensajes en su bucle de mensajes principal. Si una aplicación instala un procedimiento de enlace **\_ WH MSGFILTER** o **WH \_ SYSMSGFILTER,** el sistema llama al procedimiento durante el bucle modal.

Una aplicación puede llamar directamente al **enlace \_ MSGFILTER de WH** llamando a la función [**CallMsgFilter.**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) Mediante esta función, la aplicación puede usar el mismo código para filtrar los mensajes durante los bucles modales que usa en el bucle de mensajes principal. Para ello, encapsula las operaciones de filtrado en un procedimiento de enlace **WH \_ MSGFILTER** y llama a **CallMsgFilter** entre las llamadas a las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

El último argumento de [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) simplemente se pasa al procedimiento de enlace; puede escribir cualquier valor. El procedimiento de enlace, mediante la definición de una constante como **MSGF \_ MAINLOOP**, puede usar este valor para determinar desde dónde se llamó al procedimiento.

Para obtener más información, vea las funciones de devolución de llamada [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) [*y SysMsgProc.*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85))

### <a name="wh_shell"></a>SHELL \_ DE WH

Una aplicación de shell puede usar el enlace **\_ DE SHELL** de WH para recibir notificaciones importantes. El sistema llama a un procedimiento de enlace **de WH \_ SHELL** cuando la aplicación de shell está a punto de activarse y cuando se crea o destruye una ventana de nivel superior.

Tenga en cuenta que las aplicaciones de shell personalizadas no reciben **mensajes de WH \_ SHELL.** Por lo tanto, cualquier aplicación que se registre como el shell predeterminado debe llamar a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) antes de que él (o cualquier otra aplicación) pueda recibir mensajes **de WH \_ SHELL.** Se debe llamar a esta función **con SPI \_ SETMINIMIZEDMETRICS** y una [**estructura MINIMIZEDMETRICS.**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) Establezca el **miembro iArrange** de esta estructura en **ARW \_ HIDE**.

Para obtener más información, vea la función de devolución de [*llamada ShellProc.*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))

 

 
