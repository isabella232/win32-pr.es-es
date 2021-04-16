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
# <a name="vss-restore-state"></a>Estado de restauración de VSS

Durante una operación de restauración, el solicitante puede usar el método [**IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) para definir el tipo de operación de restauración en curso. Sin embargo, la mayoría de las operaciones de restauración no tendrán que reemplazar el tipo de restauración predeterminado (RTYPE de VSS sin \_ \_ definir). Los escritores deben tratar este tipo de restauración como si fueran VSS \_ RTYPE \_ por \_ copia. Para obtener más información sobre los valores de tipo de restauración, consulte la enumeración de [**\_ \_ tipos de restauración de VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 



