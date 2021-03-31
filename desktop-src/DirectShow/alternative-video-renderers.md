---
description: En este tema se describe cómo escribir un representador de vídeo personalizado para DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Representadores de vídeo alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806608"
---
# <a name="alternative-video-renderers"></a>Representadores de vídeo alternativos

En este tema se describe cómo escribir un representador de vídeo personalizado para DirectShow.

> [!Note]  
> En lugar de escribir un representador de vídeo personalizado, se recomienda escribir un asignador de complemento para el representador de mezcla de vídeo (VMR) o [**Enhanced video renderer**](enhanced-video-renderer-filter.md) (EVR). Este enfoque le proporcionará todas las ventajas de VMR/EVR, incluida la compatibilidad con la aceleración de vídeo de DirectX (DXVA), el desentrelazado de hardware y la ejecución de fotogramas, y es probable que sea más robusto que un representador de vídeo personalizado. Para obtener más información, vea los temas siguientes:
>
> -   [Modo de reproducción no representativo de VMR (asignador personalizado)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Cómo escribir un presentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Escribir un representador alternativo

Microsoft DirectShow proporciona un representador de vídeo basado en ventanas. también proporciona un representador de pantalla completa en la instalación en tiempo de ejecución. Puede usar las clases base de DirectShow para escribir representadores de vídeo alternativos. Para que los representadores alternativos interactúen correctamente con las aplicaciones basadas en DirectShow, los representadores deben cumplir las directrices descritas en este artículo. Puede usar las clases [**CBaseRenderer**](cbaserenderer.md) y [**CBaseVideoRenderer**](cbasevideorenderer.md) para ayudar a seguir estas instrucciones al implementar una representación de vídeo alternativa. Debido al desarrollo continuo de DirectShow, revise la implementación periódicamente para asegurarse de que los representadores son compatibles con la versión más reciente de DirectShow.

En este tema se tratan muchas notificaciones que un representador es responsable de controlar. Una breve revisión de las notificaciones de DirectShow puede ayudarle a establecer la fase. Esencialmente, hay tres tipos de notificaciones que se producen en DirectShow:

-   *Notificaciones de secuencia*, que son eventos que se producen en el flujo multimedia y se pasan de un filtro al siguiente. Estas pueden ser el vaciado inicial, el vaciado de final o las notificaciones de final de secuencia y se envían llamando al método adecuado en el PIN de entrada del filtro de nivel inferior (por ejemplo, [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)).
-   *Filtre las notificaciones de gráficos*, que son eventos enviados desde un filtro al administrador de gráficos de filtro, como la [**\_ finalización de EC**](ec-complete.md). Esto se logra mediante una llamada al método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) en el administrador de gráficos de filtro.
-   *Notificaciones de aplicación*, que la aplicación de control recupera del administrador de gráficos de filtro. Una aplicación llama al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en el administrador de gráficos de filtro para recuperar estos eventos. A menudo, el administrador de gráficos de filtro pasa por los eventos que recibe a la aplicación.

En este tema se describe la responsabilidad del filtro de representador en el control de las notificaciones de transmisión que recibe y en el envío de notificaciones de gráfico de filtro apropiadas.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Control de las notificaciones de final de secuencia y de vaciado

Una notificación de final de secuencia comienza en un filtro de nivel superior (como el filtro de origen) cuando ese filtro detecta que no puede enviar más datos. Se pasa por todos los filtros del gráfico y finalmente finaliza en el representador, que es responsable de enviar posteriormente una notificación de [**\_ finalización de EC**](ec-complete.md) al administrador de gráficos de filtro. Los representadores tienen responsabilidades especiales cuando se trata de administrar estas notificaciones.

Un representador recibe una notificación de final de secuencia cuando el filtro de nivel superior llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) del PIN de entrada. Un representador debe anotar esta notificación y continuar representando los datos que ya haya recibido. Una vez que se han recibido todos los datos restantes, el representador debe enviar una notificación de [**\_ finalización de EC**](ec-complete.md) al administrador de gráficos de filtro. La notificación de finalización de **EC \_** solo debe enviarse una vez por un representador cada vez que llega al final de una secuencia. Además, las notificaciones **\_ completas de EC** nunca deben enviarse, excepto cuando se está ejecutando el gráfico de filtro. Por lo tanto, si el gráfico de filtros se pausa cuando un filtro de origen envía una notificación de final de secuencia, no se debe enviar la finalización de **EC \_** hasta que finalmente se ejecute el gráfico de filtro.

