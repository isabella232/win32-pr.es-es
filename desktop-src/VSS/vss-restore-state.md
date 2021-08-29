---
description: Durante una operación de restauración, el solicitante puede usar el método IVssBackupComponents::SetRestoreState para definir el tipo de operación de restauración en curso.
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: Estado de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45e3be9863904440c295ed8e32dd9d5a288226c5ab850a46556eff5953a7236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986555"
---
# <a name="vss-restore-state"></a>Estado de restauración de VSS

Durante una operación de restauración, el solicitante puede usar el método [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) para definir el tipo de operación de restauración en curso. Sin embargo, la mayoría de las operaciones de restauración no tendrán que invalidar el tipo de restauración predeterminado (VSS \_ RTYPE \_ UNDEFINED). Los escritores deben tratar este tipo de restauración como si fuera VSS \_ RTYPE \_ BY \_ COPY. Para obtener más información sobre los valores de tipo de restauración, vea la [**enumeración \_ RESTORE TYPE \_ de VSS.**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)

 

 



