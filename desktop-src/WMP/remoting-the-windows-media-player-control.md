---
title: Control remoto del Reproductor de Windows Media
description: Control remoto del Reproductor de Windows Media
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media, control remoto ActiveX remoto
- Reproductor de Windows Media modelo de objetos, control remoto ActiveX control
- modelo de objetos, control ActiveX remoto
- Reproductor de Windows Media Móvil, control de ActiveX remoto
- Reproductor de Windows Media ActiveX control remoto, comunicación remota
- Reproductor de Windows Media Control ActiveX móvil, comunicación remota
- ActiveX control remoto, comunicación remota
- control de Reproductor de Windows Media ActiveX comunicación remota
- embedding,remoting ActiveX control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476202"
---
# <a name="remoting-the-windows-media-player-control"></a>Control remoto del Reproductor de Windows Media

Al insertar el control Reproductor de Windows Media en un programa de C++, puede usarlo como una extensión remota del modo completo del Reproductor. Esto se denomina "comunicación remota" Reproductor de Windows Media control y le permite proporcionar todas las características del reproductor en modo completo sin implementarlas usted mismo.

Cuando se remota el control, comparte el mismo motor de reproducción que el modo completo del reproductor y los usuarios pueden cambiar entre el modo incrustado (el estado "acoplado") y el modo completo (el estado "desacoplado") mientras la reproducción de medios digitales continúa sin interrupciones.

## <a name="enabling-remote-embedding"></a>Habilitación de la inserción remota

Para habilitar la inserción remota del control Reproductor de Windows Media, el programa debe implementar las interfaces **IServiceProvider** e [IWMPRemoteMediaServices.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) **IServiceProvider es** una interfaz de Modelo de objetos componentes (COM) estándar con un único método denominado **QueryService**. Reproductor de Windows Media llama a este método para recuperar un puntero a una **interfaz IWMPRemoteMediaServices.**

**IWMPRemoteMediaServices tiene varios métodos,** pero solo dos de ellos son directamente relevantes para la comunicación remota. En [GetApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname), devuelve el nombre del programa, que Reproductor de Windows Media agrega a la lista **Cambiar** a otro programa en el **menú** Ver. En [GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype), se indica el modo de inserción del control devolviendo un valor de "Remote" o "Local". Si se establece correctamente una conexión remota, el [método get \_ isRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) de la [interfaz IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) devuelve true.

## <a name="specifying-an-exclusive-online-store"></a>Especificar una tienda en línea exclusiva

