---
description: Las instantáneas transportables se pueden usar para facilitar una recuperación rápida.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Recuperación rápida mediante volúmenes de instantáneas transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473372"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperación rápida mediante volúmenes de instantáneas transportables

[*Las instantáneas transportables*](vssgloss-t.md) se pueden usar para facilitar una *recuperación rápida.*

La recuperación rápida se puede usar para revertir rápidamente a una instantánea anterior. Estos son los pasos que hay que realizar:

1.  Cree la instantánea transportable de los LUN adecuados. La instantánea puede ser [*persistente o*](vssgloss-p.md) no persistente.
2.  Eliminación de los LUN originales
    1.  Si el equipo está dentro de un clúster, marque los recursos de disco afectados como sin conexión o habilite el modo [de](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) mantenimiento para estos recursos de disco.
    2.  Enmascara los LUN afectados de este equipo (y todos los demás nodos si el equipo está en un clúster).
3.  Importe la instantánea mediante [**el método IVssBackupComponents::ImportSnapshots.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots)
4.  Interrumpir la instantánea mediante el [**método IVssBackupComponents::BreakSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)
5.  Marque los nuevos volúmenes de instantáneas como de lectura y escritura.
6.  Si el equipo está en un clúster, exponga los nuevos LUN de instantáneas como LUN originales.
    1.  Desenmascarar los LUN de instantáneas en los demás nodos del clúster.
    2.  Marque los recursos marcados anteriormente como sin conexión como en línea o deshabilite el modo de mantenimiento para esos recursos de disco.

> [!Note]  
> Las instantáneas transportables en un clúster no se admiten antes Windows Server 2003 con Service Pack 1 (SP1). Esto solo se admite con LUN compatibles, que tienen al menos una página SCSI Vital Product Data (VPD) 0x83 STORAGE IDENTIFIER de tipo 1,2 u 8, y la asociación 0, y los LUN deben mantener un disco básico con \_ particiones MBR.

 

 

 
