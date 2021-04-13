---
description: Los solicitantes controlan las características de la instantánea estableciendo su contexto. Este contexto indica si la instantánea sobreviverá a la operación actual y el grado de la coordinación del escritor o del proveedor.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configuraciones de contexto de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544955"
---
# <a name="shadow-copy-context-configurations"></a>Configuraciones de contexto de instantáneas

Los solicitantes controlan las características de la instantánea estableciendo su contexto. Este contexto indica si la instantánea sobreviverá a la operación actual y el grado de la coordinación del escritor o del proveedor.

## <a name="persistence-and-shadow-copy-context"></a>Persistencia y contexto de instantáneas

Una instantánea puede ser [*persistente*](vssgloss-p.md), es decir, la instantánea no se elimina después de la finalización de una operación de copia de seguridad o de la liberación de un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Las instantáneas persistentes requieren contextos de [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) del **cliente de VSS \_ CTX \_ \_ accesible**, **\_ \_ \_ reversión de aplicación de VSS CTX** o **\_ \_ \_ reversión de NAS de VSS CTX**. Solo se pueden realizar instantáneas persistentes para volúmenes NTFS.

Las instantáneas no persistentes se crean con contextos de la copia de seguridad de **VSS \_ CTX \_** o del **\_ \_ \_ recurso compartido \_ de archivos de VSS CTX**. Se pueden realizar instantáneas no persistentes para volúmenes NTFS y no NTFS.

## <a name="writer-participation-and-shadow-copies"></a>Participación y instantáneas del escritor

Un contexto de instantánea se puede clasificar como que implique A escritores o que no implique escritores.

Entre los contextos de instantáneas que implican escritores en su creación se incluyen los siguientes:

-   **reversión de la aplicación de VSS \_ CTX \_ \_**
-   **copia de seguridad de VSS \_ CTX \_**
-   **\_ \_ \_ escritores accesibles del cliente \_ de VSS CTX**

Entre los que no implican escritores en su creación se incluyen los siguientes:

-   **cliente de VSS \_ CTX \_ \_ accesible**
-   **\_copia de \_ \_ seguridad de recurso compartido de archivos de VSS CTX \_**
-   **reversión de NAS de VSS \_ CTX \_ \_**

Un contexto se puede usar con ambos tipos de instantáneas, pero no se puede usar para crear una instantánea:

-   **All de VSS \_ \_**

No se admite la creación de una instantánea con un contexto de **VSS \_ CTX \_ All** (mediante [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) y [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)).

Las operaciones que admiten un contexto de **VSS \_ CTX \_** son las operaciones administrativas [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)y [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Obtener información de instantáneas

Si un solicitante conoce el GUID de identificación de una instantánea (su **\_ identificador de VSS**), puede obtener información sobre el contexto de una instantánea específica (identificada por su **\_ identificador de VSS**) desempaquetando la estructura de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) devuelta por una llamada a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Para obtener información de contexto sobre todas las instantáneas de un sistema, un solicitante examina el miembro **m \_ lSnapshotAttributes** del miembro **obj. Snap** del [**\_ objeto VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura de [**\_ instantáneas \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar por la lista de objetos devueltos por una llamada a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



