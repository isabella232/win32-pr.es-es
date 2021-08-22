---
title: Acerca de la supervisión de carpetas
description: Acerca de la supervisión de carpetas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Reproductor de Windows Media,supervisión de carpetas
- Reproductor de Windows Media de objetos, supervisión de carpetas
- modelo de objetos, supervisión de carpetas
- Reproductor de Windows Media ActiveX control,supervisión de carpetas
- ActiveX control,supervisión de carpetas
- Reproductor de Windows Media Control de ActiveX móvil,supervisión de carpetas
- Reproductor de Windows Media Móvil, supervisión de carpetas
- supervisión de carpetas
- supervisar carpetas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055513"
---
# <a name="about-folder-monitoring"></a>Acerca de la supervisión de carpetas

Reproductor de Windows Media supervisar las carpetas que contienen archivos multimedia digitales y actualizar la biblioteca cuando se agregan o quitan archivos. Esta funcionalidad de supervisión de carpetas la proporciona la [interfaz IWMPFolderMonitorServices.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

Para usar los servicios de supervisión de carpetas, debe crear el objeto Player en un estado remoto. Para obtener más información sobre la comunicación remota, vea [Comunicación remota Reproductor de Windows Media control](remoting-the-windows-media-player-control.md). Después de crear una instancia remota del reproductor, obtenga un puntero a la interfaz **IWMPFolderMonitorServices** mediante una llamada a **QueryInterface** en la [interfaz IWMPPlayer.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)

Reproductor de Windows Media mantiene una lista de carpetas que se están supervisando. Para obtener una lista de carpetas supervisadas, use los [métodos IWMPFolderMonitorServices::get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices::item.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) Para agregar carpetas a la lista o quitarlas de la lista, use los [métodos IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) y [remove,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) respectivamente.

**Iniciar un examen**

Normalmente, la supervisión de carpetas es un proceso en segundo plano al que no es necesario llamar explícitamente. Si desea examinar activamente una carpeta, llame a [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Puede detener un examen en curso con el [método IWMPFolderMonitorServices::stopScan.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan)

**Recuperación del estado de supervisión de carpetas**

**IWMPFolderMonitorServices proporciona** funcionalidad para recuperar el estado del proceso de supervisión de carpetas.

El examen de carpetas se realiza en dos pases. En el primer paso, el Reproductor examina las carpetas denominadas en la lista de carpetas supervisadas una por una y crea una lista de archivos que se van a agregar a la biblioteca. En el segundo paso, pasa por la lista de archivos y agrega los archivos a la biblioteca, y también quita los elementos multimedia de la biblioteca cuyos archivos físicos correspondientes se han eliminado del sistema de archivos.

El [evento FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) se usa para notificar al programa cada vez que el reproductor cambia a un estado nuevo. También puede recuperar el estado actual llamando a [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Cuando se inicia el primer paso, el valor de estado actual es wmpfssScanning. Durante el segundo paso, el estado cambia a wmpfssUpdating. Una vez finalizado el proceso, el estado cambia a wmpfssStopped.

Mientras el reproductor examina las carpetas supervisadas en el primer paso, llame a [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para comprobar cuántos archivos se han examinado. El [método \_ get currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) le mostrará qué carpeta se está analizando actualmente.

Una vez que se inicia el segundo paso, llame a [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para comprobar cuántos archivos se han agregado a la biblioteca. El [método \_ get updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) le mostrará el progreso del segundo paso, como un porcentaje de 0 a 100.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPFolderMonitorServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