Las llamadas a los métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) después de una notificación de final de secuencia se deben rechazar. **E \_ Inesperado** es el mensaje de error más apropiado que se devuelve en este caso.

Cuando se detiene un gráfico de filtros, se debe borrar cualquier notificación de final de secuencia almacenada en caché y no volver a enviarla cuando se inicie la siguiente. Esto se debe a que Filter Graph Manager siempre pausa todos los filtros justo antes de ejecutarlos para que se produzca el vaciado adecuado. Por lo tanto, por ejemplo, si el gráfico de filtros está en pausa y se recibe una notificación de final de secuencia y, a continuación, se detiene el gráfico de filtros, el representador no debe enviar una notificación [**\_ completa de EC**](ec-complete.md) cuando se ejecute posteriormente. Si no se ha producido ninguna búsqueda, el filtro de origen enviará automáticamente otra notificación de final de secuencia durante el estado de pausa que precede a un estado de ejecución. Por otro lado, si se ha producido una búsqueda mientras se detiene el gráfico de filtros, el filtro de origen podría tener datos para enviar, por lo que no enviará una notificación de final de secuencia.

Los representadores de vídeo a menudo dependen de las notificaciones de final de secuencia durante más tiempo que el envío de notificaciones [**\_ completas de EC**](ec-complete.md) . Por ejemplo, si una secuencia ha terminado de reproducirse (es decir, se envía una notificación de final de secuencia) y se arrastra otra ventana sobre una ventana de representador de vídeo, se generará una serie de mensajes de ventana de [**\_ Paint de WM**](/windows/desktop/gdi/wm-paint) . La práctica habitual para ejecutar representadores de vídeo es abstenerse de volver a pintar el fotograma actual tras la recepción de los mensajes de **\_ pintura de WM** (en función de la suposición de que se recibirá otro fotograma que se va a dibujar). Sin embargo, cuando se ha enviado la notificación de final de secuencia, el representador se encuentra en estado de espera; todavía se está ejecutando pero es consciente de que no recibirá ningún dato adicional. En estas circunstancias, el representador normalmente dibuja el área de reproducción en negro.

Controlar el vaciado es una complicación adicional para los representadores. El vaciado se lleva a cabo a través de un par de métodos [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) denominados [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush). El vaciado es esencialmente un estado adicional que el representador debe controlar. No es válido que un filtro de origen llame a **BeginFlush** sin llamar a **EndFlush**, por lo que espero que el estado sea corto y discreto; sin embargo, el representador debe administrar correctamente los datos o las notificaciones que recibe durante la transición de vaciado.

Cualquier dato recibido después de llamar a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) debe rechazarse inmediatamente devolviendo **S \_ false**. Además, cualquier notificación de final de secuencia en caché también debe borrarse cuando se vacía un representador. Un representador se vaciará normalmente como respuesta a una búsqueda. El vaciado garantiza que los datos antiguos se borran del gráfico de filtro antes de que se envíen los ejemplos actualizados. (Normalmente, la reproducción de dos secciones de una secuencia, una tras otra, se controla mejor mediante comandos diferidos en lugar de esperar a que finalice una sección y, a continuación, emitir un comando de búsqueda).

## <a name="handling-state-changes-and-pause-completion"></a>Control de los cambios de estado y pausa de la finalización

Un filtro de representador se comporta igual que cualquier otro filtro del gráfico de filtro cuando se cambia su estado, con la siguiente excepción. Una vez que se haya pausado, el representador tendrá algunos datos en cola, listos para ser representados cuando se ejecuten posteriormente. Cuando se detiene el representador de vídeo, este se mantiene en los datos en cola. Se trata de una excepción a la regla de DirectShow de que los filtros no deben mantener ningún recurso mientras se detiene el gráfico de filtros.

