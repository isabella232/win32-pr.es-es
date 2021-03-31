---
description: Hay una serie de tipos diferentes de instantánea que puede crear un solicitante.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Creación simple de instantáneas para copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809422"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Creación simple de instantáneas para copia de seguridad

Hay una serie de tipos diferentes de instantánea que puede crear un solicitante. Sin embargo, para la mayoría de las aplicaciones de copia de seguridad, realizaría lo siguiente:

1.  Llame a [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con un contexto de la copia de seguridad de VSS \_ CTX \_ .
2.  Llame a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para inicializar la comunicación con escritores.
3.  Llame a [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar componentes de archivo y de base de datos a la copia de seguridad.
4.  Llame a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para inicializar el mecanismo de instantáneas.
5.  Llame a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para incluir los volúmenes en la instantánea.
6.  Llame a [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar a los escritores las operaciones de copia de seguridad.

 

 



