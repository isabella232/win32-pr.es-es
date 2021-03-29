---
title: Permitir al usuario especificar dispositivos y archivos
description: Permitir al usuario especificar dispositivos y archivos
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog (macro)
- MCIWndOpen (macro)
- MCIWndOpenInterface (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776519"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Permitir al usuario especificar dispositivos y archivos

Puede asociar un dispositivo o un archivo a una ventana de MCIWnd existente mediante las macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)y [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) , y la función [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .

Para permitir que un usuario de la aplicación Seleccione un archivo para reproducirlo, use **MCIWndOpenDialog**. Esta macro muestra el cuadro de diálogo **abrir** (que se muestra en la siguiente captura de pantalla) para elegir un archivo y asocia el archivo seleccionado a la ventana de MCIWnd actual.

![imagen de la ventana de mciwnd](images/mciwnd3.gif)

Puede permitir que un usuario de la aplicación Seleccione un archivo para asociarlo a una ventana de MCIWnd y obtenga una vista previa del archivo mediante [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen). La función **GetOpenFileNamePreview** muestra el cuadro de diálogo **abrir** para elegir un archivo y permite a la vista previa del usuario (reproducir) su contenido. Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo, **GetOpenFileNamePreview** proporciona un pequeño control para permitir que el usuario obtenga una vista previa del contenido del archivo. Puede asociar un archivo especificado, seleccionado con **GetOpenFileNamePreview** o especificado de otra manera, con una ventana de MCIWnd con **MCIWndOpen**.

También puede usar **MCIWndOpen** para especificar un dispositivo que se va a asociar a una ventana de MCIWnd. Por ejemplo, puede usar un nombre de dispositivo, como "CDAudio".

Para asociar una ventana de MCIWnd con una interfaz de archivo o una interfaz de flujo de datos a datos multimedia, use la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) . Para obtener más información sobre las interfaces de archivo y de flujo de datos, vea [AVIFile Functions and macros](avifile-functions-and-macros.md).

> [!Note]  
> Antes de asociar un nuevo archivo o dispositivo a una ventana de MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) cierran cualquier dispositivo asociado actualmente a la ventana. No es necesario que la aplicación cierre ningún dispositivo abierto antes de usar estas macros.

 

 

 




