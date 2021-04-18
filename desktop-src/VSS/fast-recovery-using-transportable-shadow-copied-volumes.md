---
description: Las instantáneas transportables se pueden usar para facilitar una recuperación rápida.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Recuperación rápida mediante el uso de volúmenes de instantáneas transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697738"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperación rápida mediante el uso de volúmenes de instantáneas transportables

Las [*instantáneas transportables*](vssgloss-t.md) se pueden usar para facilitar una *recuperación rápida*.

La recuperación rápida se puede usar para revertir rápidamente a una instantánea anterior. Estos son los pasos que hay que realizar:

1.  Cree la instantánea transportable de los LUN correspondientes. La instantánea puede ser [*persistente*](vssgloss-p.md) o no persistente.
2.  Quitar los LUN originales
    1.  Si el equipo está dentro de un clúster, marque los recursos de disco afectados como sin conexión o habilite el [modo de mantenimiento](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) para estos recursos de disco.
    2.  Enmascarar los LUN afectados desde este equipo (y todos los demás nodos si el equipo está en un clúster).
3.  Importe la instantánea con el método [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .
4.  Divida la instantánea con el método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .
5.  Marque los nuevos volúmenes de instantáneas como de lectura/escritura.
6.  Si el equipo está en un clúster, exponga los LUN de instantáneas nuevos como los LUN originales.
    1.  Desenmascarar los LUN de instantánea en los otros nodos del clúster.
    2.  Marque los recursos que se han marcado previamente como sin conexión como en línea o deshabilite el modo de mantenimiento para esos recursos de disco.

> [!Note]  
> No se admiten las instantáneas transportables en un clúster antes de Windows Server 2003 con Service Pack 1 (SP1). Esto solo es compatible con los LUN compatibles, que tienen al menos una página de datos vitales de producto (VPD) de SCSI 0x83 \_ identificador de almacenamiento de tipo 1, 2 u 8, y la Asociación 0, y los LUN deben mantener un disco básico con particiones MBR.

 

 

 
