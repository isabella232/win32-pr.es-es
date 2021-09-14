---
description: En este tema se describe cómo escribir un representador de vídeo personalizado para DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Representadores de vídeo alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162370"
---
# <a name="alternative-video-renderers"></a>Representadores de vídeo alternativos

En este tema se describe cómo escribir un representador de vídeo personalizado para DirectShow.

> [!Note]  
> En lugar de escribir un representador de vídeo personalizado, se recomienda escribir un asignador-presentador de complementos para el representador de mezcla de vídeo (VMR) o el representador de vídeo [**mejorado**](enhanced-video-renderer-filter.md) (EVR). Este enfoque le dará todas las ventajas de VMR/EVR, incluida la compatibilidad con la aceleración de vídeo directX (DXVA), el desinterlazado de hardware y la ejecución paso a paso de fotogramas, y es probable que sea más sólido que un representador de vídeo personalizado. Para obtener más información, vea los temas siguientes:
>
> -   [Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Cómo escribir un presentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Escribir un representador alternativo

Microsoft DirectShow proporciona un representador de vídeo basado en ventanas; también proporciona un representador de pantalla completa en la instalación en tiempo de ejecución. Puede usar las clases base DirectShow para escribir representadores de vídeo alternativos. Para que los representadores alternativos interactúen correctamente con DirectShow basadas en aplicaciones basadas en datos, los representadores deben cumplir las directrices descritas en este artículo. Puede usar las clases [**CBaseRenderer**](cbaserenderer.md) y [**CBaseVideoRenderer**](cbasevideorenderer.md) para ayudar a seguir estas instrucciones al implementar una representación de vídeo alternativa. Debido al desarrollo continuo de DirectShow, revise la implementación periódicamente para asegurarse de que los representadores son compatibles con la versión más reciente de DirectShow.

En este tema se de abordan muchas notificaciones que un representador es responsable de controlar. Una breve revisión de DirectShow notificaciones podría ayudar a establecer la fase. Básicamente, hay tres tipos de notificaciones que se producen en DirectShow:

-   *Notificaciones de secuencia,* que son eventos que se producen en la secuencia multimedia y se pasan de un filtro al siguiente. Pueden ser notificaciones de inicio, vaciado final o fin de flujo y se envían mediante una llamada al método adecuado en el pin de entrada del filtro de bajada (por [**ejemplo, IPin::BeginFlush).**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)
-   *Filtrar notificaciones de grafo,* que son eventos enviados desde un filtro al Administrador de Graph, como [**EC \_ COMPLETE.**](ec-complete.md) Para ello, se llama al [**método IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) en el Administrador de Graph filtros.
-   *Notificaciones de aplicación*, que se recuperan del Administrador de Graph mediante la aplicación de control. Una aplicación llama al [**método IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en filter Graph Manager para recuperar estos eventos. A menudo, filter Graph Manager pasa a través de los eventos que recibe a la aplicación.

En este tema se describe la responsabilidad del filtro de representador en el control de las notificaciones de flujo que recibe y en el envío de las notificaciones de gráfico de filtros adecuadas.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Control de notificaciones de fin de flujo y vaciado

Una notificación de fin de flujo comienza en un filtro ascendente (como el filtro de origen) cuando ese filtro detecta que no puede enviar más datos. Se pasa a través de todos los filtros del gráfico y, finalmente, termina en el representador, que es responsable de enviar posteriormente una notificación [**EC \_ COMPLETE**](ec-complete.md) al Administrador de Graph Filtro. Los representadores tienen responsabilidades especiales a la hora de controlar estas notificaciones.

Un representador recibe una notificación de fin de flujo cuando el filtro ascendente llama al método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) de su pin de entrada. Un representador debe tener en cuenta esta notificación y seguir representando los datos que ya ha recibido. Una vez recibidos todos los datos restantes, el representador debe enviar una notificación [**EC \_ COMPLETE**](ec-complete.md) al Administrador de Graph filtros. La **notificación \_ EC COMPLETE** solo debe enviarla una vez un representador cada vez que llegue al final de una secuencia. Además, las **notificaciones EC \_ COMPLETE** nunca deben enviarse excepto cuando se ejecuta el gráfico de filtros. Por lo tanto, si el gráfico de filtros se pausa cuando un filtro de origen envía una notificación de fin de flujo, **EC \_ COMPLETE** no se debe enviar hasta que se ejecute finalmente el gráfico de filtros.

Las llamadas a los métodos [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) después de que se señale una notificación de fin de flujo deben rechazarse. **E \_ UNEXPECTED** es el mensaje de error más adecuado que se devuelve en este caso.

Cuando se detiene un gráfico de filtros, cualquier notificación de fin de flujo almacenada en caché debe borrarse y no enviarse cuando se inicia la siguiente vez. Esto se debe a que el Administrador de Graph siempre pausa todos los filtros justo antes de ejecutarlos para que se produzca el vaciado adecuado. Por ejemplo, si el gráfico de filtros está en pausa y se recibe una notificación de fin de flujo y, a continuación, se detiene el gráfico de filtros, el representador no debe enviar una notificación [**EC \_ COMPLETE**](ec-complete.md) cuando se ejecute posteriormente. Si no se ha producido ninguna búsqueda, el filtro de origen enviará automáticamente otra notificación de fin de secuencia durante el estado de pausa que precede a un estado de ejecución. Por otro lado, si se ha producido una búsqueda mientras se detiene el gráfico de filtros, es posible que el filtro de origen tenga datos para enviar, por lo que no enviará una notificación de fin de flujo.

Los representadores de vídeo a menudo dependen de las notificaciones de final de secuencia para más que el envío de [**notificaciones EC \_ COMPLETE.**](ec-complete.md) Por ejemplo, si una secuencia ha terminado de reproducirse (es decir, se envía una notificación de fin de secuencia) y se arrastra otra ventana sobre una ventana de representador de vídeo, se generarán varios mensajes de ventana [**\_ WM PAINT.**](/windows/desktop/gdi/wm-paint) La práctica habitual para ejecutar representadores de vídeo es evitar volver a dibujar el marco actual tras la recepción de mensajes **WM \_ PAINT** (en función de la suposición de que se recibirá otro fotograma que se va a dibujar). Sin embargo, cuando se ha enviado la notificación de fin de flujo, el representador está en estado de espera; todavía se está ejecutando, pero es consciente de que no recibirá ningún dato adicional. En estas circunstancias, el representador dibuja de forma personalizada el área de reproducción en negro.

Controlar el vaciado es una complicación adicional para los representadores. El vaciado se lleva a cabo a través de un par de [**métodos IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**denominados BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) [**y EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) El vaciado es básicamente un estado adicional que el representador debe controlar. No es posible que un filtro de origen llame a **BeginFlush** sin llamar a **EndFlush,** por lo que esperamos que el estado sea corto y discreto. sin embargo, el representador debe controlar correctamente los datos o las notificaciones que recibe durante la transición de vaciado.

Los datos recibidos después de [**llamar a BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) deben rechazarse inmediatamente devolviendo **S \_ FALSE**. Además, cualquier notificación de fin de flujo almacenada en caché también debe borrarse cuando se vacía un representador. Normalmente, un representador se vaciará en respuesta a una búsqueda. El vaciado garantiza que los datos antiguos se borran del gráfico de filtros antes de enviar muestras nuevas. (Normalmente, la reproducción de dos secciones de una secuencia, una tras otra, se controla mejor mediante comandos diferidos en lugar de esperar a que finalice una sección y, a continuación, emitir un comando seek).

## <a name="handling-state-changes-and-pause-completion"></a>Controlar los cambios de estado y pausar la finalización

Un filtro de representador se comporta igual que cualquier otro filtro del gráfico de filtros cuando se cambia su estado, con la siguiente excepción. Después de pausarse, el representador tendrá algunos datos en cola, listos para representarse cuando se ejecute posteriormente. Cuando se detiene el representador de vídeo, se mantiene en estos datos en cola. Se trata de una excepción a la regla DirectShow que los filtros no deben tener recursos mientras se detiene el gráfico de filtros.

La razón de esta excepción es que, al contener recursos, el representador siempre tendrá una imagen con la que volver a dibujar la ventana si recibe un [**mensaje \_ WM PAINT.**](/windows/desktop/gdi/wm-paint) También tiene una imagen para satisfacer métodos, como [**CBaseControlVideo::GetStaticImage**](cbasecontrolvideo-getstaticimage.md), que solicitan una copia de la imagen actual. Otro efecto de mantener los recursos es que mantener en la imagen impide que se desasigne el asignador, lo que a su vez hace que el siguiente cambio de estado se produzca mucho más rápido porque los búferes de imagen ya están asignados.

Un representador de vídeo debe representar y liberar ejemplos solo durante la ejecución. Mientras está en pausa, el filtro podría representarlos (por ejemplo, al dibujar una imagen de póster estático en una ventana), pero no debe liberarlos. Los representadores de audio no realizarán ninguna representación mientras están en pausa (aunque pueden realizar otras actividades, como preparar el dispositivo de onda, por ejemplo). La hora a la que se deben representar los ejemplos se obtiene combinando el tiempo de secuencia del ejemplo con el tiempo de referencia pasado como parámetro al [**método IMediaControl::Run.**](/windows/desktop/api/Control/nf-control-imediacontrol-run) Los representadores deben rechazar las muestras con horas de inicio menores o iguales que las horas de finalización.

Cuando una aplicación pausa un gráfico de filtros, el gráfico de filtros no devuelve desde su método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) hasta que haya datos en cola en los representadores. Para garantizar esto, cuando un representador está en pausa, debe devolver S FALSE si no hay ningún dato en espera \_ para representarse. Si tiene datos en cola, puede devolver **S \_ OK**.

