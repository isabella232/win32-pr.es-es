---
description: Obtenga información sobre cómo evitar que se Windows aplicaciones para Windows 7 y Windows Server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prevención de bloqueos en aplicaciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a2d8fac95039f20c8c684c50138933c54750c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474549"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prevención de bloqueos en aplicaciones de Windows

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="description"></a>Descripción

**Hangs - User Perspective**

A los usuarios les gusta las aplicaciones con capacidad de respuesta. Al hacer clic en un menú, quieren que la aplicación reaccione al instante, incluso si actualmente imprime su trabajo. Cuando guarda un documento largo en su procesador de textos favorito, quiere seguir escribiendo mientras el disco sigue girando. Los usuarios se impacientan bastante rápidamente cuando la aplicación no reacciona a tiempo a su entrada.

Un programador podría reconocer muchas razones legítimas para que una aplicación no responda al instante a la entrada del usuario. Es posible que la aplicación esté ocupada recalculando algunos datos o simplemente esperando a que se complete su E/S de disco. Sin embargo, a partir de la investigación de los usuarios, sabemos que los usuarios se frustran y se frustran después de un par de segundos de falta de respuesta. Después de 5 segundos, intentarán finalizar una aplicación que está sin cerrar. Junto a los bloqueos, los bloqueos de aplicaciones son la fuente más común de interrupción del usuario al trabajar con aplicaciones Win32.

Hay muchas causas principales diferentes para los problemas de aplicación y no todas se manifiestan en una interfaz de usuario que no responde. Sin embargo, una interfaz de usuario que no responde es una de las experiencias de hang más comunes y este escenario recibe actualmente la mayor compatibilidad del sistema operativo tanto para la detección como para la recuperación. Windows automáticamente detecta, recopila información de depuración y, opcionalmente, finaliza o reinicia las aplicaciones que se han quedados. De lo contrario, es posible que el usuario tenga que reiniciar la máquina para recuperar una aplicación que se ha quebrado.

**Hangs - Operating System Perspective**

Cuando una aplicación (o con más precisión, un subproceso) crea una ventana en el escritorio, entra en un contrato implícito con el Administrador de ventanas de escritorio (DWM) para procesar los mensajes de ventana de forma oportuna. DwM envía mensajes (entrada de teclado y mouse y mensajes de otras ventanas, así como de sí mismo) en la cola de mensajes específica del subproceso. El subproceso recupera y envía esos mensajes a través de su cola de mensajes. Si el subproceso no da servicio a la cola mediante una llamada a GetMessage(), los mensajes no se procesan y la ventana se bloqueo: no puede volver a dibujar ni puede aceptar la entrada del usuario. El sistema operativo detecta este estado adjuntando un temporizador a los mensajes pendientes en la cola de mensajes. Si no se ha recuperado un mensaje en 5 segundos, el DWM declara la ventana que se va a cargar. Puede consultar este estado de ventana determinado a través de la API IsHungAppWindow().

La detección es solo el primer paso. En este momento, el usuario todavía no puede terminar la aplicación; al hacer clic en el botón X (Cerrar), se produciría un mensaje WM CLOSE, que se atascaría en la cola de mensajes como cualquier \_ otro mensaje. El Administrador de ventanas de escritorio ayuda a ocultar sin problemas y, a continuación, reemplazar la ventana con una copia "fantasma" que muestra un mapa de bits del área de cliente anterior de la ventana original (y agregar "No respondiendo" a la barra de título). Siempre y cuando el subproceso de la ventana original no recupere mensajes, dwm administra ambas ventanas simultáneamente, pero permite al usuario interactuar solo con la copia fantasma. Con esta ventana fantasma, el usuario solo puede mover, minimizar y, lo que es más importante, cerrar la aplicación que no responde, pero no cambiar su estado interno.

La experiencia fantasma completa tiene este aspecto:

![Captura de pantalla que muestra el cuadro de Bloc de notas "no responde".](images/preventinghangs-ghostwindow.gif)

El Administrador de ventanas de escritorio hace una última cosa; se integra con Informe de errores de Windows, lo que permite al usuario no solo cerrar y reiniciar opcionalmente la aplicación, sino también enviar datos de depuración valiosos a Microsoft. Puede obtener estos datos de desahora para sus propias aplicaciones si se sucriba al sitio web de Winqual.

