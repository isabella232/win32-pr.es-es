---
description: El hash de archivo está disponible con Windows Installer. Para obtener más información, vea MsiGetFileHash y la tabla MsiFileHash. La tabla MsiFileHash solo se puede usar con archivos sin versión.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Ninguno de los archivos tiene una versión con comprobación de hash de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544254"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="3f8de-105">Ninguno de los archivos tiene una versión con comprobación de hash de archivo</span><span class="sxs-lookup"><span data-stu-id="3f8de-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="3f8de-106">El hash de archivo está disponible con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3f8de-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="3f8de-107">Para obtener más información, vea [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f8de-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="3f8de-108">La tabla MsiFileHash solo se puede usar con archivos sin versión.</span><span class="sxs-lookup"><span data-stu-id="3f8de-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="3f8de-109">Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.</span><span class="sxs-lookup"><span data-stu-id="3f8de-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="3f8de-110">Si ninguno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.</span><span class="sxs-lookup"><span data-stu-id="3f8de-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="3f8de-111">Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.</span><span class="sxs-lookup"><span data-stu-id="3f8de-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="3f8de-112">Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="3f8de-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="3f8de-113">El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".</span><span class="sxs-lookup"><span data-stu-id="3f8de-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![reglas predeterminadas de control de versiones de archivo cuando se invalida con la configuración de la propiedad REINSTALLMODE](images/waiflow2b.png)

<span data-ttu-id="3f8de-115">Vea los ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="3f8de-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="3f8de-116">Ambos archivos tienen una versión</span><span class="sxs-lookup"><span data-stu-id="3f8de-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="3f8de-117">Ninguno de los archivos tiene una versión</span><span class="sxs-lookup"><span data-stu-id="3f8de-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="3f8de-118">Un archivo tiene una versión</span><span class="sxs-lookup"><span data-stu-id="3f8de-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



