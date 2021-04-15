---
title: Parámetros de la línea de comandos
description: Parámetros de la línea de comandos
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Media Player de Windows, parámetros
- Windows Media Player, parámetros de la línea de comandos
- Windows Media Player, wmplayer
- Media Player de Windows, Wmpconfig
- Media Player de Windows, wmpnscfg
- parámetros de la línea de comandos
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa65b686f8a746111a62bd6afcc3df280191c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695438"
---
# <a name="command-line-parameters"></a>Parámetros de la línea de comandos

## <a name="command-line-parameters-for-wmplayer"></a>Parámetros de línea de comandos para wmplayer

Windows Media Player admite un conjunto de parámetros de línea de comandos que especifican cómo se comporta el reproductor cuando se inicia. En la tabla siguiente se detallan los parámetros y sus comportamientos.



| Sintaxis                                                                                                              | Comportamiento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*\\ nombre de archivo de ruta de acceso*" (por ejemplo: `wmplayer "c:\filename.wma"` )<br/>                                            | Inicie el reproductor y reproduzca el archivo.                                                                                                                                                                                                                                                                                                        |
| "*\\ nombre de archivo de ruta de acceso*"/Fullscreen (por ejemplo: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Reproducir el archivo especificado en modo de pantalla completa. Debe especificar la ruta de acceso y el nombre de archivo del contenido que se va a reproducir.<br/>                                                                                                                                                                                                                     |
| /Device: {DVD \| audio * (por ejemplo: `wmplayer /device:audio CD` )<br/>                                         | Reproducir un CD de DVD o audio.                                                                                                                                                                                                                                                                                                                    |
| "*\\ nombre de archivo de ruta de acceso*? WMPSkin =*nombre* de la máscara "por ejemplo: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Abra el reproductor y aplique la máscara especificada.                                                                                                                                                                                                                                                                                              |
| /Service:*keyName*                                                                                                  | Abra el reproductor que muestra la tienda en línea especificada por *keyName*. Requiere Windows Media Player 10 o posterior.<br/>                                                                                                                                                                                                                      |
| /Secuencias NowPlaying                                                                                                    | Abra el reproductor en la característica **reproducción en curso** .                                                                                                                                                                                                                                                                                            |
| /Secuencias MediaGuide                                                                                                    | Abra el reproductor en la característica de la **guía multimedia** (tienda en línea activa actual en Windows Media Player 10 o posterior).                                                                                                                                                                                                                          |
| /Secuencias CDAudio                                                                                                       | Abra el reproductor en la característica **Copiar desde el CD** (**Rip** en Windows Media Player 10 o Windows Media Player 11). Este parámetro no se admite en Windows Media Player 12.                                                                                                                                                       |
| /Secuencias CDWrite                                                                                                       | Abra el reproductor en la característica de **grabación** . Requiere Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| /Secuencias MediaLibrary                                                                                                  | Abra el reproductor en la característica de **biblioteca** .                                                                                                                                                                                                                                                                                                |
| /Secuencias radiotune                                                                                                    | Abra el reproductor en la característica de **sintonizador de radio** (tienda en línea activa actual en Windows Media Player 10 o posterior).                                                                                                                                                                                                                          |
| /Secuencias PortableDevice                                                                                                | Abra el reproductor en la característica **Copiar en CD o dispositivo** (**sincronización** en Windows Media Player 10 o posterior).                                                                                                                                                                                                                            |
| /Secuencias Services/Service *ServiceName*                                                                               | Abra el reproductor en la característica de **servicios Premium** , mostrando el servicio especificado por el parámetro *ServiceName* . Este valor es el nombre único para el servicio. Si el servicio especificado no se ha visto anteriormente, se omite el parámetro *ServiceName* . (Abre la tienda en línea especificada en Windows Media Player 10 o posterior). |
| /Secuencias ServiceTask *X*                                                                                                | Abra el reproductor en el panel de tareas servicio de tienda en línea especificado por *X*. Por ejemplo,/secuencias ServiceTask1 abre el reproductor en el panel de tareas del primer servicio de tienda en línea.                                                                                                                                                                      |
| /Secuencias SkinViewer                                                                                                    | Abra el reproductor en la característica **selector de máscara** .                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Abra el reproductor y reproduzca la lista de reproducción especificada.                                                                                                                                                                                                                                                                                           |
| /Schema: {Music \| Pictures \| video \| TV \| otros} por ejemplo: `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Abra el reproductor y muestre la categoría de medios especificada. Requiere Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parámetros de línea de comandos para Wmpconfig

Wmpconfig.exe se usa para ejecutar determinados comandos de Windows Media Player que requieren permisos de administrador. Algunos ejemplos son el inicio y la detención de los servicios de exploración y uso compartido y la habilitación de excepciones en el Firewall de Windows. En la tabla siguiente se describen los posibles valores para los parámetros de la línea de comandos.



| Sintaxis                                                                                    | Comportamiento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| *Mac* DisableHMEDevice                                                                    | Deshabilita el dispositivo especificado por un identificador de Access Control de medios (MAC).  |
| Ejemplo de HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Deshabilita el servicio de uso compartido de red de Windows Media Player.                 |
| Ejemplo de HMEOn:<br/> wmpconfig HMEOn<br/>                                      | Habilita el uso compartido, la exploración y la excepción del firewall.                     |
| *Mac* RemoveHMEDevice                                                                     | Quita el dispositivo especificado por un identificador de MAC.                          |
| *Mac* RestoreHMEDevice                                                                    | Restaura el dispositivo especificado por un identificador de MAC.                         |
| Ejemplo de *nivel* de SetDVDParentalLevel:<br/> wmpconfig SetDVDParentalLevel 3<br/> | Establece el nivel de control parental de DVD. El nivel se especifica como un entero. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parámetros de línea de comandos para wmpnscfg

Microsoft Windows usa wmpnscfg.exe para alertar a los usuarios cuando se encuentran dispositivos de representación multimedia en la red. Wmpnscfg inicia el servicio de uso compartido de red de Windows Media Player (NSS) y, a continuación, espera las notificaciones del servicio. Cuando wmpnscfg recibe una notificación de que un nuevo dispositivo multimedia está disponible en la red, muestra una ventana emergente en la bandeja del sistema que informa al usuario sobre la disponibilidad del nuevo dispositivo. Si el usuario hace clic en el menú emergente, wmpnscfg inicia Windows Media Player, que muestra un cuadro de diálogo que pide al usuario que permita o deniegue el uso compartido con el nuevo dispositivo.

Normalmente, Windows llama a wmpnscfg sin parámetros de línea de comandos. Sin embargo, hay un parámetro disponible, que se describe en la tabla siguiente.



| Parámetro | Comportamiento                         |
|-----------|----------------------------------|
| /Close    | Cierre todas las instancias de wmpnscfg. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





