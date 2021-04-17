---
description: 'La versión 2003 de Windows Server de VSS ya no es compatible con lo siguiente:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Funcionalidad eliminada de Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697017"
---
# <a name="functionality-removed-from-windows-server-2003"></a>Funcionalidad eliminada de Windows Server 2003

La versión 2003 de Windows Server de VSS ya no es compatible con lo siguiente:

-   Los escritores no pueden especificar nuevos destinos de restauración de archivos ([*nuevas ubicaciones de destino*](vssgloss-n.md)) en las operaciones de restauración.
-   Ya no se admite volver a montar una instantánea expuesta como un volumen grabable. El método **IVssBackupComponents:: RemountReadWrite** ya no está disponible.
-   Los escritores no pueden especificar archivos incluidos explícitamente (mediante [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Los archivos solo se pueden agregar a un componente como parte de un conjunto de archivos mediante [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    Los archivos todavía se pueden excluir explícitamente de un componente mediante [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



