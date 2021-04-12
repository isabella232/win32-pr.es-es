---
description: Windows Installer los desarrolladores pueden preparar el paquete de instalación para que funcione con reinicio Manager siguiendo las instrucciones descritas en uso de Windows Installer con el administrador de reinicio.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Uso del administrador de reinicio con una interfaz de usuario externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275434"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Uso del administrador de reinicio con una interfaz de usuario externa

Windows Installer los desarrolladores pueden preparar el paquete de instalación para que funcione con [reinicio Manager](../rstmgr/restart-manager-portal.md) siguiendo las instrucciones descritas en [uso de Windows Installer con el administrador de reinicio](using-windows-installer-with-restart-manager.md).

Especifique el \_ tipo de mensaje RMFILESINUSE de INSTALLLOGMODE al llamar a la función [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) o [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) para habilitar el controlador de la interfaz de usuario externo. A continuación, Windows Installer envía un \_ mensaje RMFILESINUSE de INSTALLMESSAGE para que lo usen los controladores externos de la interfaz de usuario que admiten el [Administrador de reinicio](../rstmgr/restart-manager-portal.md).

El controlador de la interfaz de usuario externo debe administrar la información contenida en \_ los mensajes de INSTALLMESSAGE RMFILESINUSE. Si no hay ninguna interfaz de usuario registrada o interna que controla el \_ mensaje INSTALLMESSAGE RMFILESINUSE, Windows Installer envía un \_ mensaje FILESINUSE de INSTALLMESSAGE para que lo usen los controladores externos existentes que admiten \_ los mensajes INSTALLMESSAGE FILESINUSE y el cuadro de diálogo [FILESINUSE](filesinuse-dialog.md) .

La interfaz de usuario externa puede devolver los valores que se muestran en la tabla siguiente.



| Valor devuelto de IU externa | Acción realizada por Windows Installer                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | El usuario presionó el botón **Aceptar** . El Windows Installer solicitará que el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) se apague y reinicie las aplicaciones que contienen archivos que están en uso actualmente.                                                                                                                                               |
| IDCANCEL                 | Se presionó el botón **Cancelar** . Cancele la instalación.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | Se presionó el botón **omitir** . Omitir y continuar con la instalación. Al final de la instalación, se requerirá un reinicio.                                                                                                                                                                                                            |
| IDNO                     | Se presionó el botón **no** . Si el paquete tiene un cuadro de diálogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) , envíe un mensaje 1610. Para obtener más información, vea [Windows Installer mensajes de error](windows-installer-error-messages.md). Si el paquete no tiene un cuadro de diálogo MsiRMFilesInUse, envíe un \_ mensaje INSTALLMESSAGE FILESINUSE. |
| IDRETRY                  | Se presionó el botón **Reintentar** . Envíe el \_ mensaje FILESINUSE de INSTALLMESSAGE.                                                                                                                                                                                                                                                                 |
| -1                       | Un error. Finalice la instalación.                                                                                                                                                                                                                                                                                                                |



 

 

 
