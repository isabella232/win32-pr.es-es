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
ms.openlocfilehash: 8a7bf14f8afda284d8d0ae3d4f36d37fff0baa63f4f42802a98830038ec2d850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028133"
---
# <a name="backup-restorer-object"></a>Objeto Restorer de copia de seguridad

El restaurador de copias de seguridad proporciona interfaces para controlar la copia de seguridad de licencias, normalmente en medios extraíbles y, a continuación, restaurar esas licencias en un nuevo equipo.

La función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) crea el objeto del restaurador de copia de seguridad, que establece un puntero a una [**interfaz IWMLicenseBackup.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) Las demás interfaces del objeto del restaurador de copia de seguridad se pueden obtener llamando al **método QueryInterface.**

El objeto de restaurador de copia de seguridad admite las interfaces siguientes.



| Interfaz                                              | Descripción                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Establece y recupera las propiedades requeridas por las interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) [**e IWMLicenseRestore.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Realiza una copia de seguridad de las licencias, normalmente para que se puedan restaurar en otro equipo.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Restaura las licencias.                                                                                                                                        |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto del restaurador de copia de seguridad.



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copia de seguridad y restauración de licencias**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