Windows 7 agregó una nueva característica a esta experiencia. El sistema operativo analiza la aplicación bloqueado y, en determinadas circunstancias, ofrece al usuario la opción de cancelar una operación de bloqueo y hacer que la aplicación responda de nuevo. La implementación actual admite la cancelación de llamadas socket de bloqueo; En futuras versiones, se cancelarán más operaciones.

Para integrar la aplicación con la experiencia de recuperación de hang y sacar el máximo partido a los datos disponibles, siga estos pasos:

-   Asegúrese de que la aplicación se registra para el reinicio y la recuperación, lo que hace que el usuario no se desasocie lo más posible. Una aplicación registrada correctamente puede reiniciarse automáticamente con la mayoría de los datos no guardados intactos. Esto funciona para bloqueos y bloqueos de la aplicación.
-   Obtenga información de frecuencia, así como datos de depuración de las aplicaciones que se bloquean y bloquean desde el sitio web de Winqual. Puede usar esta información incluso durante la versión beta para mejorar el código. Vea "Introducing Informe de errores de Windows" (Introducción a Informe de errores de Windows) para obtener una breve introducción.
-   Puede deshabilitar la característica de fantasmas en la aplicación mediante una llamada a DisableProcessWindowsGhosting (). Sin embargo, esto evita que el usuario medio cierre y reinicie una aplicación que se ha cerrado y, a menudo, termina en un reinicio.

**Hangs - Developer Perspective**

El sistema operativo define un error de aplicación como un subproceso de interfaz de usuario que no ha procesado los mensajes durante al menos 5 segundos. Los errores obvios provocan algunos bloqueos, por ejemplo, un subproceso que espera un evento que nunca se señala y dos subprocesos que mantienen un bloqueo e intentan adquirir los demás. Puede corregir esos errores sin demasiado esfuerzo. Sin embargo, muchos de los problemas no están tan claros. Sí, el subproceso de interfaz de usuario no está recuperando mensajes, pero está igualmente ocupado realizando otro trabajo "importante" y finalmente volverá al procesamiento de mensajes.

Sin embargo, el usuario lo percibe como un error. El diseño debe coincidir con las expectativas del usuario. Si el diseño de la aplicación conduce a una aplicación que no responde, el diseño tendrá que cambiar. Por último, y esto es importante, la falta de respuesta no se puede solucionar como un error de código. requiere trabajo inicial durante la fase de diseño. Intentar adaptar la base de código existente de una aplicación para que la interfaz de usuario sea más dinámica suele ser demasiado costosa. Las siguientes directrices de diseño pueden ser de ayuda.

-   Convertir la capacidad de respuesta de la interfaz de usuario en un requisito de nivel superior; el usuario siempre debe tener el control de la aplicación
-   Asegúrese de que los usuarios pueden cancelar operaciones que tardan más de un segundo en completarse o que las operaciones pueden completarse en segundo plano; Proporcionar la interfaz de usuario de progreso adecuada si es necesario

![Captura de pantalla que muestra el cuadro de diálogo "Copiar elementos".](images/preventinghangs-progressbar.gif)

-   Poner en cola operaciones de ejecución o bloqueo como tareas en segundo plano (esto requiere un mecanismo de mensajería bien pensado para informar al subproceso de la interfaz de usuario cuando se ha completado el trabajo).
-   Mantener el código de los subprocesos de interfaz de usuario simple; quitar tantas llamadas API de bloqueo como sea posible
-   Mostrar ventanas y cuadros de diálogo solo cuando estén listos y totalmente operativos. Si el cuadro de diálogo necesita mostrar información que consume demasiados recursos para calcularla, primero debe mostrar información genérica y actualizarla sobre la marcha cuando haya más datos disponibles. Un buen ejemplo es el cuadro de diálogo de propiedades de carpeta Windows Explorer. Debe mostrar el tamaño total de la carpeta, información que no está disponible fácilmente en el sistema de archivos. El cuadro de diálogo se muestra inmediatamente y el campo "tamaño" se actualiza desde un subproceso de trabajo:

![Captura de pantalla que muestra la página "General" de Windows propiedades con el texto "Tamaño", "Tamaño en disco" y "Contiene" en círculo.](images/preventinghangs-updatingdialog.gif)