Con Reproductor de Windows Media 11, una aplicación que inserta el control Player de forma remota puede especificar una tienda en línea exclusiva. En ese caso, el selector de servicios de Reproductor de Windows Media está deshabilitado y solo el usuario tiene disponible la tienda en línea especificada. Para obtener información detallada sobre cómo especificar una tienda en línea exclusiva, vea [Exclusive Online Stores](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Acoplamiento y desacoplamiento

La **interfaz IWMPPlayer4** también proporciona acceso a la [interfaz IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) mediante el [método get \_ playerApplication.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) Use **IWMPPlayerApplication** para cambiar entre los estados acoplado y desacoplado y para determinar el estado acoplado actual y la ubicación de la visualización o el vídeo.

El [método IWMPPlayerApplication::switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) desacopla el control abriendo el modo completo de Reproductor de Windows Media y transfiriendo el vídeo o la visualización al panel **Reproducción** ahora. El [método IWMPPlayerApplication::switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) acopla el control transfiriendo el vídeo o la visualización al programa y cerrando el modo completo del reproductor, si está abierto. El control también se puede acoplar seleccionando un programa en la lista Cambiar a otro programa o cerrando el modo completo del reproductor.  En ambos casos, los medios digitales que se reproducen continúan ininterrumpidos.

## <a name="transferring-the-video-or-visualization-display"></a>Transferencia de la pantalla de vídeo o visualización

Cuando varios programas con controles integrados y remotos Reproductor de Windows Media se ejecutan simultáneamente, todos los controles comparten el mismo motor de reproducción. También comparten la misma instancia del modo completo del reproductor en estado desacoplado. Sin embargo, en el estado acoplado, solo un control puede mostrar el vídeo o la visualización. En estado desacoplado, solo el modo completo del reproductor muestra el vídeo o la visualización. El **método switchToControl** funciona en los estados acoplado y desacoplado y transferirá el vídeo o la visualización a cualquier programa que lo llame.

La única diferencia entre los estados acoplados y desacoplados es la presencia del modo completo de Reproductor de Windows Media y su propiedad de la pantalla de vídeo o visualización. En el estado desacoplado, todos los controles remotos incrustados que se están ejecutando actualmente siguen siendo visibles y sus interfaces de usuario siguen siendo totalmente funcionales. Sin embargo, si hay un vídeo o una ventana de visualización, está vacío. En el estado acoplado, solo uno de los controles remotos incrustados posee la pantalla, pero todas las interfaces de usuario siguen funcionando.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Ocultar o cambiar el control en estado desacoplado

Debe proporcionar su propia implementación si desea ocultar o modificar la interfaz de usuario de un control incrustado en estado desacoplado o cuando el programa no posee la pantalla. Puede realizar estas modificaciones al acoplar y desacoplar el control, o bien puede realizarlas en respuesta a Reproductor de Windows Media eventos. Sin embargo, dado que  el reproductor se puede acoplar mediante la opción de menú Cambiar a otro programa, normalmente es mejor proporcionar esta funcionalidad en respuesta a eventos.

Puede implementar controladores de eventos para los eventos [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) y [SwitchedToControl,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) o puede implementar un único controlador de eventos para el evento [PlayerDockedStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) En el último caso, puede determinar el estado acoplado llamando a [IWMPPlayerApplication::get \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked). En ambos casos, use [IWMPPlayerApplication::get \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) para determinar si el programa posee la pantalla de vídeo o visualización.

## <a name="re-establishing-a-remote-connection"></a>Restablecimiento de una conexión remota

En determinadas circunstancias, se producirá un error en la conexión entre un control remoto insertado y el reproductor independiente, invalidando los punteros a las Reproductor de Windows Media independientes. Reproductor de Windows Media automáticamente intentará volver a conectarse y se activa el evento [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) para indicar este intento. Aunque la reconexión es automática, debe proporcionar un controlador de eventos para este evento si desea liberar los punteros no válidos y recuperar otros nuevos para poder acceder al reproductor independiente a través de la nueva conexión.

## <a name="controlling-the-undocked-player"></a>Controlar el reproductor desacoplado

Todas las instancias remotas del control Reproductor de Windows Media control pueden manipular el modo completo del reproductor independientemente del estado acoplado. Sin embargo, las características que no tienen relevancia para el modo completo del reproductor se omiten hasta que se acopla Reproductor de Windows Media control. Esto incluye las propiedades de [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) y las interfaces derivadas, como **enabled**, **enableContextMenu**, **uiMode** y **windowlessVideo**.

## <a name="error-dialog-boxes"></a>Cuadros de diálogo de error

Desde una instancia Reproductor de Windows Media control remoto, el *Configuración*. **La propiedad enableErrorDialogs** se comporta de una manera específica. Se aplican las reglas siguientes:

-   Cuando Reproductor de Windows Media está desacoplado (la interfaz de usuario de Reproductor de Windows Media está visible), se omite la propiedad **enableErrorDialogs** y el reproductor controla los cuadros de diálogo de error.
-   Cuando Reproductor de Windows Media está acoplado, el valor especificado por cada instancia remota del control para **enableErrorDialogs** solo se aplica a la instancia de control individual. Es decir, si una instancia de control determinada especifica un valor de "true" para **enableErrorDialogs**, solo esa instancia mostrará un cuadro de diálogo cuando se produzca un error si todas las demás instancias del control han especificado un valor de "false".

## <a name="remoting-in-the-background"></a>Comunicación remota en segundo plano

Debe evitar mantener una instancia remota del reproductor en ejecución en segundo plano durante los momentos en los que el control no está en uso. Dado que la instancia de control Player remota comparte su motor de reproducción con el reproductor en modo completo, mantener una instancia en segundo plano en ejecución puede provocar un comportamiento inesperado. Por ejemplo, el usuario podría cerrar el reproductor en modo completo mientras se reproduce un archivo. El usuario esperaría que la reproducción de archivos se detuviera completamente cuando se cierre el reproductor, pero es posible que el audio siga reproduciendo porque el motor de reproducción sigue activo.

## <a name="samples"></a>Ejemplos

El Reproductor de Windows Media de instalación del SDK instala ejemplos que muestran la comunicación remota. Consulte los ejemplos de RemoteSkin y WMPML para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Muestras**](samples.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




