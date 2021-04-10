---
description: La clase CBaseControlWindow implementa la interfaz IVideoWindow y controla el acceso externo a su filtro asociado.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: Clase CBaseControlWindow
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
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274753"
---
# <a name="cbasecontrolwindow-class"></a>Clase CBaseControlWindow

![jerarquía de clases cbasecontrolwindow](images/wctrl01.png)

La clase **CBaseControlWindow** implementa la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y controla el acceso externo a su filtro asociado. Debe sincronizar el objeto **CBaseControlWindow** con el filtro pasándole un puntero a un objeto de sincronización de sección crítica. La clase **CBaseControlWindow** proporciona una serie de métodos que devuelven valores de propiedad sin tratar con esta sección crítica. Por ejemplo, al llamar a [**CBaseControlWindow:: get \_ Autoshow**](cbasecontrolwindow-get-autoshow.md) para recuperar el valor del miembro de datos **m \_ bAutoShow** se bloquea la sección crítica. No obstante, es posible que el filtro tenga una sección crítica interna bloqueada, que podría infringir la jerarquía de bloqueo del filtro. En su lugar, al llamar a la función miembro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) se devuelve el valor necesario sin que ello afecte a la sección crítica.

Todos los métodos [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implementados de **CBaseControlWindow** requieren que el filtro se conecte correctamente con su filtro de nivel superior. Por este motivo, los objetos de clase requieren un PIN de sincronización, que se establece mediante una llamada al método [**CBaseControlWindow:: SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md) . Siempre que se llama a un método **IVideoWindow** , el objeto **CBaseControlWindow** comprueba que el PIN todavía está conectado.



| Miembros de datos protegidos                                                     | Descripción                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Resultado cuando cambia el estado.                                                                                                              |
| m \_ bCursorHidden                                                           | Determinación de si el cursor se muestra o se oculta.                                                                                 |
| m \_ BorderColour                                                            | Color del borde de la ventana actual.                                                                                                         |
| m \_ hwndDrain                                                               | Identificador de ventana en el que se envían los mensajes recibidos.                                                                                        |
| m \_ hwndOwner                                                               | Ventana propietaria.                                                                                                                              |
| m \_ pFilter                                                                 | Puntero al filtro multimedia propietario.                                                                                                         |
| m \_ pInterfaceLock                                                          | Sección crítica definida externamente.                                                                                                        |
| m \_ pPin                                                                    | Control de los tipos de medios para la conexión.                                                                                                  |
| Funciones de miembro                                                           | Descripción                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Construye un objeto **CBaseControlWindow** .                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Recupera los estilos de ventana típicos o extendidos.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Establece los estilos de ventana típicos o extendidos.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Recupera el color del borde actual. Se trata de una función miembro auxiliar.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Recupera la ventana propietaria. Se trata de una función miembro auxiliar.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera el estado actual del miembro de datos **m \_ bCursorHidden** sin bloquear la sección crítica. Se trata de una función miembro auxiliar. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribuye los mensajes a la ventana primaria.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Notifica al objeto del PIN al que se aplica.                                                                                         |
| Métodos IVideoWindow                                                       | Descripción                                                                                                                                 |
| [**obtener \_ Automostrar**](cbasecontrolwindow-get-autoshow.md)                   | Recupera la configuración de la marca de Automostrar actual.                                                                                                |
| [**obtener \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Recupera la paleta realizada en la marca de fondo.                                                                                      |
| [**obtener \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Recupera el color del borde actual.                                                                                                         |
| [**obtener \_ título**](cbasecontrolwindow-get-caption.md)                     | Recupera el título de la ventana actual.                                                                                                       |
| [**obtener \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Recupera el modo de pantalla completa actual.                                                                                                     |
| [**obtener \_ alto**](cbasecontrolwindow-get-height.md)                       | Recupera el alto de la ventana actual.                                                                                                        |
| [**obtener a la \_ izquierda**](cbasecontrolwindow-get-left.md)                           | Recupera la coordenada de la ventana izquierda actual.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Recupera el tamaño máximo de la imagen ideal.                                                                                              |
| [**obtener \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Recupera la purga del mensaje actual.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Recupera el tamaño mínimo de la imagen ideal.                                                                                              |
| [**obtener \_ propietario**](cbasecontrolwindow-get-owner.md)                         | Recupera el identificador de la ventana primaria.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Recupera la posición en la que se restaurará la ventana al maximizar o minimizar.                                                    |
| [**obtener la \_ parte superior**](cbasecontrolwindow-get-top.md)                             | Recupera la coordenada y de la parte superior de la ventana.                                                                                       |
| [**obtener \_ visible**](cbasecontrolwindow-get-visible.md)                     | Recupera la configuración de visibilidad actual de la ventana.                                                                                     |
| [**obtener \_ ancho**](cbasecontrolwindow-get-width.md)                         | Recupera el ancho de la ventana.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Recupera las coordenadas de la ventana actual.                                                                                                   |
| [**obtener \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Recupera el estado actual de la ventana.                                                                                                  |
| [**obtener \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Recupera los estilos de ventana estándar.                                                                                                       |
| [**obtener \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Recupera los estilos extendidos de ventana.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Oculta o muestra el cursor.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Recupera el estado actual del miembro de datos **m \_ bCursorHidden** .                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Pasa los mensajes que se envían a las ventanas propietarias.                                                                                         |
| [**poner \_ Automostrar**](cbasecontrolwindow-put-autoshow.md)                   | Establece la propiedad de Automostrar.                                                                                                                 |
| [**Put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Establece una marca para obtener la paleta en segundo plano.                                                                                       |
| [**poner \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Establece el color del borde actual.                                                                                                              |
| [**poner \_ título**](cbasecontrolwindow-put-caption.md)                     | Establece el título de la ventana actual.                                                                                                            |
| [**Put \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Establece el modo de pantalla completa.                                                                                                                  |
| [**colocar \_ alto**](cbasecontrolwindow-put-height.md)                       | Establece el alto de la ventana actual.                                                                                                             |
| [**colocar a la \_ izquierda**](cbasecontrolwindow-put-left.md)                           | Establece la coordenada izquierda de la ventana.                                                                                                    |
| [**Put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Establece la ventana de purga de mensajes.                                                                                                              |
| [**colocar \_ propietario**](cbasecontrolwindow-put-owner.md)                         | Establece el identificador de ventana primaria de Microsoft Win32.                                                                                              |
| [**colocar \_ arriba**](cbasecontrolwindow-put-top.md)                             | Establece la posición de la parte superior de la ventana.                                                                                                |
| [**poner \_ visibles**](cbasecontrolwindow-put-visible.md)                     | Oculta o muestra la ventana.                                                                                                                  |
| [**colocar \_ ancho**](cbasecontrolwindow-put-width.md)                         | Establece el ancho de la ventana.                                                                                                               |
| [**colocar \_ WindowState**](cbasecontrolwindow-put-windowstate.md)             | Establece el estado de la ventana.                                                                                                               |
| [**poner \_ estiloVentana**](cbasecontrolwindow-put-windowstyle.md)             | Establece los estilos de ventana estándar.                                                                                                            |
| [**Put \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Establece los estilos extendidos de ventana.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Establece la ventana en primer plano.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Establece la posición de la ventana.                                                                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