Desafortunadamente, no hay ninguna manera sencilla de diseñar y escribir una aplicación con capacidad de respuesta. Windows proporciona un marco asincrónico simple que permita una programación sencilla de operaciones de bloqueo o de ejecución larga. En las secciones siguientes se presentan algunos de los procedimientos recomendados para evitar los ahorcaciones y se resaltan algunos de los problemas comunes.

## <a name="best-practices"></a>Prácticas recomendadas

**Mantener el subproceso de interfaz de usuario simple**

La responsabilidad principal del subproceso de interfaz de usuario es recuperar y enviar mensajes. Cualquier otro tipo de trabajo presenta el riesgo de que se colócar las ventanas propiedad de este subproceso.

**Hacer:**

-   Mover algoritmos que consumen muchos recursos o sin enlazar que resulten en operaciones de larga duración a subprocesos de trabajo
-   Identifique tantas llamadas de función de bloqueo como sea posible e intente moverlas a subprocesos de trabajo. cualquier función que llame a otro archivo DLL debería ser sospechosa
-   Realice un esfuerzo adicional para quitar todas las llamadas API de E/S y redes de archivos del subproceso de trabajo. Estas funciones pueden bloquearse durante muchos segundos si no son minutos. Si necesita realizar cualquier tipo de E/S en el subproceso de la interfaz de usuario, considere la posibilidad de usar E/S asincrónica.
-   Tenga en cuenta que el subproceso de interfaz de usuario también está dando servicio a todos los servidores COM de un solo subproceso (STA) hospedados por el proceso; Si realiza una llamada de bloqueo, estos servidores COM no responderán hasta que vuelva a dar servicio a la cola de mensajes.

**No:**

-   Espere en cualquier objeto de kernel (como Event o Mutex) durante más de un período de tiempo muy corto. Si tiene que esperar, considere la posibilidad de usar MsgWaitForMultipleObjects(), que se desbloqueará cuando llegue un mensaje nuevo.
-   Comparta la cola de mensajes de ventana de un subproceso con otro subproceso mediante la función AttachThreadInput(). No solo es muy difícil sincronizar correctamente el acceso a la cola, sino que también puede impedir que el sistema operativo Windows detecte correctamente una ventana que se ha quedado.
-   Use TerminateThread() en cualquiera de los subprocesos de trabajo. La terminación de un subproceso de esta manera no le permitirá liberar bloqueos ni señalar eventos y puede dar lugar fácilmente a objetos de sincronización huérfanos
-   Llame a cualquier código "desconocido" desde el subproceso de la interfaz de usuario. Esto es especialmente cierto si la aplicación tiene un modelo de extensibilidad; no hay ninguna garantía de que el código de terceros siga las directrices de capacidad de respuesta
-   Realizar cualquier tipo de llamada de difusión de bloqueo; SendMessage (HWND BROADCAST) le coloca al día de todas las aplicaciones mal escritas que se están \_ ejecutando actualmente

**Implementar patrones asincrónicos**

La eliminación de operaciones de ejecución larga o bloqueo del subproceso de interfaz de usuario requiere la implementación de un marco asincrónico que permita descargar esas operaciones en subprocesos de trabajo.

**Hacer:**

-   Use las API de mensajes de ventana asincrónicas en el subproceso de interfaz de usuario, especialmente reemplazando SendMessage por uno de sus elementos del mismo nivel sin bloqueo: PostMessage, SendNotifyMessage o SendMessageCallback.
-   Use subprocesos en segundo plano para ejecutar tareas de ejecución larga o de bloqueo. Uso de la nueva API del grupo de subprocesos para implementar los subprocesos de trabajo
-   Proporcionar compatibilidad con la cancelación para tareas en segundo plano de ejecución larga. Para bloquear operaciones de E/S, use la cancelación de E/S, pero solo como último recurso; no es fácil cancelar la operación "right"
-   Implementación de un diseño asincrónico para código administrado mediante el patrón IAsyncResult o mediante eventos

**Usar bloqueos de forma inteligente**

