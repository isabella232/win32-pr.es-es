---
description: 'El modelo de transición de estado en un proveedor de instantáneas se simplifica mediante la serialización de la creación de instantáneas desde el momento en que se llama a IVssBackupComponents:: StartSnapshotSet hasta que la llamada a IVssBackupComponents::D oSnapshotSet devuelve.'
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transiciones de estado en proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d628d11419158f947225b2e4cabd7f93975f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697160"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transiciones de estado en proveedores de instantáneas

El modelo de transición de estado en un proveedor de instantáneas se simplifica mediante la serialización de la creación de instantáneas desde el momento en que se llama a [**ivssbackupcomponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) hasta que la llamada a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) devuelve. Si otro solicitante intenta crear una instantánea durante este tiempo, se producirá un error en la llamada a **StartSnapshotSet** con **el \_ \_ conjunto de instantáneas de VSS e \_ \_ en \_ curso**, lo que indica que el segundo solicitante debe esperar e intentarlo de nuevo.

VSS solo llamará a [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) después de que el solicitante haya llamado a [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), incluso si se produce un error en la instantánea o se anula antes de este punto. Esto significa que un proveedor no recibirá una llamada a **AbortSnapshots** hasta que no se haya llamado a [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) . Si se anula una instantánea o se produce un error antes de este punto, el proveedor no recibirá ninguna indicación hasta que se inicie una nueva instantánea. Por esta razón, el proveedor debe estar preparado para controlar una llamada fuera de secuencia a [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) en cualquier momento. Esta llamada fuera de secuencia representa el inicio de una nueva secuencia de instantáneas y tendrá un nuevo identificador de conjunto de instantáneas.

 

 



