---
description: 'En la lista siguiente se indican adiciones y cambios en la interfaz Servicio de instantáneas de volumen en Windows Server 2003 con Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novedades de VSS en Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344213"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Novedades de VSS en Windows Server 2003 SP1

En la lista siguiente se indican adiciones y cambios en la interfaz Servicio de instantáneas de volumen en Windows Server 2003 con Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Recuperación automática

[*La recuperación automática*](vssgloss-a.md) permite a los escritores actualizar los componentes de una instantánea antes de que la instantánea se cambie permanentemente a solo lectura. Por ejemplo, una base de datos puede necesitar revertir las transacciones incompletas para todas las instantáneas (el escritor de base de datos establecería la marca **BACKUP \_ \_ \_ RECOVERY** de VSS CF para los componentes de la base de datos). La recuperación automática iniciada por el solicitante permite la restauración específica (por ejemplo, la restauración de una tabla en una base de datos o una carpeta en un servidor de correo) o la reversión para admitir la minería de datos para realizar análisis que serían demasiado lentos para un servidor de producción (el solicitante agregaría **VSS \_ VOLSNAP \_ ATTR \_ ROLLBACK \_ RECOVERY** al contexto de instantánea). La recuperación automática no es compatible con las instantáneas transportables, pero se admite la misma funcionalidad mediante la recuperación rápida mediante volúmenes de [instantáneas transportables.](fast-recovery-using-transportable-shadow-copied-volumes.md)

Los siguientes elementos de programación tienen cambios para admitir la recuperación automática:

Métodos de clase

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumeraciones

-   [**MARCAS DE \_ COMPONENTES \_ DE VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_ATRIBUTOS DE INSTANTÁNEAS \_ DE \_ VOLUMEN DE \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Métodos de interfaz

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Compatibilidad total con instantáneas transportables

Las instantáneas transportables se admiten en todas las ediciones de Windows Server 2003 con SP1. Para obtener más información, vea [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperación rápida mediante volúmenes de instantáneas transportables

[Recuperación rápida mediante volúmenes de instantáneas transportables](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Administración del área de almacenamiento de instantáneas

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