La aplicación o dll necesita bloqueos para sincronizar el acceso a sus estructuras de datos internas. El uso de varios bloqueos aumenta el paralelismo y hace que la aplicación tenga más capacidad de respuesta. Sin embargo, el uso de varios bloqueos también aumenta la posibilidad de adquirir esos bloqueos en distintos pedidos y hacer que los subprocesos entren en interbloqueo. Si dos subprocesos mantienen un bloqueo y, a continuación, intentan adquirir el bloqueo del otro subproceso, sus operaciones formarán una espera circular que bloquea cualquier progreso hacia delante de estos subprocesos. Puede evitar este interbloqueo solo asegurándose de que todos los subprocesos de la aplicación siempre adquieren todos los bloqueos en el mismo orden. Sin embargo, no siempre es fácil adquirir bloqueos en el orden "correcto". Los componentes de software se pueden componer, pero las adquisiciones de bloqueo no. Si el código llama a algún otro componente, los bloqueos de ese componente ahora forman parte del orden de bloqueo implícito, incluso si no tiene visibilidad sobre esos bloqueos.

Las cosas son aún más difíciles porque las operaciones de bloqueo incluyen muchas más funciones que las habituales para secciones críticas, exclusiones mutuas y otros bloqueos tradicionales. Cualquier llamada de bloqueo que cruza los límites del subproceso tiene propiedades de sincronización que pueden dar lugar a un interbloqueo. El subproceso que realiza la llamada realiza una operación con semántica "acquire" y no se puede desbloquear hasta que el subproceso de destino "libere" esa llamada. Algunas funciones User32 (por ejemplo, SendMessage), así como muchas llamadas COM de bloqueo se clasifican en esta categoría.

Peor aún, el sistema operativo tiene su propio bloqueo interno específico del proceso que a veces se mantiene mientras se ejecuta el código. Este bloqueo se adquiere cuando se cargan archivos DLL en el proceso y, por tanto, se denomina "bloqueo del cargador". La función DllMain siempre se ejecuta bajo el bloqueo del cargador; Si adquiere algún bloqueo en DllMain (y no debería), debe hacer que el bloqueo del cargador sea parte del orden de bloqueo. Llamar a determinadas API de Win32 también podría adquirir el bloqueo del cargador en su nombre: funciones como LoadLibraryEx, GetModuleHandle y, especialmente, CoCreateInstance.

Para unir todo esto, vea el código de ejemplo siguiente. Esta función adquiere varios objetos de sincronización y define implícitamente un orden de bloqueo, algo que no es necesariamente obvio en la inspección cursory. En la entrada de función, el código adquiere una sección crítica y no la libera hasta que se cierra la función, lo que lo convierte en el nodo superior de la jerarquía de bloqueos. A continuación, el código llama a la función LoadIcon() de Win32, que, en primer lugar, podría llamar al cargador de sistema operativo para cargar este archivo binario. Esta operación adquiriría el bloqueo del cargador, que ahora también forma parte de esta jerarquía de bloqueos (asegúrese de que la función DllMain no adquiere el bloqueo \_ g cs). A continuación, el código llama a SendMessage(), una operación de bloqueo entre subprocesos, que no se devolverá a menos que el subproceso de la interfaz de usuario responda. De nuevo, asegúrese de que el subproceso de interfaz de usuario nunca adquiere g \_ cs.

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

Si observamos este código, parece claro que hemos hecho implícitamente g cs el bloqueo de nivel superior en nuestra jerarquía de bloqueos, incluso si solo se quisiera sincronizar el acceso a las variables miembro \_ de clase.

**Hacer:**

-   Diseñe una jerarquía de bloqueos y obedézcala. Agregue todos los bloqueos necesarios. Hay muchas más primitivas de sincronización que solo Mutex y CriticalSections. todos ellos deben incluirse. Incluya el bloqueo del cargador en la jerarquía si se toman bloqueos en DllMain()
-   Acepte el protocolo de bloqueo con sus dependencias. Cualquier código que llame a la aplicación o que pueda llamar a la aplicación debe compartir la misma jerarquía de bloqueos
-   Bloquear estructuras de datos no funciones. Aleja las adquisiciones de bloqueo de los puntos de entrada de la función y protege solo el acceso a los datos con bloqueos. Si hay menos código bajo un bloqueo, hay menos posibilidades de interbloqueos.
-   Analice las adquisiciones y versiones de bloqueo en el código de control de errores. A menudo, la jerarquía de bloqueos si se olvida al intentar recuperarse de una condición de error
-   Reemplace los bloqueos anidados por contadores de referencia: no pueden interbloqueo. Los elementos bloqueados individualmente en listas y tablas son buenos candidatos
-   Tenga cuidado al esperar un identificador de subproceso desde un archivo DLL. Supongamos siempre que se puede llamar al código bajo el bloqueo del cargador. Es mejor hacer un recuento de referencias de los recursos y dejar que el subproceso de trabajo realice su propia limpieza (y, a continuación, use FreeLibraryAndExitThread para finalizar correctamente).
-   Use wait chain traversal API si desea diagnosticar sus propios interbloqueos

