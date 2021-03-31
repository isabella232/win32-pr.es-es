---
description: Obtenga información acerca de cómo evitar bloqueos en aplicaciones Windows para plataformas Windows 7 y Windows Server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prevención de bloqueos en aplicaciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a2d8fac95039f20c8c684c50138933c54750c3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104083526"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prevención de bloqueos en aplicaciones de Windows

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="description"></a>Descripción

**Bloqueos: perspectiva del usuario**

Usuarios como aplicaciones con capacidad de respuesta. Cuando hacen clic en un menú, quieren que la aplicación reaccione al instante, incluso si está imprimiendo su trabajo en ese momento. Cuando guardan un documento largo en su procesador de textos favorito, quieren seguir escribiendo mientras el disco sigue girando. Los usuarios reciben un poco más rápido cuando la aplicación no reacciona de manera oportuna a su entrada.

Un programador podría reconocer muchas razones legítimas para que una aplicación no responda instantáneamente a los datos proporcionados por el usuario. Es posible que la aplicación esté ocupada recalculando algunos datos o simplemente esperando a que se complete la e/s de disco. Sin embargo, a partir de la investigación del usuario, sabemos que los usuarios se sienten molestados y frustrados después de un par de segundos de falta de respuesta. Después de 5 segundos, intentarán terminar una aplicación bloqueada. Junto a bloqueos, la aplicación deja de responder a la causa más común de la interrupción del usuario cuando se trabaja con aplicaciones Win32.

Hay muchas causas raíz diferentes para los bloqueos de la aplicación y no todas ellas se manifiestan en una interfaz de usuario que no responde. Sin embargo, una interfaz de usuario que no responde es una de las experiencias más comunes de bloqueo, y este escenario recibe actualmente la mayor parte de la compatibilidad con el sistema operativo para la detección y la recuperación. Windows detecta automáticamente, recopila información de depuración y, opcionalmente, finaliza o reinicia las aplicaciones bloqueadas. De lo contrario, es posible que el usuario tenga que reiniciar el equipo para recuperar una aplicación bloqueada.

**Se bloquea: perspectiva del sistema operativo**

Cuando una aplicación (o más concretamente, un subproceso) crea una ventana en el escritorio, entra en un contrato implícito con el Administrador de ventanas de escritorio (DWM) para procesar los mensajes de la ventana de manera oportuna. DWM envía mensajes (entrada de teclado/mouse y mensajes desde otras ventanas, así como a sí mismos) en la cola de mensajes específica del subproceso. El subproceso recupera y envía los mensajes a través de su cola de mensajes. Si el subproceso no presta servicio a la cola mediante una llamada a GetMessage (), los mensajes no se procesan y la ventana se bloquea: no puede volver a dibujar ni aceptar la entrada del usuario. El sistema operativo detecta este estado adjuntando un temporizador a los mensajes pendientes en la cola de mensajes. Si un mensaje no se ha recuperado en un plazo de 5 segundos, el DWM declara que la ventana está bloqueada. Puede consultar este estado de ventana concreto a través de la API IsHungAppWindow ().

La detección es solo el primer paso. En este momento, el usuario todavía no puede incluso terminar la aplicación: al hacer clic en el botón X (cerrar) se produciría un \_ mensaje de cierre de WM, que se bloquearía en la cola de mensajes como cualquier otro mensaje. El Administrador de ventanas de escritorio ayuda a ocultar sin problemas y, a continuación, reemplazar la ventana de bloqueo con una copia "fantasma" que muestra un mapa de bits del área cliente anterior de la ventana original (y la adición de "no responde" a la barra de título). Siempre que el subproceso de la ventana original no recupere los mensajes, DWM administra ambas ventanas simultáneamente, pero permite que el usuario interactúe solo con la copia fantasma. Con esta ventana fantasma, el usuario solo puede moverse, minimizar y, lo que es más importante, cerrar la aplicación que no responde, pero no cambiar su estado interno.

Toda la experiencia de Ghost tiene el siguiente aspecto:

![Captura de pantalla que muestra el cuadro de diálogo "el Bloc de notas no responde".](images/preventinghangs-ghostwindow.gif)

