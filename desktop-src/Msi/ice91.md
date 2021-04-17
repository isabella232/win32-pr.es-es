---
description: ICE91 publica una advertencia si un archivo, archivo. ini o archivo de acceso directo se instala en un directorio solo por usuario.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652945"
---
# <a name="ice91"></a><span data-ttu-id="f1c32-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="f1c32-103">ICE91</span></span>

<span data-ttu-id="f1c32-104">ICE91 publica una advertencia si un archivo, archivo. ini o archivo de acceso directo se instala en un directorio solo por usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c32-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="f1c32-105">Estas advertencias son inocuas si el paquete solo se usa para la instalación en el [contexto de instalación](installation-context.md) por usuario y nunca se usa para las instalaciones por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="f1c32-106">Los archivos, los archivos. ini o los accesos directos de los directorios de solo usuario se instalan en el perfil de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="f1c32-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="f1c32-107">Incluso si el usuario establece la propiedad [**AllUsers**](allusers.md) para las instalaciones por equipo, los archivos, los archivos. ini o los accesos directos de los directorios de solo usuario no se copian en el perfil "todos los usuarios" y no están disponibles para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="f1c32-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="f1c32-108">Los directorios solo por usuario no varían con la propiedad **AllUsers** .</span><span class="sxs-lookup"><span data-stu-id="f1c32-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="f1c32-109">A continuación se muestra una lista de los directorios solo por usuario:</span><span class="sxs-lookup"><span data-stu-id="f1c32-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="f1c32-110">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-110">AppDataFolder</span></span>
-   <span data-ttu-id="f1c32-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-111">FavoritesFolder</span></span>
-   <span data-ttu-id="f1c32-112">NetHoodFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-112">NetHoodFolder</span></span>
-   <span data-ttu-id="f1c32-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-113">PersonalFolder</span></span>
-   <span data-ttu-id="f1c32-114">PrintHoodFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="f1c32-115">RecentFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-115">RecentFolder</span></span>
-   <span data-ttu-id="f1c32-116">SendToFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-116">SendToFolder</span></span>
-   <span data-ttu-id="f1c32-117">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="f1c32-118">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="f1c32-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="f1c32-119">Result</span></span>

<span data-ttu-id="f1c32-120">ICE91 expone las siguientes advertencias.</span><span class="sxs-lookup"><span data-stu-id="f1c32-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="f1c32-121">ADVERTENCIA de ICE91</span><span class="sxs-lookup"><span data-stu-id="f1c32-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="f1c32-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1c32-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c32-123">El archivo ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 \] ', que no varía según el valor de [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c32-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="f1c32-124">Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="f1c32-125">El archivo se instala en un directorio solo por usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c32-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="f1c32-126">No se instala en el perfil de cada usuario durante una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="f1c32-127">El IniFile ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 \] ', que no varía según el valor de [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c32-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="f1c32-128">Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="f1c32-129">El archivo. ini se instala en un directorio solo por usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c32-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="f1c32-130">No se instala en el perfil de cada usuario durante una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="f1c32-131">El acceso directo ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 ', \] que no varía según el valor de [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c32-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="f1c32-132">Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="f1c32-133">El acceso directo se instala en un directorio solo por usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c32-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="f1c32-134">No se instala en el perfil de cada usuario durante una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="f1c32-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="f1c32-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1c32-135">Example</span></span>

<span data-ttu-id="f1c32-136">ICE91 notifica las siguientes advertencias para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f1c32-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="f1c32-137">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f1c32-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="f1c32-138">Archivo</span><span class="sxs-lookup"><span data-stu-id="f1c32-138">File</span></span>  | <span data-ttu-id="f1c32-139">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f1c32-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="f1c32-140">Archivo1</span><span class="sxs-lookup"><span data-stu-id="f1c32-140">File1</span></span> | <span data-ttu-id="f1c32-141">C1</span><span class="sxs-lookup"><span data-stu-id="f1c32-141">C1</span></span>          |



 

<span data-ttu-id="f1c32-142">[Tabla de componentes](component-table.md) (parcial) (parcial) (parcial) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f1c32-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="f1c32-143">Componente</span><span class="sxs-lookup"><span data-stu-id="f1c32-143">Component</span></span> | <span data-ttu-id="f1c32-144">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="f1c32-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="f1c32-145">C1</span><span class="sxs-lookup"><span data-stu-id="f1c32-145">C1</span></span>        | <span data-ttu-id="f1c32-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-146">MyDir</span></span>       |



 

[<span data-ttu-id="f1c32-147">Tabla IniFile</span><span class="sxs-lookup"><span data-stu-id="f1c32-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="f1c32-148">IniFile</span><span class="sxs-lookup"><span data-stu-id="f1c32-148">IniFile</span></span>  | <span data-ttu-id="f1c32-149">DirProperty</span><span class="sxs-lookup"><span data-stu-id="f1c32-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="f1c32-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="f1c32-150">IniFile1</span></span> | <span data-ttu-id="f1c32-151">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="f1c32-152">Tabla de acceso directo</span><span class="sxs-lookup"><span data-stu-id="f1c32-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="f1c32-153">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="f1c32-153">Shortcut</span></span>  | <span data-ttu-id="f1c32-154">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="f1c32-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="f1c32-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="f1c32-155">Shortcut1</span></span> | <span data-ttu-id="f1c32-156">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="f1c32-157">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="f1c32-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="f1c32-158">Directorio</span><span class="sxs-lookup"><span data-stu-id="f1c32-158">Directory</span></span>     | <span data-ttu-id="f1c32-159">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="f1c32-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="f1c32-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-160">MyDir</span></span>         | <span data-ttu-id="f1c32-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="f1c32-162">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-162">MyIniDir</span></span>      | <span data-ttu-id="f1c32-163">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="f1c32-164">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="f1c32-164">MyShortcutDir</span></span> | <span data-ttu-id="f1c32-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="f1c32-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="f1c32-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c32-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c32-167">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="f1c32-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