La razón de esta excepción es que, al almacenar los recursos, el representador siempre tendrá una imagen con la que volver a dibujar la ventana si recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) . También tiene una imagen para satisfacer métodos, como [**CBaseControlVideo:: GetStaticImage**](cbasecontrolvideo-getstaticimage.md), que solicitan una copia de la imagen actual. Otro efecto de la retención de recursos es que al mantener la imagen se detiene el asignador, lo que, a su vez, hace que el siguiente cambio de estado se realice mucho más rápido porque los búferes de imagen ya están asignados.

Un representador de vídeo debe presentar y publicar los ejemplos solo mientras se ejecuta. Mientras está en pausa, el filtro podría representarlos (por ejemplo, al dibujar una imagen de póster estático en una ventana), pero no debe liberarlas. Los representadores de audio no realizarán ninguna representación mientras están en pausa (aunque pueden realizar otras actividades, como preparar el dispositivo de onda, por ejemplo). La hora a la que se deben representar los ejemplos se obtiene combinando el tiempo de flujo en el ejemplo con el tiempo de referencia pasado como un parámetro al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Los representadores deben rechazar los ejemplos con horas de inicio menores o iguales que las horas de finalización.

Cuando una aplicación pone en pausa un gráfico de filtros, el gráfico de filtros no vuelve de su método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) hasta que haya datos en cola en los representadores. Para garantizar esto, cuando un representador está en pausa, debe devolver S \_ false si no hay ningún dato en espera para ser representado. Si tiene datos en cola, puede devolver **S \_ correctos**.

Filter Graph Manager comprueba todos los valores devueltos al pausar un gráfico de filtros para asegurarse de que los representadores tengan datos en cola. Si uno o más filtros no están listos, el administrador de gráficos de filtros sondea los filtros del gráfico mediante una llamada a [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). El método **GetState** toma un parámetro de tiempo de espera. Un filtro (normalmente un representador) que todavía está esperando a que lleguen los datos antes de completar el cambio de estado devuelve el **\_ Estado VFW S \_ \_ intermedia** si el método **GetState** expira. Una vez que los datos llegan al representador, **GetState** debe devolverse inmediatamente con **S \_ OK**.

En el estado intermedio y completado, el estado de filtro indicado será en \_ pausa. Solo el valor devuelto indica si el filtro está realmente listo o no. Si, mientras un representador está esperando a que lleguen los datos, su filtro de origen envía una notificación de final de secuencia, que también debe completar el cambio de estado.

Una vez que todos los filtros realmente tienen datos en espera de ser representados, el gráfico de filtros completará el cambio de estado de pausa.

## <a name="handling-termination"></a>Control de la terminación

Los representadores de vídeo deben controlar correctamente los eventos de finalización del usuario. Esto implica ocultar correctamente la ventana y saber qué hacer si posteriormente se fuerza la presentación de una ventana. Además, los representadores de vídeo deben notificar al administrador de gráficos de filtro cuando se destruya su ventana (o con más precisión, cuando el representador se quite del gráfico de filtros) libere recursos.

Si el usuario cierra la ventana de vídeo (por ejemplo, presionando ALT + F4), la Convención consiste en ocultar la ventana inmediatamente y enviar una [**notificación \_ USERABORT de EC**](ec-userabort.md) al administrador de gráficos de filtros. Esta notificación se pasa a la aplicación, que detendrá la reproducción del gráfico. Después de enviar el **\_ USERABORT de EC**, un representador de vídeo debe rechazar cualquier ejemplo adicional que se le haya entregado.

El representador debe dejar en el representador hasta que se detenga, momento en el que se debe restablecer para que una aplicación pueda invalidar la acción del usuario y seguir reproduciendo el gráfico si lo desea. Si se presiona ALT + F4 mientras se está ejecutando el vídeo, se ocultará la ventana y se rechazarán todas las muestras proporcionadas. Si la ventana se muestra posteriormente (quizás a través de [**IVideoWindow::p UT \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)), no se deben generar notificaciones de [**\_ Repaint de EC**](ec-repaint.md) .

