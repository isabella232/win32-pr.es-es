---
title: Copia de seguridad y restauración de licencias
description: Copia de seguridad y restauración de licencias
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- SDK de Windows Media Format, copia de seguridad de licencias
- SDK de Windows Media Format, restaurar licencias
- SDK de Windows Media Format, copia de seguridad y restauración de licencias
- Advanced Systems Format (ASF), copia de seguridad de licencias
- ASF (formato de sistemas avanzados), copia de seguridad de licencias
- Advanced Systems Format (ASF), restaurar licencias
- ASF (formato de sistemas avanzados), restaurar licencias
- Formato de sistemas avanzados (ASF), copia de seguridad y restauración de licencias
- ASF (formato de sistemas avanzados), copia de seguridad y restauración de licencias
- Administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- Administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- Administración de derechos digitales (DRM), copia de seguridad y restauración de licencias
- DRM (administración de derechos digitales), copia de seguridad y restauración de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788787"
---
# <a name="backing-up-and-restoring-licenses"></a>Copia de seguridad y restauración de licencias

Los procesos de copia de seguridad y restauración son asíncronos. Se desencadenan cuando el usuario selecciona un comando de menú u opción en la aplicación para realizar una copia de seguridad o restaurar licencias. Debe permitir que el usuario especifique las ubicaciones en las que se debe realizar una copia de seguridad de las licencias y restaurarlas desde.

Para realizar una copia de seguridad de las licencias:

1.  Utilice la función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) para crear el objeto de almacén de copias de seguridad.
2.  Llame al método [**IWMBackupRestoreProps:: SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) para establecer la ruta de acceso de copia de seguridad (la ubicación donde escribirá los archivos, como un: \\ o D: \\ licenses).
3.  Llame al método [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) para realizar una copia de seguridad de las licencias en la ruta de acceso especificada.

Los eventos siguientes se envían al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ BACKUPRESTORE \_ Begin** indica que se ha iniciado el proceso de copia de seguridad.
-   **WMT \_ BACKUPRESTORE \_ End** indica que se ha completado el proceso de copia de seguridad.
-   **WMT \_ \_Licencia restringida** indica que no se puede realizar una copia de seguridad de una o varias licencias porque el propietario del contenido no lo ha permitido.

El identificador de clave también se incluye en este mensaje. Si ha implementado una base de datos para archivos protegidos que incluye el identificador y los metadatos de la clave, puede mostrar un mensaje al usuario con el título específico (por ejemplo, un título de la canción) para el que no se puede hacer una copia de seguridad de la licencia. De lo contrario, el mensaje debe ser genérico e informar al usuario de que no se puede realizar una copia de seguridad de algunas licencias.

Para restaurar licencias:

1.  Utilice la función **WMCreateBackupRestorer** para crear el objeto de almacén de copias de seguridad.
2.  Llame al método **IWMBackupRestoreProps:: SetProp** para establecer la ruta de acceso de restauración en la ubicación donde se realiza la copia de seguridad de las licencias.
3.  Llame al método [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) para restaurar licencias desde esa ubicación.

Los eventos siguientes se envían al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ La \_ conexión de BACKUPRESTORE** indica que la aplicación se está conectando al servicio de administración de licencias.
-   **WMT \_ La \_ desconexión de BACKUPRESTORE** indica que la aplicación se está desconectando del servicio de administración de licencias.
-   **WMT \_ BACKUPRESTORE \_ Begin** indica que se ha iniciado el proceso de restauración.
-   **WMT \_ BACKUPRESTORE \_ End** indica que se ha completado el proceso de restauración.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Interfaz IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Interfaz IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Interfaz IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