El Administrador de ventanas de escritorio hace lo último; se integra con Informe de errores de Windows, lo que permite que el usuario no solo cierre y, opcionalmente, reinicie la aplicación, sino que también envíe datos de depuración valiosos a Microsoft. Puede obtener estos datos de bloqueo para sus propias aplicaciones. para ello, Regístrese en el sitio web de WinQual.

Windows 7 ha agregado una nueva característica a esta experiencia. El sistema operativo analiza la aplicación bloqueada y, en determinadas circunstancias, proporciona al usuario la opción de cancelar una operación de bloqueo y hacer que la aplicación responda de nuevo. La implementación actual admite la cancelación de llamadas de socket de bloqueo. en futuras versiones se podrán cancelar más operaciones por el usuario.

Para integrar la aplicación con la experiencia de recuperación de bloqueo y sacar el máximo partido de los datos disponibles, siga estos pasos:

-   Asegúrese de que la aplicación se registra para el reinicio y la recuperación, lo que permite que el usuario se bloquee de forma tan sencilla como sea posible. Una aplicación correctamente registrada puede reiniciarse automáticamente con la mayoría de los datos no guardados intactos. Esto funciona para los bloqueos y bloqueos de la aplicación.
-   Obtenga información sobre la frecuencia y depure datos de las aplicaciones bloqueadas y bloqueadas desde el sitio web de WinQual. Puede usar esta información incluso durante la versión beta para mejorar el código. Consulte "Introducing Informe de errores de Windows" para obtener una breve introducción.
-   Puede deshabilitar la característica de Ghost en la aplicación a través de una llamada a DisableProcessWindowsGhosting (). Sin embargo, esto impide que el usuario medio cierre y reinicie una aplicación bloqueada y, a menudo, termina en un reinicio.

**Hanges: perspectiva para desarrolladores**

El sistema operativo define un bloqueo de aplicación como un subproceso de interfaz de usuario que no ha procesado mensajes durante al menos 5 segundos. Los errores obvios producen bloqueos, por ejemplo, un subproceso que espera un evento que nunca se señaliza y dos subprocesos mantienen un bloqueo y intentan adquirir los demás. Puede corregir estos errores sin demasiado esfuerzo. Sin embargo, muchos bloqueos no son tan claros. Sí, el subproceso de la interfaz de usuario no recupera los mensajes, pero está igualmente ocupado en otros trabajos "importantes" y, finalmente, volverá a procesar los mensajes.

Sin embargo, el usuario percibe esto como un error. El diseño debe coincidir con las expectativas del usuario. Si el diseño de la aplicación conduce a una aplicación que no responde, el diseño tendrá que cambiar. Por último, y esto es importante, no se puede solucionar la falta de respuesta como un error de código. requiere un trabajo inicial durante la fase de diseño. Intentar reajustar la base de código existente de una aplicación para que la interfaz de usuario tenga mayor capacidad de respuesta suele ser demasiado costosa. Las siguientes directrices de diseño pueden ayudarle.

-   Haga que la capacidad de respuesta de la interfaz de usuario sea un requisito de nivel superior; el usuario siempre debe sentirse en el control de la aplicación.
-   Asegúrese de que los usuarios pueden cancelar las operaciones que tardan más de un segundo en completarse y/o que las operaciones se pueden completar en segundo plano. proporcionar la interfaz de usuario de progreso adecuada si es necesario

![Captura de pantalla que muestra el cuadro de diálogo "copiando elementos".](images/preventinghangs-progressbar.gif)

-   Poner en cola operaciones de ejecución prolongada o de bloqueo como tareas en segundo plano (esto requiere un mecanismo de mensajería bien diseñado para informar al subproceso de la interfaz de usuario cuando se ha completado el trabajo)
-   Mantenga el código para los subprocesos de interfaz de usuario sencillos; quitar todas las llamadas de API de bloqueo posibles
-   Muestre las ventanas y los cuadros de diálogo solo cuando estén listos y totalmente operativos. Si el cuadro de diálogo necesita Mostrar información que requiere demasiado recursos para calcular, muestre primero información genérica y actualícelo sobre la marcha cuando haya más datos disponibles. Un buen ejemplo es el cuadro de diálogo Propiedades de la carpeta del explorador de Windows. Debe mostrar el tamaño total de la carpeta, la información que no está disponible en el sistema de archivos. El cuadro de diálogo se muestra de inmediato y el campo "tamaño" se actualiza desde un subproceso de trabajo:

