---
title: Objeto Restorer de copia de seguridad
description: Objeto Restorer de copia de seguridad
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows SDK de formato multimedia, objetos de restaurador de copia de seguridad
- Formato de sistemas avanzados (ASF), objetos de restaurador de copia de seguridad
- ASF (formato de sistemas avanzados), objetos de restaurador de copia de seguridad
- objects,backup restorer objects
- restaurador de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267175"
---
# <a name="backup-restorer-object"></a>Objeto Restorer de copia de seguridad

El restaurador de copias de seguridad proporciona interfaces para controlar la copia de seguridad de licencias, normalmente en medios extraíbles y, a continuación, restaurar esas licencias en un nuevo equipo.

La función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) crea el objeto de restaurador de copia de seguridad, que establece un puntero a una [**interfaz IWMLicenseBackup.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) Las demás interfaces del objeto de restaurador de copia de seguridad se pueden obtener llamando al **método QueryInterface.**

El objeto de restaurador de copia de seguridad admite las interfaces siguientes.



| Interfaz                                              | Descripción                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Establece y recupera las propiedades requeridas por las interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) [**e IWMLicenseRestore.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Realiza una copia de seguridad de las licencias, normalmente para que se puedan restaurar en otro equipo.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Restaura licencias.                                                                                                                                        |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de restaurador de copia de seguridad.



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copia de seguridad y restauración de licencias**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




