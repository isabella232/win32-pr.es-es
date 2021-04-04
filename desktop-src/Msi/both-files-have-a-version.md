---
description: Si ambos archivos tienen un número de versión, el Windows Installer usa la lógica que se ilustra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Ambos archivos tienen una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909046"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="42f48-103">Ambos archivos tienen una versión</span><span class="sxs-lookup"><span data-stu-id="42f48-103">Both Files Have a Version</span></span>

<span data-ttu-id="42f48-104">Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión y el idioma de los dos archivos.</span><span class="sxs-lookup"><span data-stu-id="42f48-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="42f48-105">Si ambos archivos tienen un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.</span><span class="sxs-lookup"><span data-stu-id="42f48-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="42f48-106">Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.</span><span class="sxs-lookup"><span data-stu-id="42f48-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="42f48-107">Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="42f48-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="42f48-108">El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".</span><span class="sxs-lookup"><span data-stu-id="42f48-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![reglas predeterminadas de control de versiones de archivo cuando ambos archivos tienen el mismo nombre o número de versión](images/waiflow1.png)

<span data-ttu-id="42f48-110">El diagrama anterior también se puede usar con archivos sin idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="42f48-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="42f48-111">Si Copy-A tiene un idioma especificado y Copy-B no tiene ningún idioma especificado, Copy-B se reemplaza por Copy-A.</span><span class="sxs-lookup"><span data-stu-id="42f48-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="42f48-112">Si no se especifica ningún idioma para Copy-A y Copy-B, no se reemplazará Copy-B.</span><span class="sxs-lookup"><span data-stu-id="42f48-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="42f48-113">Vea ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="42f48-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="42f48-114">Ninguno de los archivos tiene una versión</span><span class="sxs-lookup"><span data-stu-id="42f48-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="42f48-115">Ninguno de los archivos tiene una versión con comprobación de hash de archivo</span><span class="sxs-lookup"><span data-stu-id="42f48-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="42f48-116">Un archivo tiene una versión</span><span class="sxs-lookup"><span data-stu-id="42f48-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