El representador de vídeo también debe enviar la notificación de la [**ventana de EC \_ \_ destruida**](ec-window-destroyed.md) al gráfico de filtros cuando el representador de vídeo está finalizando. De hecho, es mejor controlar esto cuando se llama al método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del representador con un parámetro null (lo que indica que el representador está a punto de quitarse del gráfico de filtro), en lugar de esperar hasta que se destruya la ventana de vídeo real. El envío de esta notificación permite que el distribuidor del complemento del administrador de gráficos de filtro pase los recursos que dependen del foco de la ventana a otros filtros, como los dispositivos de audio.

## <a name="handling-dynamic-format-changes"></a>Control de los cambios de formato dinámico

En algunos casos, el filtro de nivel superior del representador podría intentar cambiar el formato de vídeo mientras se reproduce el vídeo. Suele ser el descompresor de vídeo que inicia un cambio de formato dinámico.

Un filtro de nivel superior que intenta cambiar los formatos de forma dinámica siempre debe llamar al método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de entrada del representador. Un representador de vídeo tiene algunas libertad en cuanto a los tipos de cambios de formato dinámicos que debe admitir. Como mínimo, debe permitir que el filtro de nivel superior cambie las paletas. Cuando un filtro de nivel superior cambia los tipos de medios, adjunta el tipo de medio al primer ejemplo entregado en el nuevo formato. Si el representador contiene muestras en una cola para su representación, no debe cambiar el formato hasta que represente el ejemplo con el cambio de tipo.

Un representador de vídeo también puede solicitar un cambio de formato desde el descodificador. Por ejemplo, podría pedirle al descodificador que proporcione un formato compatible con DirectDraw con una **bialtura** negativa. Cuando el representador está en pausa, debe llamar a [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de nivel superior para ver qué formatos puede proporcionar el descodificador. Sin embargo, es posible que el descodificador no enumere todos los tipos que puede aceptar, por lo que el representador debería ofrecer algunos tipos incluso si el descodificador no los anuncia.

Si el descodificador puede cambiar al formato solicitado, devuelve **S \_** de [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). A continuación, el representador asocia el nuevo tipo de medio al siguiente ejemplo multimedia en el asignador de nivel superior. Para que esto funcione, el representador debe proporcionar un asignador personalizado que implemente un método privado para adjuntar el tipo de medio a la siguiente muestra. (Dentro de este método privado, llame a [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para establecer el tipo).

El PIN de entrada del representador debe devolver el asignador personalizado del representador en el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) . Invalide [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para que se produzca un error si el filtro de nivel superior no usa el asignador del representador.

Con algunos descodificadores, el establecimiento de **biheight** en un número positivo en los tipos YUV hace que el descodificador dibuje la imagen al revés. (Esto es incorrecto y debe considerarse un error en el descodificador).

Cada vez que el representador de vídeo detecta un cambio de formato, debe enviar una notificación de [**\_ visualización de \_ cambios de EC**](ec-display-changed.md) . La mayoría de los representadores de vídeo eligen un formato durante la conexión para que el formato se pueda dibujar eficazmente a través de GDI. Si el usuario cambia el modo de presentación actual sin reiniciar el equipo, un representador podría encontrarse con una conexión de formato de imagen incorrecta y debería enviar esta notificación. El primer parámetro debe ser el PIN que necesita volver a conectarse. Filter Graph Manager organizará el gráfico de filtro para que se detenga y el PIN se vuelva a conectar. Durante la reconexión posterior, el representador puede aceptar un formato más adecuado.

Siempre que un representador de vídeo detecta un cambio de paleta en la secuencia, debe enviar la notificación de cambio de la [**\_ \_ paleta de EC**](ec-palette-changed.md) al administrador de gráficos de filtro. Los representadores de vídeo de DirectShow detectan si una paleta ha cambiado realmente en formato dinámico o no. Los representadores de vídeo lo hacen no solo para filtrar el número de notificaciones de la **paleta de EC que \_ \_ han cambiado** , sino también para reducir la cantidad de creación de paletas, la instalación y la eliminación necesarias.

Por último, el representador de vídeo también podría detectar que el tamaño del vídeo ha cambiado, en cuyo caso debe enviar la notificación de [**cambio de tamaño de vídeo de EC \_ \_ \_**](ec-video-size-changed.md) . Una aplicación podría usar esta notificación para negociar el espacio en un documento compuesto. Las dimensiones de vídeo reales están disponibles a través de la interfaz de control [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Los representadores de DirectShow detectan si el vídeo ha cambiado de tamaño o no antes de enviar estos eventos.

## <a name="handling-persistent-properties"></a>Controlar propiedades persistentes

Todas las propiedades que se establecen a través de las interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) y [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) están pensadas para ser persistentes entre conexiones. Por lo tanto, desconectar y volver a conectar un representador no debe mostrar ningún efecto en el tamaño, la posición o los estilos de la ventana. Sin embargo, si las dimensiones de vídeo cambian entre las conexiones, el representador debe restablecer los rectángulos de origen y de destino a sus valores predeterminados. Las posiciones de origen y destino se establecen a través de la interfaz **IBasicVideo** .

Tanto [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) como [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) proporcionan un acceso suficiente a las propiedades para permitir que una aplicación guarde y restaure todos los datos de la interfaz en un formato persistente. Esto resultará útil para las aplicaciones que deben guardar la configuración exacta y las propiedades de los gráficos de filtros durante una sesión de edición y restaurarlos más adelante.

## <a name="handling-ec_repaint-notifications"></a>Control de \_ notificaciones de REpintar de EC

La notificación de [**\_ Repaint de EC**](ec-repaint.md) solo se envía cuando el representador está en pausa o detenido. Esta notificación indica al administrador de gráficos de filtro que el representador necesita datos. Si el gráfico de filtros se detiene cuando recibe una de estas notificaciones, pausará el gráfico de filtros, esperará a que todos los filtros reciban datos (mediante una llamada a [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)) y, a continuación, lo detendrán de nuevo. Cuando se detiene, un representador de vídeo debe conservar la imagen para que se puedan controlar los mensajes de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) posteriores.

Por lo tanto, si un representador de vídeo recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) cuando está detenido o en pausa, y no tiene nada con el que pintar su ventana, debe enviar el redibujo de EC al administrador de gráficos de filtro. [**\_**](ec-repaint.md) Si se recibe una notificación de **\_ repintar de EC** mientras está en pausa, el administrador de gráficos de filtros llama a [**IMediaPosition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) con la posición actual (es decir, busca en la posición actual). Esto hace que los filtros de origen vacíen el gráfico de filtro y hace que se envíen nuevos datos a través del gráfico de filtro.

