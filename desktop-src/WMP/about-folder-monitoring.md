---
title: Acerca de la supervisión de carpetas
description: Acerca de la supervisión de carpetas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, supervisión de carpetas
- Modelo de objetos de Windows Media Player, supervisión de carpetas
- modelo de objetos, supervisión de carpetas
- Control ActiveX de Windows Media Player, supervisión de carpetas
- Control ActiveX, supervisión de carpetas
- Control ActiveX móvil de Windows Media Player, supervisión de carpetas
- Windows Media Player Mobile, supervisión de carpetas
- supervisión de carpetas
- carpetas de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420226"
---
# <a name="about-folder-monitoring"></a>Acerca de la supervisión de carpetas

Windows Media Player puede supervisar carpetas que contienen archivos multimedia digitales y actualizar la biblioteca cuando se agregan o quitan archivos. La interfaz [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) proporciona esta funcionalidad de supervisión de carpetas.

Para usar los servicios de supervisión de carpetas, debe crear el objeto de reproductor en un estado remoto. Para obtener más información sobre la comunicación remota, vea [comunicación remota del control de Media Player de Windows](remoting-the-windows-media-player-control.md). Después de crear una instancia remota del reproductor, obtenga un puntero a la interfaz **IWMPFolderMonitorServices** llamando a **QueryInterface** en la interfaz [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .

Windows Media Player mantiene una lista de carpetas que se están supervisando. Para obtener una lista de las carpetas supervisadas, use los métodos [IWMPFolderMonitorServices:: get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) y [IWMPFolderMonitorServices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) . Para agregar carpetas a la lista o quitarlas de la lista, use los métodos [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) y [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) , respectivamente.

**Iniciar un examen**

La supervisión de carpetas suele ser un proceso en segundo plano que no necesita llamarse explícitamente. Si desea examinar activamente una carpeta, llame a [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Puede detener un examen en curso con el método [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .

**Recuperando el estado de supervisión de carpetas**

**IWMPFolderMonitorServices** proporciona funcionalidad para recuperar el estado del proceso de supervisión de carpetas.

El examen de carpetas se realiza en dos pasos. En el primer paso, el reproductor examina las carpetas mencionadas en la lista de carpetas supervisadas de una en una y crea una lista de los archivos que se van a agregar a la biblioteca. En el segundo paso, se recorre la lista de archivos y se agregan los archivos a la biblioteca, y también se quitan los elementos multimedia de la biblioteca cuyos archivos físicos correspondientes se han eliminado del sistema de archivos.

El evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) se usa para notificar al programa cada vez que el jugador cambie a un nuevo estado. También puede recuperar el estado actual llamando a [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Cuando se inicia el primer paso, el valor de estado actual es wmpfssScanning. Durante el segundo paso, el estado cambia a wmpfssUpdating. Una vez finalizado el proceso, el estado cambia a wmpfssStopped.

Mientras el reproductor está examinando las carpetas supervisadas en el primer paso, llame a [Get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para comprobar el número de archivos que se han analizado. El método [Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) le indicará qué carpeta se está analizando actualmente.

Una vez iniciada la segunda fase, llame a [Get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para comprobar el número de archivos que se han agregado a la biblioteca. El método [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) le indicará el progreso del segundo paso, en forma de porcentaje de 0 a 100.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interfaz IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




