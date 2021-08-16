---
title: Parámetros de línea de comandos
description: Parámetros de línea de comandos
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Reproductor de Windows Media,parameters
- Reproductor de Windows Media, parámetros de línea de comandos
- Reproductor de Windows Media,Wmplayer
- Reproductor de Windows Media,Wmpconfig
- Reproductor de Windows Media,Wmpnscfg
- parámetros de la línea de comandos
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341955"
---
# <a name="command-line-parameters"></a>Parámetros de línea de comandos

## <a name="command-line-parameters-for-wmplayer"></a>Parámetros de línea de comandos para Wmplayer

Reproductor de Windows Media admite un conjunto de parámetros de línea de comandos que especifican cómo se comporta el reproductor cuando se inicia. En la tabla siguiente se detallan los parámetros y sus comportamientos.



| Syntax                                                                                                              | Comportamiento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*nombre de archivo \\ de* ruta de acceso "(Por ejemplo: `wmplayer "c:\filename.wma"` )<br/>                                            | Inicie el reproductor y reprodgue el archivo.                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*" /fullscreen(Por ejemplo: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Reprodgue el archivo especificado en modo de pantalla completa. Debe especificar la ruta de acceso y el nombre de archivo del contenido que se va a reproducir.<br/>                                                                                                                                                                                                                     |
| /Device:{DVD \| AudioCD}(Por ejemplo: `wmplayer /device:audio CD` )<br/>                                         | Reproducir un DVD o un CD de audio.                                                                                                                                                                                                                                                                                                                    |
| " path *\\ filename*? WMPSkin=*nombre de máscara*"Por ejemplo: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Abra el Reproductor, aplicando la máscara especificada.                                                                                                                                                                                                                                                                                              |
| /Service:*keyname*                                                                                                  | Abra el reproductor que muestra el almacén en línea especificado por *keyname*. Requiere Reproductor de Windows Media 10 o posterior.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Abra el reproductor en la **característica Reproducción** ahora.                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | Abra la característica Reproductor en la **guía multimedia** (tienda en línea activa actual en Reproductor de Windows Media 10 o posterior).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | Abra el reproductor en la **característica Copiar** desde CD **(característica** Desgarrar en Reproductor de Windows Media 10 Reproductor de Windows Media 11). Este parámetro no se admite en Reproductor de Windows Media 12.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Abra el reproductor en la **característica Grabar.** Requiere Reproductor de Windows Media 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Abra el reproductor en la **característica Biblioteca.**                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Abra el reproductor en la **característica Radio Tuner** (tienda en línea activa actual en Reproductor de Windows Media 10 o posterior).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | Abra el reproductor en la característica **Copiar en CD o Dispositivo** (característica de sincronización Reproductor de Windows Media 10 o posterior).                                                                                                                                                                                                                            |
| /Task Services /Service *servicename*                                                                               | Abra el Reproductor en la **característica Premium Services,** que muestra el servicio especificado por el *parámetro servicename.* Este valor es el nombre único del servicio. Si el servicio especificado no se ha visto previamente, se omite el parámetro *servicename.* (Abre el almacén en línea especificado en Reproductor de Windows Media 10 o posterior). |
| /Task ServiceTask *X*                                                                                                | Abra el reproductor en el panel de tareas del servicio de tienda en línea especificado por *X*. Por ejemplo, /Task ServiceTask1 abre el Reproductor en el primer panel de tareas del servicio de tienda en línea.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Abra la característica Player in the Skin Chooser (Reproductor **en la característica Skin Chooser).**                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Abra el Reproductor y reprodgue la lista de reproducción especificada.                                                                                                                                                                                                                                                                                           |
| /Schema:{Música \| Pictures \| Video TV \| \| Other}Por ejemplo:`wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Abra el Reproductor, que muestra la categoría de medios especificada. Requiere Reproductor de Windows Media 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parámetros de la línea de comandos para Wmpconfig

Wmpconfig.exe se usa para ejecutar determinados comandos en Reproductor de Windows Media que requieren permiso de administrador. Entre los ejemplos se incluyen el inicio y la detención de los servicios de exploración y uso compartido, y la habilitación de excepciones en Windows Firewall. En la tabla siguiente se describen los valores posibles para los parámetros de la línea de comandos.



| Syntax                                                                                    | Comportamiento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *MAC*                                                                    | Deshabilita el dispositivo especificado por un identificador Access Control multimedia (MAC).  |
| Ejemplo de HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Deshabilita el servicio Reproductor de Windows Media uso compartido de red.                 |
| Ejemplo de HMEOn:<br/> wmpconfig HMEOn<br/>                                      | Habilita el uso compartido, la exploración y la excepción de firewall.                     |
| RemoveHMEDevice *MAC*                                                                     | Quita el dispositivo especificado por un identificador MAC.                          |
| RestoreHMEDevice *MAC*                                                                    | Restaura el dispositivo especificado por un identificador MAC.                         |
| Ejemplo de nivel SetDVDParentalLevel:<br/> wmpconfig SetDVDParentalLevel 3<br/> | Establece el nivel de control parental del DVD. El nivel se especifica como un entero. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parámetros de la línea de comandos para Wmpnscfg

Microsoft Windows usa wmpnscfg.exe alertar a los usuarios cuando se encuentran dispositivos de representación multimedia en la red. Wmpnscfg inicia Reproductor de Windows Media servicio de uso compartido de red (NSS) y, a continuación, espera las notificaciones del servicio. Cuando se notifica a wmpnscfg que hay un nuevo dispositivo multimedia disponible en la red, muestra un elemento emergente en la bandeja del sistema que informa al usuario sobre la disponibilidad del nuevo dispositivo. Si el usuario hace clic en el elemento emergente, wmpnscfg inicia Reproductor de Windows Media, que muestra un cuadro de diálogo que pide al usuario que permita o deniegue el uso compartido con el nuevo dispositivo.

Normalmente, Windows a wmpnscfg sin parámetros de línea de comandos. Sin embargo, hay un parámetro disponible, que se describe en la tabla siguiente.



| Parámetro | Comportamiento                         |
|-----------|----------------------------------|
| /Close    | Cierre todas las instancias de wmpnscfg. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





