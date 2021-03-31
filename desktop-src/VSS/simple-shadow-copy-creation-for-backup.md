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
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="b8665-103">Creación simple de instantáneas para copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="b8665-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="b8665-104">Hay una serie de tipos diferentes de instantánea que puede crear un solicitante.</span><span class="sxs-lookup"><span data-stu-id="b8665-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="b8665-105">Sin embargo, para la mayoría de las aplicaciones de copia de seguridad, realizaría lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8665-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="b8665-106">Llame a [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con un contexto de la copia de seguridad de VSS \_ CTX \_ .</span><span class="sxs-lookup"><span data-stu-id="b8665-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="b8665-107">Llame a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para inicializar la comunicación con escritores.</span><span class="sxs-lookup"><span data-stu-id="b8665-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="b8665-108">Llame a [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para agregar componentes de archivo y de base de datos a la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b8665-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="b8665-109">Llame a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para inicializar el mecanismo de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="b8665-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="b8665-110">Llame a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para incluir los volúmenes en la instantánea.</span><span class="sxs-lookup"><span data-stu-id="b8665-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="b8665-111">Llame a [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar a los escritores las operaciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b8665-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



