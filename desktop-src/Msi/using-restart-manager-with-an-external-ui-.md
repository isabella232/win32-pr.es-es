---
description: Windows Los desarrolladores del instalador pueden preparar su paquete de instalación para que funcione con el Administrador de reinicio siguiendo las instrucciones descritas en Uso de Windows instalador con el Administrador de reinicio.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Usar el Administrador de reinicio con una interfaz de usuario externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad6a8bee0e98adbcea853a21378b539e02f14468a93aed3cff7dc8bf6f25800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996225"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Usar el Administrador de reinicio con una interfaz de usuario externa

Windows Los desarrolladores de instaladores pueden preparar su paquete de instalación para que funcione con [el](../rstmgr/restart-manager-portal.md) Administrador de reinicio siguiendo las instrucciones descritas en Uso [de Windows Installer con el Administrador de reinicio](using-windows-installer-with-restart-manager.md).

Especifique el tipo de mensaje INSTALLLOGMODE RMFILESINUSE al llamar a la función \_ [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) o [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) para habilitar el controlador de interfaz de usuario externo. Windows A continuación, el instalador envía un mensaje INSTALLMESSAGE RMFILESINUSE para que lo usen los controladores de interfaz de usuario externos que \_ [admiten el Administrador de reinicio.](../rstmgr/restart-manager-portal.md)

El controlador de interfaz de usuario externo debe controlar la información contenida en los mensajes INSTALLMESSAGE \_ RMFILESINUSE. Si ninguna interfaz de usuario interna o registrada controla el mensaje INSTALLMESSAGE RMFILESINUSE, el instalador de Windows envía un mensaje INSTALLMESSAGE FILESINUSE para que lo usen los controladores externos existentes que admiten mensajes INSTALLMESSAGE FILESINUSE y el cuadro de diálogo \_ \_ \_ [FilesInUse.](filesinuse-dialog.md)

La interfaz de usuario externa puede devolver los valores enumerados en la tabla siguiente.



| Valor devuelto de la interfaz de usuario externa | Acción realizada por Windows Instalador                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | El **usuario** presionó el botón Aceptar. El Windows de archivos solicitará que [el](../rstmgr/restart-manager-portal.md) Administrador de reinicio apague y reinicie las aplicaciones que tienen archivos actualmente en uso.                                                                                                                                               |
| IDCANCEL                 | Se **ha** presionado el botón CANCELAR. Cancele la instalación.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | Se **presionó** el botón IGNORE. Ignore y continúe con la instalación. Se requiere un reinicio al final de la instalación.                                                                                                                                                                                                            |
| IDNO                     | Se **presionó** el botón NO. Si el paquete tiene un [cuadro de diálogo MsiRMFilesInUse,](msirmfilesinuse-dialog.md) envíe un mensaje 1610. Para obtener más información, [vea Windows de error del instalador.](windows-installer-error-messages.md) Si el paquete no tiene un cuadro de diálogo MsiRMFilesInUse, envíe un mensaje INSTALLMESSAGE \_ FILESINUSE. |
| IDRETRY                  | Se **presionó** el botón RETRY. Envíe el mensaje INSTALLMESSAGE \_ FILESINUSE.                                                                                                                                                                                                                                                                 |
| -1                       | Un error. Finalice la instalación.                                                                                                                                                                                                                                                                                                                |



 

 

 