Un representador solo debe enviar una de estas notificaciones a la vez. Por lo tanto, una vez que el representador envía una notificación, debe asegurarse de que no se envíen más hasta que se entreguen algunos ejemplos. La manera convencional de hacerlo es tener una marca para indicar que se puede enviar un recorte, que se desactiva después de enviar una notificación de [**\_ repintar de EC**](ec-repaint.md) . Esta marca debe restablecerse una vez que se entreguen los datos o cuando se vacíe el PIN de entrada, pero no si el final de la secuencia se señala en el PIN de entrada.

Si el representador no supervisa sus notificaciones de [**\_ Repaint de EC**](ec-repaint.md) , desbordará el administrador de gráficos de filtro con solicitudes de **\_ repintar de EC** (que son relativamente costosas de procesar). Por ejemplo, si un representador no tiene ninguna imagen para dibujar y se arrastra otra ventana por la ventana del representador en una operación de arrastre completo, el representador recibe varios mensajes de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) . Solo el primero de ellos debe generar una notificación de evento de **EC \_ Repaint** desde el representador al administrador de gráficos de filtro.

Un representador debe enviar su PIN de entrada como primer parámetro a la notificación de [**\_ Repaint de EC**](ec-repaint.md) . Al hacerlo, se consultará la clavija de salida adjunta para [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)y, si se admite, la notificación de **\_ repintar de EC** se enviará en primer lugar. Esto permite que los pin de salida controlen los retoques antes de que se deba tocar el gráfico de filtro. Esto no se realizará si el gráfico de filtros se detiene, porque no hay ningún búfer disponible en el asignador de representador desasignado.

