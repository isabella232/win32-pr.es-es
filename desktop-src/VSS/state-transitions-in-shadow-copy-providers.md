---
description: El modelo de transición de estado en un proveedor de instantáneas se simplifica mediante la serialización de la creación de instantáneas desde el momento en que se llama a IVssBackupComponents::StartSnapshotSet hasta que se devuelve la llamada a IVssBackupComponents::D oSnapshotSet.
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transiciones de estado en proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6141b9b8f221a1e67e95fde1e6b33ad819c0cbdead57eeb676164e89acc392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121605"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transiciones de estado en proveedores de instantáneas

El modelo de transición de estado en un proveedor de instantáneas se simplifica mediante la serialización de la creación de instantáneas desde el momento en que se llama a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) hasta que se devuelve la llamada a [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) Si otro solicitante intenta crear una instantánea durante este tiempo, se producirá un error en la llamada a **StartSnapshotSet** con el error **VSS \_ E SNAPSHOT SET IN \_ \_ \_ \_ PROGRESS**, que indica que el segundo solicitante debe esperar e intentarlo de nuevo.

VSS solo llamará a [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) después de que el solicitante haya llamado [**a DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)incluso si se produce un error en la instantánea o se anula antes de este punto. Esto significa que un proveedor no recibirá una llamada a **AbortSnapshots** hasta que se haya llamado a [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) Si se anula una instantánea o se produce un error antes de este punto, el proveedor no tiene ninguna indicación hasta que se inicia una nueva instantánea. Por este motivo, el proveedor debe estar preparado para controlar una llamada fuera de secuencia a [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) en cualquier momento. Esta llamada fuera de secuencia representa el inicio de una nueva secuencia de instantáneas y tendrá un nuevo identificador de conjunto de instantáneas.

 

 



