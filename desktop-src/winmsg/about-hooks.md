---
description: En este tema se describe cómo se deben usar los enlaces.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Información general sobre enlaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659939"
---
# <a name="hooks-overview"></a>Información general sobre enlaces

Un *enlace* es un mecanismo por el que una aplicación puede interceptar eventos, como mensajes, acciones del mouse y pulsaciones de teclas. Una función que intercepta un tipo determinado de evento se conoce como procedimiento de *enlace*. Un procedimiento de enlace puede actuar en cada evento que recibe y, a continuación, modificar o descartar el evento.

En el siguiente ejemplo se usan los enlaces:

-   Supervisar mensajes con fines de depuración
-   Proporcionar compatibilidad para grabar y reproducir macros
-   Proporcionar compatibilidad con una tecla de ayuda (F1)
-   Simular la entrada del mouse y del teclado
-   Implementar una aplicación de aprendizaje basado en equipos (CBT)

> [!Note]  
> Los enlaces tienden a ralentizar el sistema porque aumentan la cantidad de procesamiento que el sistema debe realizar para cada mensaje. Solo debe instalar un enlace cuando sea necesario y quitarlo lo antes posible.

 

En esta sección se trata lo siguiente:

-   [Cadenas de enlace](#hook-chains)
-   [Procedimientos de enlace](#hook-procedures)
-   [Tipos de enlace](#hook-types)
    -   [QU \_ CALLWNDPROC y qu \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [QU \_ CBT](#wh_cbt)
    -   [QU \_ depuración](#wh_debug)
    -   [QU \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [\_qume](#wh_getmessage)
    -   [QU \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [QU \_ JOURNALRECORD](#wh_journalrecord)
    -   [QU \_ Keyboard \_ ll](#wh_keyboard_ll)
    -   [QU \_ Keyboard](#wh_keyboard)
    -   [QU \_ mouse \_ ll](#wh_mouse_ll)
    -   [QU \_ mouse](#wh_mouse)
    -   [QU \_ MSGFILTER y qu \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [QU \_ Shell](#wh_shell)

## <a name="hook-chains"></a>Cadenas de enlace

El sistema admite muchos tipos diferentes de enlaces; cada tipo proporciona acceso a un aspecto diferente del mecanismo de control de mensajes. Por ejemplo, una aplicación puede usar el [enlace \_ del mouse](#wh_mouse) para supervisar el tráfico de mensajes de mouse.

El sistema mantiene una cadena de enlace independiente para cada tipo de enlace. Una *cadena de enlaces* es una lista de punteros a funciones de devolución de llamada especiales definidas por la aplicación llamadas *procedimientos de enlace*. Cuando se produce un mensaje que está asociado a un tipo determinado de enlace, el sistema pasa el mensaje a cada uno de los procedimientos de enlace a los que se hace referencia en la cadena de enlaces, uno después de otro. La acción que puede realizar un procedimiento de enlace depende del tipo de enlace implicado. Los procedimientos de enlace para algunos tipos de enlaces solo pueden supervisar mensajes; otros usuarios pueden modificar los mensajes o detener su progreso a través de la cadena, evitando que lleguen al siguiente procedimiento de enlace o a la ventana de destino.

## <a name="hook-procedures"></a>Procedimientos de enlace

Para beneficiarse de un tipo determinado de enlace, el desarrollador proporciona un procedimiento de enlace y usa la función [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) para instalarlo en la cadena asociada con el enlace. Un procedimiento de enlace debe tener la siguiente sintaxis:

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

*HookProc* es un marcador de posición para un nombre definido por la aplicación.

El parámetro *nCode* es un código de enlace que el procedimiento de enlace usa para determinar la acción que se va a realizar. El valor del código de enlace depende del tipo del enlace; cada tipo tiene su propio conjunto característico de códigos de enlace. Los valores de los parámetros *wParam* e *lParam* dependen del código de enlace, pero suelen contener información sobre un mensaje que se envió o se publicó.

La función [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) siempre instala un procedimiento de enlace al principio de una cadena de enlaces. Cuando se produce un evento supervisado por un tipo de enlace determinado, el sistema llama al procedimiento situado al principio de la cadena de enlace asociada al enlace. Cada procedimiento de enlace de la cadena determina si se debe pasar el evento al procedimiento siguiente. Un procedimiento de enlace pasa un evento al procedimiento siguiente mediante una llamada a la función [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) .

Tenga en cuenta que los procedimientos de enlace para algunos tipos de enlaces solo pueden supervisar mensajes. el sistema pasa los mensajes a cada procedimiento de enlace, con independencia de si un procedimiento determinado llama a [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).

Un *enlace global* supervisa los mensajes de todos los subprocesos del mismo escritorio que el subproceso que realiza la llamada. Un *enlace específico del subproceso* solo supervisa los mensajes de un subproceso individual. Se puede llamar a un procedimiento de enlace global en el contexto de cualquier aplicación en el mismo escritorio que el subproceso que realiza la llamada, por lo que el procedimiento debe encontrarse en un módulo DLL independiente. Solo se llama a un procedimiento de enlace específico del subproceso en el contexto del subproceso asociado. Si una aplicación instala un procedimiento de enlace para uno de sus propios subprocesos, el procedimiento de enlace puede estar en el mismo módulo que el resto del código de la aplicación o en un archivo DLL. Si la aplicación instala un procedimiento de enlace para un subproceso de una aplicación diferente, el procedimiento debe estar en un archivo DLL. Para obtener más información, consulte [bibliotecas de vínculos dinámicos](../dlls/dynamic-link-libraries.md).

> [!Note]  
> Los enlaces globales solo se deben usar con fines de depuración; de lo contrario, debe evitarlos. Los enlaces globales perjudican el rendimiento del sistema y causan conflictos con otras aplicaciones que implementan el mismo tipo de enlace global.

 

## <a name="hook-types"></a>Tipos de enlace

Cada tipo de enlace permite a una aplicación supervisar un aspecto diferente del mecanismo de control de mensajes del sistema. En las secciones siguientes se describen los enlaces disponibles.

-   [QU \_ CALLWNDPROC y qu \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [QU \_ CBT](#wh_cbt)
-   [QU \_ depuración](#wh_debug)
-   [QU \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [\_qume](#wh_getmessage)
-   [QU \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [QU \_ JOURNALRECORD](#wh_journalrecord)
-   [QU \_ Keyboard \_ ll](#wh_keyboard_ll)
-   [QU \_ Keyboard](#wh_keyboard)
-   [QU \_ mouse \_ ll](#wh_mouse_ll)
-   [QU \_ mouse](#wh_mouse)
-   [QU \_ MSGFILTER y qu \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [QU \_ Shell](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>QU \_ CALLWNDPROC y qu \_ CALLWNDPROCRET

Los enlaces **qu \_ CALLWNDPROC** y **qu \_ CALLWNDPROCRET** permiten supervisar los mensajes enviados a los procedimientos de ventana. El sistema llama a un procedimiento de enlace de **qu \_ CALLWNDPROC** antes de pasar el mensaje al procedimiento de ventana receptor y llama al procedimiento del enlace **qu \_ CALLWNDPROCRET** después de que el procedimiento de ventana haya procesado el mensaje.

El enlace **qu \_ CALLWNDPROCRET** pasa un puntero a una estructura [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) al procedimiento de enlace. La estructura contiene el valor devuelto por el procedimiento de ventana que procesó el mensaje, así como los parámetros de mensaje asociados al mensaje. La subclase de la ventana no funciona para los mensajes que se establecen entre los procesos.

Para obtener más información, vea las funciones de devolución de llamada [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) y [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) .

### <a name="wh_cbt"></a>QU \_ CBT

El sistema llama a un procedimiento de enlace de **qude \_** antes de activar, crear, destruir, minimizar, maximizar, mover o cambiar el tamaño de una ventana; antes de completar un comando del sistema; antes de quitar un evento del mouse o del teclado de la cola de mensajes del sistema, antes de establecer el foco de entrada o antes de sincronizar con la cola de mensajes del sistema. El valor que devuelve el procedimiento de enlace determina si el sistema permite o impide una de estas operaciones. El enlace de **\_ CBT** está diseñado principalmente para aplicaciones de aprendizaje basado en equipos (CBT).

Para obtener más información, vea la función de devolución de llamada [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) .

Para obtener información, consulte [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>QU \_ depuración

El sistema llama a un procedimiento de enlace de **\_ depuración de qu** antes de llamar a los procedimientos de enlace asociados a cualquier otro enlace del sistema. Puede usar este enlace para determinar si se permite que el sistema llame a los procedimientos de enlace asociados a otros tipos de enlaces.

Para obtener más información, vea la función de devolución de llamada [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) .

### <a name="wh_foregroundidle"></a>QU \_ FOREGROUNDIDLE

El enlace **qu \_ FOREGROUNDIDLE** le permite realizar tareas de prioridad baja en momentos en los que el subproceso en primer plano está inactivo. El sistema llama a un procedimiento de enlace **qu \_ FOREGROUNDIDLE** cuando el subproceso en primer plano de la aplicación está a punto de convertirse en inactivo.

Para obtener más información, vea la función de devolución de llamada [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) .

### <a name="wh_getmessage"></a>\_qume

El enlace **qu \_ GETMESSAGE** permite a una aplicación supervisar los mensajes que se van a devolver mediante la función [**GETMESSAGE**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Puede usar el enlace **qu \_ GETMESSAGE** para supervisar la entrada del mouse y del teclado, y otros mensajes enviados a la cola de mensajes.

Para obtener más información, vea la función de devolución de llamada [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) .

### <a name="wh_journalplayback"></a>QU \_ JOURNALPLAYBACK

El enlace **qu \_ JOURNALPLAYBACK** permite a una aplicación insertar mensajes en la cola de mensajes del sistema. Puede usar este enlace para reproducir una serie de eventos de mouse y teclado registrados anteriormente mediante el uso de [qu \_ JOURNALRECORD](#wh_journalrecord). La entrada normal del mouse y del teclado está deshabilitada, siempre y cuando esté instalado el enlace **qu \_ JOURNALPLAYBACK** . Un enlace **qu \_ JOURNALPLAYBACK** es un enlace global; no se puede usar como un enlace específico del subproceso.

El enlace **qu \_ JOURNALPLAYBACK** devuelve un valor de tiempo de espera. Este valor indica al sistema el número de milisegundos que hay que esperar antes de procesar el mensaje actual desde el enlace de reproducción. Esto permite al enlace controlar el tiempo de los eventos que se reproduce.

Para obtener más información, vea la función de devolución de llamada [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .

### <a name="wh_journalrecord"></a>QU \_ JOURNALRECORD

El enlace **qu \_ JOURNALRECORD** le permite supervisar y grabar eventos de entrada. Normalmente, este enlace se usa para registrar una secuencia de eventos del mouse y del teclado que se reproducirán más tarde mediante el uso de [qu \_ JOURNALPLAYBACK](#wh_journalplayback). El enlace **qu \_ JOURNALRECORD** es un enlace global; no se puede usar como un enlace específico del subproceso.

Para obtener más información, vea la función de devolución de llamada [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) .

### <a name="wh_keyboard_ll"></a>QU \_ Keyboard \_ ll

El enlace **qu \_ Keyboard \_ ll** permite supervisar los eventos de entrada de teclado que se van a publicar en una cola de entrada de subprocesos.

Para obtener más información, vea la función de devolución de llamada [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) .

### <a name="wh_keyboard"></a>QU \_ Keyboard

El enlace de **\_ teclado qu** permite a una aplicación supervisar el tráfico de mensajes para los mensajes [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) que va a ser devuelto por la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Puede usar el enlace **de \_ teclado qu** para supervisar las entradas de teclado enviadas a una cola de mensajes.

Para obtener más información, vea la función de devolución de llamada [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) .

### <a name="wh_mouse_ll"></a>QU \_ mouse \_ ll

El enlace **qu \_ mouse \_ ll** le permite supervisar los eventos de entrada del mouse que se van a publicar en una cola de entrada del subproceso.

Para obtener más información, vea la función de devolución de llamada [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) .

### <a name="wh_mouse"></a>QU \_ mouse

El **enganche \_ del mouse** permite supervisar los mensajes de mouse que se van a devolver mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Puede usar el enlace **\_ del mouse** para supervisar la entrada del mouse enviada a una cola de mensajes.

Para obtener más información, vea la función de devolución de llamada [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) .

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>QU \_ MSGFILTER y qu \_ SYSMSGFILTER

Los enlaces **qu \_ MSGFILTER** y **qu \_ SYSMSGFILTER** permiten supervisar mensajes que van a ser procesados por un menú, una barra de desplazamiento, un cuadro de mensaje o un cuadro de diálogo, y detectar cuándo se va a activar una ventana diferente como resultado de presionar la combinación de teclas Alt + Tab o Alt + Esc. El enlace **qu \_ MSGFILTER** solo puede supervisar los mensajes pasados a un menú, una barra de desplazamiento, un cuadro de mensaje o un cuadro de diálogo creado por la aplicación que instaló el procedimiento de enlace. El enlace **qu \_ SYSMSGFILTER** supervisa estos mensajes para todas las aplicaciones.

Los enlaces **qu \_ MSGFILTER** y **qu \_ SYSMSGFILTER** permiten realizar el filtrado de mensajes durante los bucles modales equivalentes al filtrado realizado en el bucle de mensajes principal. Por ejemplo, una aplicación suele examinar un nuevo mensaje en el bucle principal entre el momento en que recupera el mensaje de la cola y el tiempo que envía el mensaje, lo que realiza un procesamiento especial según corresponda. Sin embargo, durante un bucle modal, el sistema recupera y envía mensajes sin permitir a una aplicación la posibilidad de filtrar los mensajes en su bucle de mensajes principal. Si una aplicación instala un procedimiento de enlace **qu \_ MSGFILTER** o **qu \_ SYSMSGFILTER** , el sistema llama al procedimiento durante el bucle modal.

Una aplicación puede llamar al enlace **qu \_ MSGFILTER** directamente llamando a la función [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) . Mediante esta función, la aplicación puede usar el mismo código para filtrar los mensajes durante los bucles modales que se usan en el bucle de mensajes principal. Para ello, encapsula las operaciones de filtrado en un procedimiento de enlace de **\_ MSGFILTER** y llama a **CallMsgFilter** entre las llamadas a las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

El último argumento de [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) se pasa simplemente al procedimiento de enlace; puede escribir cualquier valor. El procedimiento de enlace, definiendo una constante como **MSGF \_ MAINLOOP**, puede usar este valor para determinar dónde se llamó al procedimiento.

Para obtener más información, vea las funciones de devolución de llamada [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) y [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) .

### <a name="wh_shell"></a>QU \_ Shell

Una aplicación de Shell puede usar el enlace del **\_ Shell de qu** para recibir notificaciones importantes. El sistema llama a un procedimiento de enlace de **\_ Shell de qu** cuando la aplicación de Shell está a punto de activarse y cuando se crea o se destruye una ventana de nivel superior.

Tenga en cuenta que las aplicaciones de Shell personalizadas no reciben los mensajes del **\_ Shell** . Por lo tanto, cualquier aplicación que se registre como el shell predeterminado debe llamar a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) antes de que esta pueda recibir los mensajes **de \_ Shell** . Se debe llamar a esta función con **SPI \_ SETMINIMIZEDMETRICS** y una estructura [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) . Establezca el miembro **iArrange** de esta estructura en **ARW \_ Hide**.

Para obtener más información, vea la función de devolución de llamada [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) .

 

 
