---
description: 'La combinación de ruta de acceso, especificación de archivo y marca de recursividad (wszPath, wszFileSpec y bRecursive, respectivamente) debe coincidir con la de uno de los conjuntos de archivos agregados a uno de los componentes del escritor mediante IVssCreateWriterMetadata:: AddFilesToFileGroup, IVssCreateWriterMetadata:: AddDatabaseFiles o IVssCreateWriterMetadata:: AddDatabaseLogFiles cuando:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Cambios semánticos en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276348"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Cambios semánticos en Windows Server 2003

La combinación de ruta de acceso, especificación de archivo y marca de recursividad (*wszPath*, *wszFileSpec* y *bRecursive*, respectivamente) debe coincidir con la de uno de los conjuntos de archivos agregados a uno de los componentes del escritor mediante [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) cuando:

-   Un solicitante agrega un nuevo destino mediante [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Un escritor agrega una asignación de ubicación alternativa mediante [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   Los archivos existentes se agregan como archivos diferenciados mediante [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Un solicitante indica que se usó una asignación de ubicación alternativa para restaurar un conjunto de archivos mediante [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).

 

 



