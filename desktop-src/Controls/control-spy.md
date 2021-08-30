---
title: Control Spy v2.0
description: Control Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes sobre cómo aplicarles estilos y cómo responden a mensajes y notificaciones.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32ad668ff1ac5912db67f48a99b31de8df09dfd417f4058ee4ff2dacfb55421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920991"
---
# <a name="control-spy-v20"></a>Control Spy v2.0

Control Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes: cómo aplicarles estilos y cómo responden a mensajes y notificaciones. Con Control Spy, puede ver inmediatamente cómo afectan los distintos estilos al comportamiento y la apariencia de cada control, así como cómo puede cambiar el estado de cada control mediante el envío de mensajes.

Hay disponibles dos versiones de Control Spy, una para [Comctl32.dll versión 5.x](common-control-versions.md) y otra para Comctl32.dll versión 6.0 y posteriores. ControlSpyV6.exe tiene un manifiesto de aplicación integrado para que use los controles con estilo más recientes. ControlSpyV5.exe no tiene este manifiesto, por lo que el valor predeterminado es la versión anterior.

En este tema se incluyen las siguientes secciones.

-   [Información general](#overview)
-   [Estilos](#styles)
-   [Mensajes](#messages)
-   [Tamaño/Color](#sizecolor)
-   [Dónde obtener Control Spy](#where-to-get-control-spy)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Control Spy hospeda un control común seleccionado en el centro de su ventana de aplicación. Para cambiar el control que se muestra, seleccione diferentes controles en el cuadro de lista del lado izquierdo de la ventana. Los mensajes o notificaciones recibidos por el control se mostrarán en el lado derecho de la ventana cuando lleguen. Puede habilitar o deshabilitar esta funcionalidad mediante las casillas **Mensajes recibidos** y **Notificaciones recibidas.**

En la imagen siguiente se muestra la aplicación Control Spy.

![ventana de spy de control](images/controlspy-main.png)

En la parte inferior de la ventana, hay varias pestañas que presentan más funcionalidad.

## <a name="styles"></a>Estilos

La **pestaña** Estilos permite cambiar el estilo de ventana actual del control. Seleccione o anule la selección de cualquiera de los estilos enumerados y, a continuación, haga clic en el botón **Aplicar** para cambiar el estilo del control mostrado. Como alternativa, puede usar el botón **Volver** a crear para crear un nuevo control con los estilos seleccionados. El **botón** Restablecer devolverá el control a los estilos predeterminados.

Los **botones Copy Style** (Estilo de copia) y Copy **ExStyle** (Copiar estilo) situados debajo de la pestaña copiarán las constantes de estilo seleccionadas en el Portapapeles como una lista delimitada bit a bit OR ( \| ). Puede pegar esta lista directamente en la llamada a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para proporcionar un control en su propia aplicación con el mismo estilo.

En la imagen siguiente se muestra **la pestaña Estilos** de un control de botón.

![pestaña de estilos de spy de control](images/controlspy-styles.png)

## <a name="messages"></a>error de Hadoop

La **pestaña** Mensajes permite enviar casi cualquier mensaje a un control . Después de seleccionar un mensaje en el cuadro de lista, puede especificar los datos que se envían como los parámetros *wParam* y *lParam* de la llamada a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Después de hacer **clic en Enviar**, el mensaje se envía al control y cualquier resultado se muestra en el cuadro de texto de la parte inferior de la pestaña.

En la imagen siguiente se muestra la pestaña mensajes cuando se selecciona un mensaje determinado.

![pestaña controlar mensajes de espionaje](images/controlspy-messages.png)

## <a name="sizecolor"></a>Tamaño/Color

La **pestaña Tamaño/Color** se puede usar para cambiar el tamaño del control, así como el color de su fondo.

## <a name="where-to-get-control-spy"></a>Dónde obtener Control Spy

Puede descargar [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) desde MSDN. Ambas versiones están contenidas en la descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Controles](window-controls.md)
</dt> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> </dl>

 

 