---
description: Un solicitante puede interrumpir un conjunto de instantáneas mediante el método IVssBackupComponents::BreakSnapshotSet o IVssBackupComponentsEx2::BreakSnapshotSetEx.
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Instantáneas de última hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473393"
---
# <a name="breaking-shadow-copies"></a>Instantáneas de última hora

Un solicitante puede interrumpir un conjunto de instantáneas mediante el método [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**IVssBackupComponentsEx2::BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

Una instantánea rota es un volumen que contiene una instantánea que VSS ya no administra. La separación de una instantánea solo tiene significado si el proveedor de la [*instantánea*](vssgloss-p.md) es un proveedor [*de hardware*](vssgloss-h.md). Esto se debe a que solo los proveedores de hardware pueden implementar una instantánea como un volumen real con un ciclo de vida independiente de VSS. Si VSS no administra este tipo de volumen, sigue estando disponible.

Los proveedores de software mantienen instantáneas solo mientras participan en las operaciones de VSS. Por ese motivo, la separación de una instantánea no tiene ningún significado para los proveedores de software.

Si un proveedor de hardware administra la instantánea, el solicitante debe importar la instantánea antes de llamar a [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) En el caso de instantáneas no transportables (creadas por un proveedor de hardware), se importan implícitamente como parte de la llamada [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)

Una vez que el solicitante ha llamado a [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)el conjunto de instantáneas sigue siendo accesible a través de sus objetos de dispositivo u otras rutas de acceso, pero ya no es un conjunto de instantáneas. Se puede administrar como uno o varios LUN mediante las interfaces COM de Virtual Disk Service (VDS). Con VDS, un solicitante puede convertir los LUN para leerlos o escribirlos, montarlos con letras de unidad o enmascararlos o desenmascararlos en otros equipos. Consulte la [documentación de VDS API](../vds/virtual-disk-service-portal.md) para obtener más información.

 

 
