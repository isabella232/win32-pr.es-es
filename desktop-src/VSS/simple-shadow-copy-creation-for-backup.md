---
description: Hay varios tipos diferentes de instantáneas que un solicitante puede crear.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Creación sencilla de instantáneas para copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f9cda7a2d2679979879a2333b30621fb7f73a449f4a15b55b42c603cd913713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394175"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Creación sencilla de instantáneas para copia de seguridad

Hay varios tipos diferentes de instantáneas que un solicitante puede crear. Sin embargo, para la mayoría de las aplicaciones de copia de seguridad, haría lo siguiente:

1.  Llame [**a IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con un contexto de VSS \_ CTX \_ BACKUP.
2.  Llame [**a IVssBackupComponents::GatherWriterMetadata para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) inicializar la comunicación con los escritores.
3.  Llame [**a IVssBackupComponents::AddComponent para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) agregar componentes de archivo y base de datos a la copia de seguridad.
4.  Llame [**a IVssBackupComponents::StartSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) inicializar el mecanismo de instantáneas.
5.  Llame [**a IVssBackupComponents::AddToSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) incluir volúmenes en la instantánea.
6.  Llame [**a IVssBackupComponents::P repareForBackup para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) notificar a los escritores las operaciones de copia de seguridad.

 

 



