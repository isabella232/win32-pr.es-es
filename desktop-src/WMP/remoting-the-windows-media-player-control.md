---
title: Control remoto del Reproductor de Windows Media
description: Control remoto del Reproductor de Windows Media
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, control remoto de ActiveX
- Modelo de objetos de Windows Media Player, control remoto de controles ActiveX
- modelo de objetos, control remoto de controles ActiveX
- Windows Media Player Mobile, control ActiveX remoto
- Control ActiveX de Windows Media Player, comunicación remota
- Control ActiveX móvil de Windows Media Player, comunicación remota
- Control ActiveX, comunicación remota
- control ActiveX de Windows Media Player remoto
- incrustación, control ActiveX remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077443"
---
# <a name="remoting-the-windows-media-player-control"></a>Control remoto del Reproductor de Windows Media

Al incrustar el control Media Player de Windows en un programa de C++, puede usarlo como una extensión remota del modo completo del reproductor. Esto se denomina "comunicación remota" del control de Media Player de Windows y le permite proporcionar todas las características del reproductor en modo completo sin implementarlas usted mismo.

Cuando el control se realiza de forma remota, comparte el mismo motor de reproducción que el modo completo del reproductor y los usuarios pueden alternar entre el modo incrustado (el estado "acoplado") y el modo completo (el estado "desacoplado") mientras la reproducción multimedia digital continúa sin interrupciones.

## <a name="enabling-remote-embedding"></a>Habilitar la inserción remota

Para habilitar la inserción remota del control de Media Player de Windows, el programa debe implementar las interfaces **IServiceProvider** y [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) . **IServiceProvider** es una interfaz estándar del modelo de objetos componentes (com) con un único método denominado **QueryService**. Windows Media Player llama a este método para recuperar un puntero a una interfaz **IWMPRemoteMediaServices** .

**IWMPRemoteMediaServices** tiene varios métodos, pero solo dos de ellos son directamente relevantes para la comunicación remota. En [GetApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname), se devuelve el nombre del programa, que Windows Media Player agrega a la lista **cambiar a otro programa** del menú **Ver** . En [GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype), se indica el modo de inserción del control devolviendo un valor de "Remote" o "local". Si se establece una conexión remota correctamente, el método [Get \_ isRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) de la interfaz [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) devuelve true.

## <a name="specifying-an-exclusive-online-store"></a>Especificación de una tienda en línea exclusiva