El Administrador Graph filtros comprueba todos los valores devueltos al pausar un gráfico de filtro para asegurarse de que los representadores tienen datos en cola. Si uno o varios filtros no están listos, el Administrador de filtros Graph sondea los filtros del gráfico mediante una llamada a [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). El **método GetState** toma un parámetro de tiempo de espera. Un filtro (normalmente un representador) que sigue esperando a que lleguen los datos antes de completar el cambio de estado devuelve **VFW \_ S STATE \_ \_ INTERMEDIATE** si el **método GetState** expira. Una vez que los datos llegan al representador, **GetState** debe devolverse inmediatamente con **S \_ OK**.

En el estado intermedio y completado, el estado de filtro notificado será Estado \_ en pausa. Solo el valor devuelto indica si el filtro está realmente listo o no. Si, mientras un representador está esperando a que lleguen los datos, su filtro de origen envía una notificación de fin de flujo, también debería completar el cambio de estado.

Una vez que todos los filtros tienen datos esperando su representación, el gráfico de filtros completará su cambio de estado de pausa.

## <a name="handling-termination"></a>Control de la terminación

Los representadores de vídeo deben controlar correctamente los eventos de terminación del usuario. Esto implica ocultar correctamente la ventana y saber qué hacer si posteriormente se obliga a mostrar una ventana. Además, los representadores de vídeo deben notificar al Administrador de filtros Graph cuando se destruye su ventana (o con más precisión, cuando se quita el representador del gráfico de filtros) para liberar recursos.

