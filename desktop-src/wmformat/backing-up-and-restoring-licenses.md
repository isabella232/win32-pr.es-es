---
title: Copia de seguridad y restauración de licencias
description: Copia de seguridad y restauración de licencias
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows SDK de formato multimedia, copia de seguridad de licencias
- Windows SDK de formato multimedia, restaurar licencias
- Windows SDK de formato multimedia, copia de seguridad y restauración de licencias
- Formato de sistemas avanzados (ASF), copia de seguridad de licencias
- ASF (formato de sistemas avanzados), copia de seguridad de licencias
- Formato de sistemas avanzados (ASF), restaurar licencias
- ASF (formato de sistemas avanzados), restaurar licencias
- Formato de sistemas avanzados (ASF), copia de seguridad y restauración de licencias
- ASF (formato de sistemas avanzados), copia de seguridad y restauración de licencias
- administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- administración de derechos digitales (DRM), copia de seguridad y restauración de licencias
- DRM (administración de derechos digitales), copia de seguridad y restauración de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378a41d975e8f19d38c637d585759d0038f5b86550769ae49d6a6490844f223e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028143"
---
# <a name="backing-up-and-restoring-licenses"></a>Copia de seguridad y restauración de licencias

Los procesos de copia de seguridad y restauración son asincrónicos. Se desencadenan cuando el usuario selecciona un comando de menú o una opción en la aplicación para hacer copias de seguridad o restaurar licencias. Debe permitir que el usuario especifique las ubicaciones desde las que se debe realizar una copia de seguridad de las licencias y desde las que se deben restaurar.

Para hacer una copia de seguridad de licencias:

1.  Use la [**función WMCreateBackupRestorer para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) crear el objeto de restaurador de copia de seguridad.
2.  Llame al [**método IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) para establecer la ruta de acceso de copia de seguridad (la ubicación donde escribirá los archivos, como A: \\ o D: \\ Licencias).
3.  Llame al [**método IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) para hacer una copia de seguridad de las licencias en la ruta de acceso especificada.

Los eventos siguientes se envían al [**método IWMStatusCallback::OnStatus:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)

-   **WMT \_ BACKUPRESTORE \_ BEGIN indica** que se ha iniciado el proceso de copia de seguridad.
-   **WMT \_ BACKUPRESTORE \_ END indica** que se ha completado el proceso de copia de seguridad.
-   **WMT \_ RESTRICTED \_ LICENSE indica** que no se puede hacer una copia de seguridad de una o varias licencias porque el propietario del contenido no ha permitido el derecho.

El identificador de clave también se incluye en este mensaje. Si ha implementado una base de datos para archivos protegidos que incluye el identificador de clave y los metadatos, puede mostrar un mensaje al usuario con el título específico (por ejemplo, un título de canción) para el que no se puede hacer una copia de seguridad de la licencia. De lo contrario, el mensaje debe ser genérico e informar al usuario de que no se puede realizar una copia de seguridad de algunas licencias.

Para restaurar licencias:

1.  Use la **función WMCreateBackupRestorer para** crear el objeto de restaurador de copia de seguridad.
2.  Llame al **método IWMBackupRestoreProps::SetProp** para establecer la ruta de acceso de restauración en la ubicación en la que se hace una copia de seguridad de las licencias.
3.  Llame al [**método IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) para restaurar licencias desde esa ubicación.

Los eventos siguientes se envían al [**método IWMStatusCallback::OnStatus:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)

-   **WMT \_ BACKUPRESTORE \_ CONNECTING** indica que la aplicación se está conectando al Servicio de administración de licencias.
-   **WMT \_ BACKUPRESTORE \_ DISCONNECTING** indica que la aplicación se está desconectando del Servicio de administración de licencias.
-   **WMT \_ BACKUPRESTORE \_ BEGIN indica** que se ha iniciado el proceso de restauración.
-   **WMT \_ BACKUPRESTORE \_ END indica** que se ha completado el proceso de restauración.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**IWMBackupRestoreProps (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**IWMLicenseBackup (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**IWMLicenseRestore (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