![Captura de pantalla que muestra la página ' general ' de las propiedades de Windows con el texto ' tamaño ', ' tamaño en disco ' y ' contiene ' en un círculo.](images/preventinghangs-updatingdialog.gif)

Desafortunadamente, no hay una manera sencilla de diseñar y escribir una aplicación con capacidad de respuesta. Windows no proporciona un marco de trabajo asincrónico sencillo que permita la programación sencilla de operaciones de bloqueo o de ejecución prolongada. En las secciones siguientes se presentan algunos de los procedimientos recomendados para evitar bloqueos y resaltar algunos de los errores comunes.

## <a name="best-practices"></a>Prácticas recomendadas

**Mantener el subproceso de la interfaz de usuario simple**

La responsabilidad principal del subproceso de la interfaz de usuario es recuperar y enviar mensajes. Cualquier otro tipo de trabajo presenta el riesgo de que se bloqueen las ventanas que pertenecen a este subproceso.

**No**

-   Trasladar algoritmos que consumen muchos recursos o no están enlazados, lo que da lugar a operaciones de larga duración en subprocesos de trabajo
-   Identifique tantas llamadas de función de bloqueo como sea posible e intente moverlas a subprocesos de trabajo. cualquier función que llame a otra DLL debe ser sospechosa
-   Haga un esfuerzo adicional para quitar todas las llamadas de API de red y de e/s de archivo del subproceso de trabajo. Estas funciones pueden bloquear muchos segundos si no son minutos. Si necesita realizar cualquier tipo de e/s en el subproceso de la interfaz de usuario, considere la posibilidad de usar e/s asincrónica
-   Tenga en cuenta que el subproceso de interfaz de usuario también está atendiendo a todos los servidores COM de contenedor uniproceso (STA) hospedados por el proceso. Si realiza una llamada de bloqueo, estos servidores COM dejarán de responder hasta que vuelva a dar servicio a la cola de mensajes

**No:**

-   Espere por cualquier objeto de kernel (como evento o exclusión mutua) durante más de un período de tiempo muy breve; Si tiene que esperar, considere la posibilidad de usar MsgWaitForMultipleObjects (), que se desbloqueará cuando llegue un mensaje nuevo.
-   Compartir la cola de mensajes de ventana de un subproceso con otro subproceso mediante la función AttachThreadInput (). No solo es extremadamente difícil sincronizar correctamente el acceso a la cola, sino que también puede impedir que el sistema operativo Windows detecte correctamente una ventana de bloqueo
-   Use TerminateThread () en cualquiera de los subprocesos de trabajo. La finalización de un subproceso de este modo no permitirá liberar bloqueos ni eventos de señal, y puede producir fácilmente objetos de sincronización huérfanos
-   Llame a cualquier código "desconocido" desde el subproceso de la interfaz de usuario. Esto es especialmente cierto si la aplicación tiene un modelo de extensibilidad; no hay ninguna garantía de que el código de terceros siga las directrices de capacidad de respuesta
-   Realice cualquier tipo de llamada de difusión de bloqueo; SendMessage ( \_ difusión HWND) le pone a merced de cada aplicación mal escrita que se esté ejecutando actualmente

**Implementar patrones asincrónicos**

La eliminación de operaciones de ejecución prolongada o de bloqueo del subproceso de interfaz de usuario requiere la implementación de un marco de trabajo asincrónico que permita descargar esas operaciones en subprocesos de trabajo.

**No**

-   Use las API de mensajes de ventana asincrónica en el subproceso de la interfaz de usuario, especialmente reemplazando SendMessage por uno de sus homólogos sin bloqueo: PostMessage, SendNotifyMessage o SendMessageCallback
-   Usar subprocesos en segundo plano para ejecutar tareas de ejecución prolongada o de bloqueo. Uso de la nueva API de grupo de subprocesos para implementar los subprocesos de trabajo
-   Proporcionar compatibilidad de cancelación para tareas en segundo plano de ejecución prolongada. Para las operaciones de e/s de bloqueo, utilice la cancelación de e/s, pero solo como último recurso. no es fácil cancelar la operación "Right"
-   Implementar un diseño asincrónico para código administrado mediante el patrón IAsyncResult o mediante eventos

**Usar bloqueos de modo inteligente**