**No:**

-   Haga algo que no sea un trabajo de inicialización muy sencillo en la función DllMain(). Consulte DllMain Callback Function (Función de devolución de llamada de DllMain) para obtener más detalles. En especial, no llame a LoadLibraryEx o CoCreateInstance.
-   Escriba sus propias primitivas de bloqueo. El código de sincronización personalizado puede introducir fácilmente errores sutiles en la base de código. En su lugar, use la selección enriquecte de objetos de sincronización del sistema operativo.
-   Realice cualquier trabajo en los constructores y destructores de variables globales; se ejecutan bajo el bloqueo del cargador.

**Tenga cuidado con las excepciones**

Las excepciones permiten la separación del flujo de programa normal y el control de errores. Debido a esta separación, puede ser difícil conocer el estado preciso del programa antes de la excepción y el controlador de excepciones podría perder los pasos fundamentales para restaurar un estado válido. Esto es especialmente cierto para las adquisiciones de bloqueos que deben liberarse en el controlador para evitar futuros interbloqueos.

El código de ejemplo siguiente muestra este problema. En ocasiones, el acceso sin enlazar a la variable "buffer" dará lugar a una infracción de acceso (AV). El controlador de excepciones nativo detecta este AV, pero no tiene ninguna manera fácil de determinar si la sección crítica ya se adquirió en el momento de la excepción (el av podría haber tenido lugar incluso en algún lugar del código EnterCriticalSection).

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**Hacer:**

-   Quite \_ \_ try/ \_ \_ excepto siempre que sea posible; no use SetUnhandledExceptionFilter
-   Ajuste los bloqueos en plantillas \_ de tipo ptr automáticas personalizadas si usa excepciones de C++. El bloqueo debe liberarse en el destructor. En el caso de las excepciones nativas, libere los bloqueos en la \_ \_ instrucción finally.
-   Tenga cuidado con el código que se ejecuta en un controlador de excepciones nativo; es posible que la excepción haya filtrado muchos bloqueos, por lo que el controlador no debe adquirir ninguno.

**No:**

-   Controle las excepciones nativas si las API de Win32 no las necesitan o las requieren. Si usa controladores de excepciones nativos para la generación de informes o la recuperación de datos después de errores catastróficos, considere la posibilidad de usar el mecanismo de sistema operativo predeterminado Informe de errores de Windows en su lugar.
-   Usar excepciones de C++ con cualquier tipo de código de interfaz de usuario (user32); Una excepción producida en una devolución de llamada recorrerá las capas de código C proporcionadas por el sistema operativo. Ese código no conoce la semántica de la inscripción de C++

## <a name="links-to-resources"></a>Vínculos a recursos

-   [Informe de errores de Windows](../wer/windows-error-reporting.md)
-   [Diseño asincrónico](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [E/S asincrónica](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput (Función)**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**auto \_ ptr (clase)**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting (Función)**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Función de devolución de llamada de DllMain**](../dlls/dllmain.md)
-   [Eventos](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage (Función)**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Cancelación de E/S](../fileio/canceling-pending-i-o-operations.md)
-   [**Función IsHungAppWindow**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Cola de mensajes](../winmsg/using-messages-and-message-queues.md)
-   [**Función MsgWaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nueva API de grupo de subprocesos](../procthread/thread-pool-api.md)
-   [**Función PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Reinicio y recuperación](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback (Función)**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage (Función)**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Objetos de sincronización](../sync/about-synchronization.md)
-   [**TerminateThread (Función)**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Informe de errores de Windows](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
