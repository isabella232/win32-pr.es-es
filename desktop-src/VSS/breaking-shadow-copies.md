---
description: Un solicitante puede interrumpir un conjunto de instantáneas mediante el método IVssBackupComponents::BreakSnapshotSet o IVssBackupComponentsEx2::BreakSnapshotSetEx.
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Instantáneas de última hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032905"
---
# <a name="breaking-shadow-copies"></a>Instantáneas de última hora

Un solicitante puede interrumpir un conjunto de instantáneas mediante el método [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**IVssBackupComponentsEx2::BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

Una instantánea rota es un volumen que contiene una instantánea que VSS ya no administra. La separación de una instantánea solo tiene significado si el proveedor de la instantánea [*es*](vssgloss-p.md) un proveedor [*de hardware.*](vssgloss-h.md) Esto se debe a que solo los proveedores de hardware pueden implementar una instantánea como un volumen real con un ciclo de vida independiente de VSS. Si VSS no administra este tipo de volumen, sigue estando disponible.

Los proveedores de software solo mantienen instantáneas mientras participan en las operaciones de VSS. Por ese motivo, la separación de una instantánea no tiene ningún significado para los proveedores de software.

Si un proveedor de hardware administra la instantánea, el solicitante debe importar la instantánea antes de llamar a [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) En el caso de instantáneas no transportables (creadas por un proveedor de hardware), se importan implícitamente como parte de la llamada [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)

Una vez que el solicitante ha llamado [**a BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)el conjunto de instantáneas sigue siendo accesible a través de sus objetos de dispositivo u otras rutas de acceso, pero ya no es un conjunto de instantáneas. Se puede administrar como uno o varios LUN mediante las interfaces COM de Virtual Disk Service (VDS). Con VDS, un solicitante puede convertir los LUN en lectura y escritura, montarlos con letras de unidad o enmascararlos o desenmascararlos en otros equipos. Consulte la [documentación de VDS API](../vds/virtual-disk-service-portal.md) para obtener más información.

 

 