La aplicación o DLL necesita bloqueos para sincronizar el acceso a sus estructuras de datos internas. El uso de varios bloqueos aumenta el paralelismo y hace que la aplicación tenga mayor capacidad de respuesta. Sin embargo, el uso de varios bloqueos también aumenta la posibilidad de adquirir los bloqueos en distintos pedidos y hacer que los subprocesos se interbloqueen. Si cada uno de los subprocesos contiene un bloqueo y, a continuación, intenta adquirir el bloqueo del otro subproceso, sus operaciones formarán una espera circular que bloquea el progreso de los subprocesos. Puede evitar este interbloqueo solo asegurándose de que todos los subprocesos de la aplicación siempre adquieran todos los bloqueos en el mismo orden. Sin embargo, no siempre es fácil adquirir bloqueos en el orden "correcto". Los componentes de software pueden estar compuestos, pero las adquisiciones de bloqueos no pueden. Si el código llama a algún otro componente, los bloqueos de ese componente pasan a formar parte de su orden de bloqueo implícito, incluso si no tiene visibilidad sobre esos bloqueos.

Las cosas son incluso más difíciles porque las operaciones de bloqueo incluyen mucho más que las funciones habituales en las secciones críticas, exclusiones mutuas y otros bloqueos tradicionales. Cualquier llamada de bloqueo que cruza los límites de subprocesos tiene propiedades de sincronización que pueden producir un interbloqueo. El subproceso que realiza la llamada realiza una operación con la semántica "adquire" y no se puede desbloquear hasta que el subproceso de destino "libera" que llama a. Algunas funciones user32 (por ejemplo, SendMessage), así como muchas llamadas COM de bloqueo, se encuentran en esta categoría.

Peor aún, el sistema operativo tiene su propio bloqueo interno específico del proceso que a veces se mantiene mientras se ejecuta el código. Este bloqueo se adquiere cuando los archivos DLL se cargan en el proceso y, por tanto, se denomina "bloqueo del cargador". La función DllMain siempre se ejecuta en el bloqueo del cargador. Si adquiere bloqueos en DllMain (y no debería), debe hacer que el cargador del cargador sea parte del orden de bloqueo. Llamar a ciertas API de Win32 también puede adquirir el bloqueo del cargador en sus funciones de nombre, como LoadLibraryEx, GetModuleHandle y, en especial, CoCreateInstance.

Para unir todo este conjunto, examine el código de ejemplo siguiente. Esta función adquiere varios objetos de sincronización y define implícitamente un orden de bloqueo, algo que no es necesariamente obvio en la inspección de cursores. En la entrada de la función, el código adquiere una sección crítica y no la libera hasta salir de la función, lo que lo convierte en el nodo superior de la jerarquía de bloqueos. A continuación, el código llama a la función de Win32 LoadIcon (), que, en segundo plano, puede llamar al cargador del sistema operativo para cargar este archivo binario. Esta operación adquiriría el bloqueo del cargador, que ahora también forma parte de esta jerarquía de bloqueos (Asegúrese de que la función DllMain no adquiere el \_ bloqueo g CS). A continuación, el código llama a SendMessage (), una operación de bloqueo entre subprocesos, que no devolverá a menos que el subproceso de la interfaz de usuario responda. De nuevo, asegúrese de que el subproceso de interfaz de usuario nunca adquiera g \_ CS.

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

Si miramos este código, parece evidente que, de forma implícita \_ , el bloqueo de nivel superior de la jerarquía de bloqueos se hizo en g CS, incluso si solo queríamos sincronizar el acceso a las variables de miembro de clase.

**No**

