---
title: Permitir al usuario especificar dispositivos y archivos
description: Permitir al usuario especificar dispositivos y archivos
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Macro MCIWndOpenDialog
- Macro MCIWndOpen
- Macro MCIWndOpenInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9e388e4b7998a932cb22545c05509277f1f7fa705a81fbde02d4d5fb35cdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786274"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Permitir al usuario especificar dispositivos y archivos

Puede asociar un dispositivo o archivo a una ventana MCIWnd existente mediante las macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen y**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) [**MCIWndOpenInterface,**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) y la función [**GetOpenFileNamePreview.**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

Para permitir que un usuario de la aplicación seleccione un archivo para reproducir, use **MCIWndOpenDialog**. Esta macro muestra el **cuadro** de diálogo Abrir (que se muestra en la siguiente captura de pantalla) para elegir un archivo y asocia el archivo seleccionado a la ventana actual de MCIWnd.

![Imagen de ventana mciwnd](images/mciwnd3.gif)

Puede permitir que un usuario de la aplicación seleccione un archivo para asociarlo a una ventana de MCIWnd y obtener una vista previa de ese archivo mediante [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen). La **función GetOpenFileNamePreview** muestra el cuadro de diálogo Abrir para elegir un archivo y permite al usuario obtener una vista previa (reproducir) de su contenido.  Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo, **GetOpenFileNamePreview** proporciona un pequeño control para permitir que el usuario obtenga una vista previa del contenido del archivo. Puede asociar un archivo especificado, seleccionado con **GetOpenFileNamePreview** o especificado de otra manera, con una ventana MCIWnd mediante **MCIWndOpen**.

También puede usar **MCIWndOpen para** especificar un dispositivo que se va a asociar a una ventana de MCIWnd. Por ejemplo, puede usar un nombre de dispositivo, como "CDAudio".

Para asociar una ventana de MCIWnd a una interfaz de archivo o una interfaz de flujo de datos a datos multimedia, use la macro [**MCIWndOpenInterface.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) Para obtener más información sobre las interfaces de flujo de datos y archivo, vea [Funciones y macros AVIFile](avifile-functions-and-macros.md).

> [!Note]  
> Antes de asociar un nuevo archivo o dispositivo a una ventana de MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) cierran cualquier dispositivo asociado actualmente a la ventana. La aplicación no necesita cerrar ningún dispositivo abierto antes de usar estas macros.

 

 

 




