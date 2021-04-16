---
description: 'Durante una operación de restauración, el solicitante puede usar el método IVssBackupComponents:: SetRestoreState para definir el tipo de operación de restauración en curso.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: Estado de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696461"
---
# <a name="vss-restore-state"></a><span data-ttu-id="30fbf-103">Estado de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="30fbf-103">VSS Restore State</span></span>

<span data-ttu-id="30fbf-104">Durante una operación de restauración, el solicitante puede usar el método [**IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) para definir el tipo de operación de restauración en curso.</span><span class="sxs-lookup"><span data-stu-id="30fbf-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="30fbf-105">Sin embargo, la mayoría de las operaciones de restauración no tendrán que reemplazar el tipo de restauración predeterminado (RTYPE de VSS sin \_ \_ definir).</span><span class="sxs-lookup"><span data-stu-id="30fbf-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="30fbf-106">Los escritores deben tratar este tipo de restauración como si fueran VSS \_ RTYPE \_ por \_ copia.</span><span class="sxs-lookup"><span data-stu-id="30fbf-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="30fbf-107">Para obtener más información sobre los valores de tipo de restauración, consulte la enumeración de [**\_ \_ tipos de restauración de VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="30fbf-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 