Si el usuario cierra la ventana de vídeo (por ejemplo, presionando ALT+F4), la convención es ocultar la ventana inmediatamente y enviar una notificación [**\_ USERABORT**](ec-userabort.md) de EC al Administrador de filtros Graph. Esta notificación se pasa a través de la aplicación, lo que detendrá la reproducción del gráfico. Después de **enviar EC \_ USERABORT,** un representador de vídeo debe rechazar los ejemplos adicionales que se le entreguen.

El representador debe dejar la marca con el gráfico detenido hasta que se detenga posteriormente, momento en el que se debe restablecer para que una aplicación pueda invalidar la acción del usuario y seguir reproduciendo el gráfico si lo desea. Si se presiona ALT+F4 mientras se ejecuta el vídeo, la ventana se ocultará y se rechazarán todas las muestras posteriores entregadas. Si posteriormente se muestra la ventana (quizás a través de [**IVideoWindow::p ut \_ Visible),**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)no se debe generar ninguna notificación [**EC \_ REPAINT.**](ec-repaint.md)

El representador de vídeo también debe enviar la notificación [**EC \_ WINDOW \_ DESTROYED**](ec-window-destroyed.md) al gráfico de filtros cuando el representador de vídeo termina. De hecho, es mejor controlar esto cuando se llama al método [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del representador con un parámetro NULL (lo que indica que el representador está a punto de quitarse del gráfico de filtros), en lugar de esperar a que se destruya la ventana de vídeo real. El envío de esta notificación permite que el distribuidor de complementos del Administrador de filtros Graph pase los recursos que dependen del foco de la ventana a otros filtros, como los dispositivos de audio.

## <a name="handling-dynamic-format-changes"></a>Control de cambios de formato dinámico

En algunos casos, el filtro ascendente del representador podría intentar cambiar el formato de vídeo mientras se reproduce el vídeo. Suele ser el descomprimidor de vídeo el que inicia un cambio de formato dinámico.

Un filtro ascendente que intente cambiar los formatos dinámicamente siempre debe llamar al método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de entrada del representador. Un representador de vídeo tiene cierta libertad sobre los tipos de cambios de formato dinámico que debe admitir. Como mínimo, debe permitir que el filtro ascendente cambie las paletas. Cuando un filtro ascendente cambia los tipos de medios, asocia el tipo de medio al primer ejemplo entregado en el nuevo formato. Si el representador contiene ejemplos en una cola para su representación, no debe cambiar el formato hasta que represente el ejemplo con el cambio de tipo.

Un representador de vídeo también puede solicitar un cambio de formato desde el descodificador. Por ejemplo, podría pedir al descodificador que proporcione un formato compatible con DirectDraw con un **valor biHeight negativo.** Cuando el representador está en pausa, debe llamar a [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin ascendente para ver qué formatos puede proporcionar el descodificador. Sin embargo, es posible que el descodificador no enumere todos los tipos que puede aceptar, por lo que el representador debe ofrecer algunos tipos incluso si el descodificador no los anuncia.

Si el descodificador puede cambiar al formato solicitado, devuelve **S \_ OK** desde [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). A continuación, el representador asocia el nuevo tipo de medio al siguiente ejemplo multimedia en el asignador ascendente. Para que esto funcione, el representador debe proporcionar un asignador personalizado que implemente un método privado para adjuntar el tipo de medio al ejemplo siguiente. (Dentro de este método privado, llame [**a IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para establecer el tipo).

El pin de entrada del representador debe devolver el asignador personalizado del representador en el [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) Invalide [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para que se produce un error si el filtro ascendente no usa el asignador del representador.

Con algunos descodificadores, establecer **biHeight** en un número positivo en los tipos YUV hace que el descodificador dibuje la imagen al revés. (Esto es incorrecto y debe considerarse un error en el descodificador).

Cada vez que el representador de vídeo detecta un cambio de formato, debe enviar una notificación [**EC \_ DISPLAY \_ CHANGED.**](ec-display-changed.md) La mayoría de los representadores de vídeo seleccionan un formato durante la conexión para que el formato se pueda dibujar eficazmente a través de GDI. Si el usuario cambia el modo de presentación actual sin reiniciar el equipo, es posible que un representador se encuentre con una conexión de formato de imagen no segura y envíe esta notificación. El primer parámetro debe ser el pin que necesita volver a conectarse. El Administrador Graph filtro organizará para que el gráfico de filtros se detenga y se vuelva a conectar el pin. Durante la reconexión posterior, el representador puede aceptar un formato más adecuado.

Cada vez que un representador de vídeo detecta un cambio de paleta en la secuencia, debe enviar la notificación [**EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md) al Administrador de Graph. Los DirectShow de vídeo detectan si una paleta ha cambiado realmente en formato dinámico o no. Los representadores de vídeo no solo hacen esto para filtrar el número de notificaciones EC **\_ PALETTE \_ CHANGED** enviadas, sino también para reducir la cantidad de creación, instalación y eliminación de paletas necesarias.

Por último, el representador de vídeo también puede detectar que el tamaño del vídeo ha cambiado, en cuyo caso debe enviar la notificación [**EC \_ VIDEO SIZE \_ \_ CHANGED.**](ec-video-size-changed.md) Una aplicación podría usar esta notificación para negociar el espacio en un documento compuesto. Las dimensiones de vídeo reales están disponibles a través de la interfaz de control [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Los DirectShow de datos detectan si el vídeo ha cambiado realmente de tamaño o no antes de enviar estos eventos.

## <a name="handling-persistent-properties"></a>Control de propiedades persistentes

Todas las propiedades establecidas a través de las interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) [**e IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) están diseñadas para ser persistentes entre conexiones. Por lo tanto, desconectar y volver a conectar un representador no debería mostrar ningún efecto en el tamaño, la posición o los estilos de la ventana. Sin embargo, si las dimensiones de vídeo cambian entre conexiones, el representador debe restablecer los rectángulos de origen y destino a sus valores predeterminados. Las posiciones de origen y destino se establecen a través de la **interfaz IBasicVideo.**

[**Tanto IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) como [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) proporcionan acceso suficiente a las propiedades para permitir que una aplicación guarde y restaure todos los datos de la interfaz en un formato persistente. Esto será útil para las aplicaciones que deben guardar la configuración exacta y las propiedades de los gráficos de filtro durante una sesión de edición y restaurarlas más adelante.

## <a name="handling-ec_repaint-notifications"></a>Control de notificaciones \_ EC REPAINT

La [**notificación \_ EC REPAINT**](ec-repaint.md) solo se envía cuando el representador está en pausa o detenido. Esta notificación indica al Administrador de Graph que el representador necesita datos. Si el gráfico de filtros se detiene cuando recibe una de estas notificaciones, pausará el gráfico de filtros, esperará a que todos los filtros reciban datos (llamando a [**GetState)**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)y, a continuación, los detendrá de nuevo. Cuando se detiene, un representador de vídeo debe mantener la imagen para que se puedan controlar los mensajes [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) posteriores.

Por lo tanto, si un representador de vídeo recibe un mensaje [**\_ WM PAINT**](/windows/desktop/gdi/wm-paint) cuando se detiene o pausa y no tiene nada con el que pintar su ventana, debe enviar EC [**\_ REPAINT**](ec-repaint.md) al Administrador de Graph Filtro. Si se recibe una notificación **\_ EC REPAINT** mientras está en pausa, el Administrador de filtros Graph llama [**a IMediaPosition::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) con la posición actual (es decir, busca en la posición actual). Esto hace que los filtros de origen vacíe el gráfico de filtros y hace que se envíen nuevos datos a través del gráfico de filtros.

Un representador solo debe enviar una de estas notificaciones a la vez. Por lo tanto, una vez que el representador envía una notificación, debe asegurarse de que no se envíen más hasta que se entreguen algunas muestras. La manera convencional de hacerlo es tener una marca para indicar que se puede enviar un repintado, que se desactivará después de enviar una notificación [**\_ EC REPAINT.**](ec-repaint.md) Esta marca se debe restablecer una vez que se entregan los datos o cuando se vacía el pin de entrada, pero no si se señala el final del flujo en el pin de entrada.

Si el representador no supervisa sus notificaciones [**\_ EC REPAINT,**](ec-repaint.md) desbordará el Administrador de filtros Graph con solicitudes **EC \_ REPAINT** (que son relativamente costosas de procesar). Por ejemplo, si un representador no tiene ninguna imagen que dibujar y se arrastra otra ventana a través de la ventana del representador en una operación de arrastre completo, el representador recibe varios mensajes [**\_ WM PAINT.**](/windows/desktop/gdi/wm-paint) Solo el primero de ellos debe generar una notificación de eventos **\_ EC REPAINT** desde el representador al Administrador de Graph filtros.

Un representador debe enviar su pin de entrada como primer parámetro a la [**notificación \_ EC REPAINT.**](ec-repaint.md) Al hacerlo, se consultará el pin de salida adjunto para [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)y, si se admite, la notificación **\_ EC REPAINT** se enviará primero allí. Esto permite que los pines de salida controle los repintados antes de que se deba tocar el gráfico de filtro. Esto no se hará si se detiene el gráfico de filtros, ya que no habría búferes disponibles en el asignador del representador confirmado.

Si el pin de salida no puede controlar la solicitud y el gráfico de filtros se está ejecutando, se omite la notificación [**\_ EC REPAINT.**](ec-repaint.md) Un pin de salida debe devolver **S \_ OK** desde [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) para indicar que procesó correctamente la solicitud de repintado. Se llamará al pin de salida en el subproceso de trabajo filter Graph Manager, lo que evita que el representador llame directamente al pin de salida, por lo que evita cualquier problema de interbloqueo. Si el gráfico de filtros está detenido o en pausa y la salida no controla la solicitud, se realiza el procesamiento predeterminado.

## <a name="handling-notifications-in-full-screen-mode"></a>Control de notificaciones en modo Full-Screen usuario

El [**distribuidor del complemento IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) del gráfico de filtros administra la reproducción a pantalla completa. Intercambiará un representador de vídeo por un representador de pantalla completa especialista, extenderá una ventana de un representador a pantalla completa o hará que el representador implemente la reproducción a pantalla completa directamente. Para interactuar en protocolos de pantalla completa, un representador de vídeo debe enviar una notificación [**EC \_ ACTIVATE**](ec-activate.md) siempre que su ventana esté activada o desactivada. Es decir, se debe enviar **una notificación \_ EC ACTIVATE** para cada mensaje WM \_ ACTIVATEAPP que recibe un representador.

Cuando se usa un representador en modo de pantalla completa, estas notificaciones administran la entrada y salida de ese modo de pantalla completa. La desactivación de ventanas suele producirse cuando un usuario presiona ALT+TAB para cambiar a otra ventana, que el representador de pantalla completa de DirectShow usa como indicación para volver al modo de representación típico.

Cuando se envía la notificación [**EC \_ ACTIVATE**](ec-activate.md) al Administrador de filtros Graph tras salir del modo de pantalla completa, el Administrador de filtros Graph envía una notificación EC [**\_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md) a la aplicación de control. La aplicación podría usar esta notificación para restaurar el estado de un botón de pantalla completa, por ejemplo. Las **notificaciones \_ EC ACTIVATE** se usan internamente DirectShow administrar la conmutación a pantalla completa en las indicaciones de los representadores de vídeo.

## <a name="summary-of-notifications"></a>Resumen de notificaciones

En esta sección se enumeran las notificaciones de gráfico de filtro que un representador puede enviar.



| Notificación de evento                                        | Descripción                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                       | Enviado por representadores de vídeo en modo de representación a pantalla completa para cada mensaje \_ WM ACTIVATEAPP recibido.                                                                                                  |
| [**EC \_ COMPLETE**](ec-complete.md)                       | Los representadores los envían después de representar todos los datos.                                                                                                                                               |
| [**EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md)        | Enviado por representadores de vídeo cuando cambia el formato de presentación.                                                                                                                                            |
| [**EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md)        | Se envía cada vez que un representador de vídeo detecta un cambio de paleta en la secuencia.                                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                         | Enviado por representadores de vídeo detenidos o en pausa cuando se recibe un mensaje WM PAINT y \_ no hay datos que mostrar. Esto hace que el administrador Graph filtro genere un marco para pintar en la pantalla. |
| [**\_USERABORT DE EC**](ec-userabort.md)                     | Enviados por representadores de vídeo para indicar un cierre que el usuario solicitó (por ejemplo, un usuario que cierra la ventana de vídeo).                                                                               |
| [**CAMBIO \_ EN EL TAMAÑO DEL VÍDEO DE \_ \_ EC**](ec-video-size-changed.md) | Los representadores de vídeo los envían cada vez que se detecta un cambio en el tamaño del vídeo nativo.                                                                                                                       |
| [**VENTANA \_ EC \_ DESTROYED**](ec-window-destroyed.md)      | Los representadores de vídeo envían cuando se quita o destruye el filtro para que los recursos que dependen del foco de ventana se puedan pasar a otros filtros.                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de representadores de vídeo](writing-video-renderers.md)
</dt> </dl>

 

 