Con Windows Media Player 11, una aplicación que incrusta el control del reproductor de forma remota puede especificar una tienda en línea exclusiva. En ese caso, el selector de servicio de Windows Media Player está deshabilitado y solo la tienda en línea especificada está disponible para el usuario. Para obtener información detallada sobre cómo especificar una tienda en línea exclusiva, consulte [tiendas en línea exclusivas](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Acoplar y desacoplar

La interfaz **IWMPPlayer4** también proporciona acceso a la interfaz [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) a través del método [Get \_ playerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) . Use **IWMPPlayerApplication** para cambiar entre los Estados acoplado y desacoplado y para determinar el estado acoplado actual y la ubicación del vídeo o visualización de la visualización.

El método [IWMPPlayerApplication:: switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) desacopla el control abriendo el modo completo de Windows Media Player y transfiriendo la presentación de vídeo o visualización al panel **reproducción en curso** . El método [IWMPPlayerApplication:: switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) acopla el control transfiriendo la presentación de vídeo o de visualización al programa y cerrando el modo completo del reproductor, si está abierto. El control también se puede acoplar seleccionando un programa de la lista **cambiar a otro programa** o cerrando el modo completo del reproductor. En ambos casos, los medios digitales que se reproducen continúan ininterrumpidos.

## <a name="transferring-the-video-or-visualization-display"></a>Transferir la presentación de vídeo o visualización

Cuando se ejecutan simultáneamente varios programas con controles de Media Player de Windows incrustados y remotos, todos los controles comparten el mismo motor de reproducción. También comparten la misma instancia del modo completo del reproductor en el estado desacoplado. En el estado acoplado, sin embargo, solo un control puede mostrar el vídeo o la visualización. En el estado desacoplado, solo el modo completo del reproductor muestra el vídeo o la visualización. El método **switchToControl** funciona en los Estados acoplado y desacoplado, y transferirá el vídeo o la visualización a cualquier programa que lo llame.

La única diferencia entre los Estados acoplado y desacoplado es la presencia del modo completo de Windows Media Player y su propiedad de la pantalla de vídeo o visualización. En el estado desacoplado, todos los controles incrustados y remotos que se están ejecutando actualmente siguen siendo visibles y sus interfaces de usuario siguen siendo totalmente funcionales. Sin embargo, si hay una ventana de vídeo o de visualización, está vacía. En el estado acoplado, solo uno de los controles incrustados remotos es el propietario de la presentación, pero todas las interfaces de usuario continúan funcionando.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Ocultar o cambiar el control en el estado desacoplado

Debe proporcionar su propia implementación si desea ocultar o modificar la interfaz de usuario de un control incrustado en el estado desacoplado o si el programa no es el propietario de la pantalla. Puede hacer estas modificaciones al acoplar y desacoplar el control, o puede hacer que sean respuesta a eventos de Windows Media Player. No obstante, dado que el reproductor se puede acoplar a través de la opción de menú **cambiar a otro programa** , normalmente es mejor proporcionar esta funcionalidad en respuesta a eventos.

Puede implementar controladores de eventos para los eventos [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) y [SwitchedToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) , o puede implementar un único controlador de eventos para el evento [PlayerDockedStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) . En el último caso, puede determinar el estado acoplado mediante una llamada a [IWMPPlayerApplication:: get \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked). En ambos casos, use [IWMPPlayerApplication:: get \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) para determinar si el programa es el propietario de la presentación de vídeo o de visualización.

## <a name="re-establishing-a-remote-connection"></a>Volver a establecer una conexión remota

En determinadas circunstancias, se producirá un error en la conexión entre un control incrustado remoto y el reproductor independiente, invalidando los punteros a las interfaces de Windows Media Player. Windows Media Player intentará volver a conectarse automáticamente y desencadenará el evento [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) para indicar este intento. Aunque la reconexión sea automática, debe proporcionar un controlador de eventos para este evento si desea liberar los punteros no válidos y recuperar otros nuevos para poder tener acceso al reproductor independiente a través de la nueva conexión.

## <a name="controlling-the-undocked-player"></a>Controlar el reproductor desacoplado

Todas las instancias remotas del control de Media Player de Windows pueden manipular el modo completo del reproductor independientemente del estado acoplado. Sin embargo, las características que no tienen ninguna relevancia para el modo completo del reproductor se omiten hasta que el control de Media Player de Windows esté acoplado. Esto incluye las propiedades de [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) y las interfaces derivadas, como **Enabled**, **enableContextMenu**, **uiMode** y **windowlessVideo**.

## <a name="error-dialog-boxes"></a>Cuadros de diálogo de error

En una instancia de control de Windows Media Player remota, la *configuración*. la propiedad **enableErrorDialogs** se comporta de una manera determinada. Se aplican las reglas siguientes:

-   Cuando Windows Media Player está desacoplado (la interfaz de usuario de Windows Media Player está visible), se omite la propiedad **enableErrorDialogs** y el reproductor controla los cuadros de diálogo de error.
-   Cuando Windows Media Player está acoplado, el valor especificado por cada instancia remota del control para **enableErrorDialogs** solo se aplica a la instancia de control individual. Es decir, si una instancia de control determinada especifica un valor de "true" para **enableErrorDialogs**, solo esa instancia mostrará un cuadro de diálogo cuando se produzca un error si todas las demás instancias del control han especificado el valor "false".

## <a name="remoting-in-the-background"></a>Comunicación remota en segundo plano

Debe evitar que una instancia remota del reproductor se ejecute en segundo plano en los momentos en los que el control no está en uso. Dado que la instancia de control del reproductor remoto comparte su motor de reproducción con el reproductor en modo completo, mantener una instancia en segundo plano en ejecución puede producir un comportamiento inesperado. Por ejemplo, el usuario puede cerrar el reproductor en modo completo mientras se reproduce un archivo. El usuario esperaría que la reproducción de archivos se detuviera por completo cuando el jugador se cerrara, pero es posible que el audio continúe reproduciéndose porque el motor de reproducción todavía está activo.

## <a name="samples"></a>Ejemplos

El paquete de instalación de Windows Media Player SDK instala ejemplos que muestran la comunicación remota. Vea los ejemplos de RemoteSkin y WMPML para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




