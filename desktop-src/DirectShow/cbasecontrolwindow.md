---
description: La clase CBaseControlWindow implementa la interfaz IVideoWindow y controla el acceso externo a su filtro asociado.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: CBaseControlWindow (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: c4b53cc5ce1b209cc7de9d68648b68096e5c4911
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361408"
---
# <a name="cbasecontrolwindow-class"></a>CBaseControlWindow (clase)

![cbasecontrolwindow (jerarquía de clases)](images/wctrl01.png)

La **clase CBaseControlWindow** implementa la [**interfaz IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y controla el acceso externo a su filtro asociado. Debe sincronizar el objeto **CBaseControlWindow** con el filtro pasando un puntero a un objeto de sincronización de sección crítica. La **clase CBaseControlWindow proporciona** una serie de métodos que devuelven la configuración de propiedades sin tratar con esta sección crítica. Por ejemplo, llamar [**a CBaseControlWindow::get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) para recuperar el valor del miembro de datos **m \_ bAutoShow** bloquea la sección crítica. Sin embargo, es posible que el filtro ya tenga una sección crítica interna bloqueada, lo que podría infringir la jerarquía de bloqueos del filtro. En su lugar, al llamar a la función miembro [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) se devuelve el valor necesario sin que ello afecte a la sección crítica.

Todos los métodos [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementados por **CBaseControlWindow** requieren que el filtro se conecte correctamente con su filtro ascendente. Por este motivo, los objetos de clase requieren un pin de sincronización, que se establece mediante una llamada al [**método CBaseControlWindow::SetControlWindowPin.**](cbasecontrolwindow-setcontrolwindowpin.md) Cada vez que se llama a **un método IVideoWindow,** el objeto **CBaseControlWindow** comprueba que el pin sigue conectado.



| Miembros de datos protegidos                                                     | Descripción                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Resultado cuando cambia el estado.                                                                                                              |
| m \_ bCursorHidden                                                           | Determinación de si el cursor se muestra u oculta.                                                                                 |
| m \_ BorderColour                                                            | Color del borde de la ventana actual.                                                                                                         |
| m \_ hwndDrain                                                               | Identificador de ventana en el que se publican los mensajes recibidos.                                                                                        |
| m \_ hwndOwner                                                               | Ventana propietaria.                                                                                                                              |
| m \_ pFilter                                                                 | Puntero al filtro de medios propietario.                                                                                                         |
| m \_ pInterfaceLock                                                          | Sección crítica definida externamente.                                                                                                        |
| m \_ pPin                                                                    | Control de los tipos de medios para la conexión.                                                                                                  |
| Funciones de miembro                                                           | Descripción                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Construye un **objeto CBaseControlWindow.**                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera los estilos de ventana típicos o extendidos.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Establece los estilos de ventana típicos o extendidos.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Recupera el color del borde actual. Se trata de una función miembro del asistente.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera la ventana propietaria. Se trata de una función miembro del asistente.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera el estado actual del miembro de datos **m \_ bCursorHidden** sin bloquear la sección crítica. Se trata de una función miembro del asistente. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribuye los mensajes a la ventana primaria.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica al objeto del pin al que se aplica.                                                                                         |
| Métodos IVideoWindow                                                       | Descripción                                                                                                                                 |
| [**get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md)                   | Recupera la configuración actual de la marca AutoShow.                                                                                                |
| [**get \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera la paleta realizada en la marca de fondo.                                                                                      |
| [**get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera el color del borde actual.                                                                                                         |
| [**get \_ Caption**](cbasecontrolwindow-get-caption.md)                     | Recupera el título de la ventana actual.                                                                                                       |
| [**get \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera el modo de pantalla completa actual.                                                                                                     |
| [**get \_ Height**](cbasecontrolwindow-get-height.md)                       | Recupera el alto actual de la ventana.                                                                                                        |
| [**get \_ Left**](cbasecontrolwindow-get-left.md)                           | Recupera la coordenada de la ventana izquierda actual.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera el tamaño máximo de la imagen ideal.                                                                                              |
| [**get \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera la purga del mensaje actual.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera el tamaño mínimo de la imagen ideal.                                                                                              |
| [**get \_ Owner**](cbasecontrolwindow-get-owner.md)                         | Recupera el identificador de ventana primaria.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera la posición en la que se restaurará la ventana cuando se maximice o minimice.                                                    |
| [**get \_ Top**](cbasecontrolwindow-get-top.md)                             | Recupera la coordenada Y de la parte superior de la ventana.                                                                                       |
| [**obtener \_ visible**](cbasecontrolwindow-get-visible.md)                     | Recupera la configuración de visibilidad actual de la ventana.                                                                                     |
| [**get \_ Width**](cbasecontrolwindow-get-width.md)                         | Recupera el ancho de la ventana.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera las coordenadas de ventana actuales.                                                                                                   |
| [**get \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Recupera el estado actual de la ventana.                                                                                                  |
| [**get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera los estilos de ventana estándar.                                                                                                       |
| [**get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera los estilos de ventana extendidos.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Oculta o muestra el cursor.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera el estado actual del miembro de datos **\_ m bCursorHidden.**                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Pasa los mensajes que se envían a las ventanas propietarias.                                                                                         |
| [**put \_ AutoShow**](cbasecontrolwindow-put-autoshow.md)                   | Establece la propiedad AutoShow.                                                                                                                 |
| [**put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Establece una marca para realizar la paleta en segundo plano.                                                                                       |
| [**put \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Establece el color del borde actual.                                                                                                              |
| [**put \_ Caption**](cbasecontrolwindow-put-caption.md)                     | Establece el título de la ventana actual.                                                                                                            |
| [**put \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Establece el modo de pantalla completa.                                                                                                                  |
| [**put \_ Height**](cbasecontrolwindow-put-height.md)                       | Establece el alto actual de la ventana.                                                                                                             |
| [**put \_ Left**](cbasecontrolwindow-put-left.md)                           | Establece la coordenada izquierda de la ventana.                                                                                                    |
| [**put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Establece la ventana de purga del mensaje.                                                                                                              |
| [**put \_ Owner**](cbasecontrolwindow-put-owner.md)                         | Establece el identificador de ventana principal de Microsoft Win32.                                                                                              |
| [**put \_ Top**](cbasecontrolwindow-put-top.md)                             | Establece la posición de la parte superior de la ventana.                                                                                                |
| [**put \_ Visible**](cbasecontrolwindow-put-visible.md)                     | Oculta o muestra la ventana.                                                                                                                  |
| [**put \_ Width**](cbasecontrolwindow-put-width.md)                         | Establece el ancho de la ventana.                                                                                                               |
| [**put \_ WindowState**](cbasecontrolwindow-put-windowstate.md)             | Establece el estado de la ventana.                                                                                                               |
| [**put \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md)             | Establece los estilos de ventana estándar.                                                                                                            |
| [**put \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Establece los estilos de ventana extendidos.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Establece la ventana en primer plano.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Establece la posición de la ventana.                                                                                                                   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 



