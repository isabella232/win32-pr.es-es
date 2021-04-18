---
description: ICE64 comprueba que los nuevos directorios del perfil de usuario se han quitado correctamente en escenarios móviles.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546139"
---
# <a name="ice64"></a><span data-ttu-id="0dee5-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="0dee5-103">ICE64</span></span>

<span data-ttu-id="0dee5-104">ICE64 comprueba que los nuevos directorios del perfil de usuario se han quitado correctamente en escenarios móviles.</span><span class="sxs-lookup"><span data-stu-id="0dee5-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="0dee5-105">Si no se corrige una advertencia o un error informados por ICE64, generalmente se producen problemas al limpiar completamente el equipo durante una desinstalación.</span><span class="sxs-lookup"><span data-stu-id="0dee5-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="0dee5-106">Cuando un usuario móvil que ha instalado la aplicación inicia sesión en un equipo por primera vez, se copia todo el perfil en el equipo.</span><span class="sxs-lookup"><span data-stu-id="0dee5-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="0dee5-107">En el anuncio (que tiene lugar después de la descarga del perfil móvil), el instalador comprueba que el directorio ya existe y, por tanto, no lo elimina durante la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="0dee5-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="0dee5-108">Esto deja el directorio en el equipo del usuario de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="0dee5-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="0dee5-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="0dee5-109">Result</span></span>

<span data-ttu-id="0dee5-110">ICE64 envía una advertencia o un error en una situación de itinerancia si no se quita un nuevo directorio del perfil de usuario que se debe quitar.</span><span class="sxs-lookup"><span data-stu-id="0dee5-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="0dee5-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dee5-111">Example</span></span>

<span data-ttu-id="0dee5-112">ICE64 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="0dee5-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="0dee5-113">La carpeta ' MyOtherFolder ' es una carpeta de perfil personalizada.</span><span class="sxs-lookup"><span data-stu-id="0dee5-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="0dee5-114">Dado que no aparece en la tabla RemoveFile, no se quita en algunos escenarios.</span><span class="sxs-lookup"><span data-stu-id="0dee5-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="0dee5-115">Para corregir este error, cree una fila para la carpeta en la tabla RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="0dee5-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="0dee5-116">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="0dee5-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="0dee5-117">Directorio</span><span class="sxs-lookup"><span data-stu-id="0dee5-117">Directory</span></span>     | <span data-ttu-id="0dee5-118">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="0dee5-118">Directory\_Parent</span></span> | <span data-ttu-id="0dee5-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="0dee5-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="0dee5-120">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-120">AppDataFolder</span></span> | <span data-ttu-id="0dee5-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="0dee5-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="0dee5-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-122">MyFolder</span></span>      | <span data-ttu-id="0dee5-123">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-123">AppDataFolder</span></span>     | <span data-ttu-id="0dee5-124">Subcarpeta</span><span class="sxs-lookup"><span data-stu-id="0dee5-124">DataFolder</span></span>  |
| <span data-ttu-id="0dee5-125">MyOtherFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-125">MyOtherFolder</span></span> | <span data-ttu-id="0dee5-126">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-126">AppDataFolder</span></span>     | <span data-ttu-id="0dee5-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="0dee5-127">DataFolder2</span></span> |



 

[<span data-ttu-id="0dee5-128">Tabla RemoveFile</span><span class="sxs-lookup"><span data-stu-id="0dee5-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="0dee5-129">FileKey</span><span class="sxs-lookup"><span data-stu-id="0dee5-129">FileKey</span></span> | <span data-ttu-id="0dee5-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="0dee5-130">Component\_</span></span> | <span data-ttu-id="0dee5-131">FileName</span><span class="sxs-lookup"><span data-stu-id="0dee5-131">FileName</span></span> | <span data-ttu-id="0dee5-132">DirProperty</span><span class="sxs-lookup"><span data-stu-id="0dee5-132">DirProperty</span></span> | <span data-ttu-id="0dee5-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="0dee5-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="0dee5-134">Tecla1</span><span class="sxs-lookup"><span data-stu-id="0dee5-134">Key1</span></span>    | <span data-ttu-id="0dee5-135">Component1</span><span class="sxs-lookup"><span data-stu-id="0dee5-135">Component1</span></span>  |          | <span data-ttu-id="0dee5-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="0dee5-136">MyFolder</span></span>    | <span data-ttu-id="0dee5-137">2</span><span class="sxs-lookup"><span data-stu-id="0dee5-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="0dee5-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0dee5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dee5-139">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="0dee5-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



