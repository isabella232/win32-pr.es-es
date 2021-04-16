---
description: Si ninguno de los archivos tiene un número de versión, el Windows Installer utiliza la lógica que se ilustra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Ninguno de los archivos tiene una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551543"
---
# <a name="neither-file-has-a-version"></a><span data-ttu-id="06f20-103">Ninguno de los archivos tiene una versión</span><span class="sxs-lookup"><span data-stu-id="06f20-103">Neither File Has a Version</span></span>

<span data-ttu-id="06f20-104">Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.</span><span class="sxs-lookup"><span data-stu-id="06f20-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="06f20-105">Si ninguno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.</span><span class="sxs-lookup"><span data-stu-id="06f20-105">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="06f20-106">Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.</span><span class="sxs-lookup"><span data-stu-id="06f20-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="06f20-107">Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="06f20-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="06f20-108">El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".</span><span class="sxs-lookup"><span data-stu-id="06f20-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![reglas predeterminadas de control de versiones de archivo cuando ningún archivo tiene un número de versión](images/waiflow2.png)

<span data-ttu-id="06f20-110">Vea los ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="06f20-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="06f20-111">Ambos archivos tienen una versión</span><span class="sxs-lookup"><span data-stu-id="06f20-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="06f20-112">Ninguno de los archivos tiene una versión con comprobación de hash de archivo</span><span class="sxs-lookup"><span data-stu-id="06f20-112">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="06f20-113">Un archivo tiene una versión</span><span class="sxs-lookup"><span data-stu-id="06f20-113">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



