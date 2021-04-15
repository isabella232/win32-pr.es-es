---
title: Objeto de restaurador de copia de seguridad
description: Objeto de restaurador de copia de seguridad
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- SDK de Windows Media Format, objetos de restauración de copia de seguridad
- Advanced Systems Format (ASF), objetos de restauración de copia de seguridad
- ASF (formato de sistemas avanzados), objetos de restauración de copia de seguridad
- objetos, objetos de restauración de copia de seguridad
- restaurador de copias de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676343"
---
# <a name="backup-restorer-object"></a>Objeto de restaurador de copia de seguridad

El restaurador de copias de seguridad proporciona interfaces para administrar las licencias de copia de seguridad, normalmente en medios extraíbles, y, a continuación, restaurar esas licencias en un nuevo equipo.

La función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) crea el objeto de almacén de copias de seguridad, que establece un puntero a una interfaz [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) . Las demás interfaces del objeto de almacén de copia de seguridad se pueden obtener llamando al método **QueryInterface** .

El objeto de almacén de copia de seguridad admite las siguientes interfaces.



| Interfaz                                              | Descripción                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Establece y recupera las propiedades requeridas por las interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) y [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) . |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Realiza una copia de seguridad de las licencias, normalmente para que se puedan restaurar en otro equipo.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Restaura las licencias.                                                                                                                                        |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de almacén de copia de seguridad.



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copia de seguridad y restauración de licencias**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




