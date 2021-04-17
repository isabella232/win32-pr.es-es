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
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="cec9b-103">Funcionalidad eliminada de Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cec9b-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="cec9b-104">La versión 2003 de Windows Server de VSS ya no es compatible con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cec9b-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="cec9b-105">Los escritores no pueden especificar nuevos destinos de restauración de archivos ([*nuevas ubicaciones de destino*](vssgloss-n.md)) en las operaciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="cec9b-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="cec9b-106">Ya no se admite volver a montar una instantánea expuesta como un volumen grabable.</span><span class="sxs-lookup"><span data-stu-id="cec9b-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="cec9b-107">El método **IVssBackupComponents:: RemountReadWrite** ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cec9b-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="cec9b-108">Los escritores no pueden especificar archivos incluidos explícitamente (mediante [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="cec9b-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="cec9b-109">Los archivos solo se pueden agregar a un componente como parte de un conjunto de archivos mediante [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span><span class="sxs-lookup"><span data-stu-id="cec9b-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="cec9b-110">Los archivos todavía se pueden excluir explícitamente de un componente mediante [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span><span class="sxs-lookup"><span data-stu-id="cec9b-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