Si el PIN de salida no puede controlar la solicitud y el gráfico de filtros se está ejecutando, se omite la notificación de [**\_ repintar de EC**](ec-repaint.md) . Un PIN de salida debe devolver **S \_ OK** desde [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) para indicar que ha procesado la solicitud Repaint correctamente. Se llamará al pin de salida en el subproceso de trabajo del administrador de gráficos de filtro, lo que evita que el representador llame directamente al pin de salida y, por tanto, evita cualquier problema de interbloqueo. Si el gráfico de filtro está detenido o en pausa y la salida no controla la solicitud, se realiza el procesamiento predeterminado.

## <a name="handling-notifications-in-full-screen-mode"></a>Control de notificaciones en modo de Full-Screen

El distribuidor de complementos de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) del gráfico de filtros administra la reproducción a pantalla completa. Cambiará un representador de vídeo para un representador de pantalla completa especialista, ajustará una ventana de un representador a la pantalla completa o hará que el representador implemente directamente la reproducción de pantalla completa. Para interactuar en los protocolos de pantalla completa, un representador de vídeo debe enviar una notificación de [**\_ activación de EC**](ec-activate.md) siempre que su ventana esté activada o desactivada. En otras palabras, se debe enviar una notificación de **\_ activación de EC** para cada mensaje de ACTIVATEAPP de WM que \_ reciba un representador.

Cuando se usa un representador en el modo de pantalla completa, estas notificaciones administran el cambio dentro y fuera del modo de pantalla completa. La desactivación de la ventana suele producirse cuando un usuario presiona ALT + TAB para cambiar a otra ventana, que el representador de pantalla completa de DirectShow usa como indicación para volver al modo de representación típico.

Cuando se envía la notificación de [**\_ activación de EC**](ec-activate.md) al administrador de gráficos de filtros al desactivar el modo de pantalla completa, el administrador de gráficos de filtros envía una notificación de [**\_ \_ pérdida de pantalla completa de EC**](ec-fullscreen-lost.md) a la aplicación de control. La aplicación podría usar esta notificación para restaurar el estado de un botón de pantalla completa, por ejemplo. DirectShow usa internamente las notificaciones de **\_ activación de EC** para administrar el cambio de pantalla completa de las pilas de los representadores de vídeo.

## <a name="summary-of-notifications"></a>Resumen de notificaciones

En esta sección se enumeran las notificaciones de gráficos de filtro que puede enviar un representador.



| Notificación de evento                                        | Descripción                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**activación de EC \_**](ec-activate.md)                       | Lo envían los representadores de vídeo en el modo de representación de pantalla completa para cada mensaje de ACTIVATEAPP de WM \_ recibido.                                                                                                  |
| [**EC \_ completado**](ec-complete.md)                       | Lo envían los representadores una vez representados todos los datos.                                                                                                                                               |
| [**visualización de EC \_ \_ modificada**](ec-display-changed.md)        | Lo envían los representadores de vídeo cuando cambia el formato de presentación.                                                                                                                                            |
| [**paleta de EC \_ \_ modificada**](ec-palette-changed.md)        | Se envía cuando un representador de vídeo detecta un cambio de paleta en la secuencia.                                                                                                                            |
| [**repintar EC \_**](ec-repaint.md)                         | Enviado por representadores de vídeo detenidos o en pausa cuando \_ se recibe un mensaje de pintura de WM y no hay datos para mostrar. Esto hace que Filter Graph Manager genere un marco para pintar en la pantalla. |
| [**USERABORT de EC \_**](ec-userabort.md)                     | Lo envían los representadores de vídeo para indicar un cierre que el usuario solicitó (por ejemplo, un usuario que cierra la ventana de vídeo).                                                                               |
| [**tamaño de vídeo de EC \_ \_ \_ cambiado**](ec-video-size-changed.md) | Lo envían los representadores de vídeo siempre que se detecta un cambio en el tamaño de vídeo nativo.                                                                                                                       |
| [**ventana de EC \_ \_ destruida**](ec-window-destroyed.md)      | Lo envían los representadores de vídeo cuando se quita o se destruye el filtro para que los recursos que dependen del foco de ventana se puedan pasar a otros filtros.                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de representadores de vídeo](writing-video-renderers.md)
</dt> </dl>

 

 
