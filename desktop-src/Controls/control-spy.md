---
title: Controlar Spy v 2.0
description: Controlar Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes sobre cómo aplicarles estilos y cómo responden a los mensajes y las notificaciones.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078536"
---
# <a name="control-spy-v20"></a>Controlar Spy v 2.0

Controlar Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes: Cómo aplicarles estilos y cómo responden a los mensajes y las notificaciones. Con control Spy, puede ver inmediatamente el modo en que los distintos estilos afectan al comportamiento y la apariencia de cada control y también cómo puede cambiar el estado de cada control mediante el envío de mensajes.

Hay disponibles dos versiones de control Spy, una para [Comctl32.dll versión 5. x](common-control-versions.md) y otra para Comctl32.dll versión 6,0 y posteriores. ControlSpyV6.exe tiene un manifiesto de aplicación integrado para que use los controles con control de versiones más recientes. ControlSpyV5.exe no tiene este manifiesto y, de forma predeterminada, es la versión anterior.

En este tema se incluyen las siguientes secciones.

-   [Información general](#overview)
-   [Estilos](#styles)
-   [Mensajes](#messages)
-   [Tamaño/color](#sizecolor)
-   [Dónde obtener el control Spy](#where-to-get-control-spy)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Control Spy hospeda un control común seleccionado en el centro de la ventana de la aplicación. Puede cambiar el control que se muestra seleccionando distintos controles en el cuadro de lista en el lado izquierdo de la ventana. Los mensajes o las notificaciones recibidas por el control se mostrarán en la parte derecha de la ventana cuando lleguen. Puede habilitar o deshabilitar esta funcionalidad mediante las casillas **mensajes recibidos** y **notificaciones recibidas** .

En la imagen siguiente se muestra la aplicación control Spy.

![ventana controlar Spy](images/controlspy-main.png)

En la parte inferior de la ventana, hay varias pestañas que presentan más funcionalidad.

## <a name="styles"></a>Estilos

La pestaña **estilos** permite cambiar el estilo de ventana actual del control. Seleccione o anule la selección de cualquiera de los estilos de la lista y, a continuación, haga clic en el botón **aplicar** para cambiar el estilo del control mostrado. Como alternativa, puede usar el botón **volver a crear** para crear un nuevo control con los estilos seleccionados. El botón **restablecer** devolverá el control a los estilos predeterminados.

Los botones **copiar estilo** y **copiar** estilo que se encuentran debajo de la ficha copiarán las constantes de estilo seleccionadas en el portapapeles como una lista delimitada OR bit a bit ( \| ). Puede pegar esta lista directamente en la llamada a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para proporcionar un control en su propia aplicación con el mismo estilo.

En la imagen siguiente se muestra la pestaña **estilos** de un control botón.

![controlar la pestaña de estilos de Spy](images/controlspy-styles.png)

## <a name="messages"></a>error de Hadoop

La pestaña **mensajes** le permite enviar casi cualquier mensaje a un control. Después de seleccionar un mensaje en el cuadro de lista, puede especificar los datos que se envían como los parámetros *wParam* y *lParam* de la llamada a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Después de hacer clic en **Enviar**, el mensaje se envía al control y los resultados se muestran en el cuadro de texto de la parte inferior de la pestaña.

La siguiente imagen muestra la ficha mensajes cuando se selecciona un mensaje determinado.

![pestaña controlar mensajes de Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a>Tamaño/color

La pestaña **tamaño/color** se puede usar para cambiar el tamaño del control y el color de fondo.

## <a name="where-to-get-control-spy"></a>Dónde obtener el control Spy

Puede descargar el [control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) de MSDN. Ambas versiones están contenidas en la descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Controles de Windows](window-controls.md)
</dt> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> </dl>

 

 