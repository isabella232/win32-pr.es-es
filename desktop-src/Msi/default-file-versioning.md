---
description: En los diagramas de flujo de las secciones siguientes se muestran las reglas de control de versiones de archivo predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo ya instalado en la ubicación de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Control de versiones de archivo predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910978"
---
# <a name="default-file-versioning"></a><span data-ttu-id="d8d6f-103">Control de versiones de archivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="d8d6f-103">Default File Versioning</span></span>

<span data-ttu-id="d8d6f-104">En los diagramas de flujo de las secciones siguientes se muestran las reglas de control de versiones de archivo predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo ya instalado en la ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="d8d6f-105">El control de versiones de archivo predeterminado también se muestra en [reemplazar archivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6f-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="d8d6f-106">Tenga en cuenta que, con Windows Installer, el hash de archivo está disponible para optimizar la copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="d8d6f-107">Para obtener más información, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6f-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="d8d6f-108">La tabla MsiFileHash solo se puede usar con archivos sin versión.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="d8d6f-109">Ambos archivos tienen una versión</span><span class="sxs-lookup"><span data-stu-id="d8d6f-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="d8d6f-110">Ninguno de los archivos tiene una versión</span><span class="sxs-lookup"><span data-stu-id="d8d6f-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="d8d6f-111">Ninguno de los archivos tiene una versión con comprobación de hash de archivo</span><span class="sxs-lookup"><span data-stu-id="d8d6f-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="d8d6f-112">Un archivo tiene una versión</span><span class="sxs-lookup"><span data-stu-id="d8d6f-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