-   Diseñar una jerarquía de bloqueos y obedecerla. Agregue todos los bloqueos necesarios. Hay muchas más primitivas de sincronización que simplemente mutex y CriticalSections; todos deben incluirse. Incluir el bloqueo del cargador en la jerarquía si se realizan bloqueos en DllMain ()
-   Acepte el bloqueo del Protocolo con las dependencias. Cualquier código que llame a la aplicación o que pueda llamar a la aplicación debe compartir la misma jerarquía de bloqueos.
-   Las estructuras de datos de bloqueo no funcionan. Mueva las adquisiciones de bloqueos fuera de los puntos de entrada de función y proteja únicamente el acceso a los datos con bloqueos. Si hay menos código que funciona bajo un bloqueo, es menos probable que se produzcan interbloqueos.
-   Analice las adquisiciones y versiones de bloqueo en el código de control de errores. A menudo, la jerarquía de bloqueo si se olvida al intentar recuperarse de una condición de error
-   Reemplace los bloqueos anidados por contadores de referencia, no pueden interbloqueos. Los elementos bloqueados individualmente en listas y tablas son buenos candidatos
-   Tenga cuidado al esperar en un identificador de subproceso de un archivo DLL. Asuma siempre que se puede llamar al código bajo el bloqueo del cargador. Es mejor recuento de referencias de los recursos y permitir que el subproceso de trabajo realice su propia limpieza (y, a continuación, use FreeLibraryAndExitThread para finalizar la limpieza)
-   Use la API de recorrido de la cadena de espera Si desea diagnosticar sus propios interbloqueos.

**No:**

-   Haga algo que no sea un trabajo de inicialización muy simple en la función DllMain (). Vea la función de devolución de llamada DllMain para obtener más detalles. En especial, no se llama a LoadLibraryEx o CoCreateInstance
-   Escriba sus propias primitivas de bloqueo. El código de sincronización personalizado puede introducir fácilmente errores sutiles en el código base. En su lugar, use la amplia selección de objetos de sincronización de sistema operativo.
-   Realizar cualquier trabajo en los constructores y destructores para las variables globales, se ejecutan bajo el bloqueo del cargador

**Tenga cuidado con las excepciones**

Las excepciones permiten separar el flujo normal del programa y el control de errores. Debido a esta separación, puede ser difícil conocer el estado exacto del programa antes de la excepción y el controlador de excepción podría pasar por alto pasos fundamentales para restaurar un estado válido. Esto es especialmente cierto para las adquisiciones de bloqueos que deben liberarse en el controlador para evitar interbloqueos en el futuro.

En el código de ejemplo siguiente se muestra este problema. En ocasiones, el acceso sin enlazar a la variable "buffer" producirá una infracción de acceso (AV). Este antivirus lo detecta el controlador de excepciones nativas, pero no tiene una forma sencilla de determinar si la sección crítica ya se adquirió en el momento de la excepción (es posible que incluso haya tenido lugar en alguna parte del código de EnterCriticalSection).

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

**No**

-   Quitar \_ \_ try/ \_ \_ Except siempre que sea posible; no use SetUnhandledExceptionFilter
-   Ajuste los bloqueos en \_ plantillas personalizadas de tipo PTR automáticas si utiliza excepciones de C++. El bloqueo debe liberarse en el destructor. Para las excepciones nativas, libere los bloqueos en la \_ \_ instrucción Finally
-   Tenga cuidado con el código que se ejecuta en un controlador de excepciones nativo; es posible que la excepción haya filtrado muchos bloqueos, por lo que el controlador no debe adquirir ningún

**No:**

-   Controle las excepciones nativas si no las necesita o las API de Win32. Si usa controladores de excepciones nativas para la recuperación de datos o de informes después de errores catastróficos, considere la posibilidad de usar en su lugar el mecanismo de sistema operativo predeterminado de Informe de errores de Windows
-   Usar excepciones de C++ con cualquier tipo de código de interfaz de usuario (user32); una excepción que se produce en una devolución de llamada viaja a través de las capas de código C proporcionadas por el sistema operativo. Ese código no conoce la semántica de deshacer de C++

## <a name="links-to-resources"></a>Vínculos a recursos

-   [Informe de errores de Windows](../wer/windows-error-reporting.md)
-   [Diseño asincrónico](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [E/s asincrónica](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput función)**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**auto- \_ ptr (clase)**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting función)**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Función de devolución de llamada DllMain**](../dlls/dllmain.md)
-   [Eventos](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage (función)**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Cancelación de e/s](../fileio/canceling-pending-i-o-operations.md)
-   [**IsHungAppWindow función)**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Cola de mensajes](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects función)**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nueva API de grupo de subprocesos](../procthread/thread-pool-api.md)
-   [**Función PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Reiniciar y recuperar](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback función)**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage función)**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Objetos de sincronización](../sync/about-synchronization.md)
-   [**TerminateThread (función)**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Informe de errores de Windows](../wer/windows-error-reporting.md)
-   [WinQual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
