---
description: 'El sistema almacena información de Perfil de usuario en un directorio específico, que tiene nombres diferentes en versiones diferentes de Windows: &\# 0034; Documents and settings&\# 0034; en Windows XP y &\# 0034; Usuarios&\# 0034; en Windows Vista y versiones posteriores.'
title: Directorio de perfiles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985635"
---
# <a name="profiles-directory"></a><span data-ttu-id="832c4-103">Directorio de perfiles</span><span class="sxs-lookup"><span data-stu-id="832c4-103">Profiles Directory</span></span>

<span data-ttu-id="832c4-104">El sistema almacena información de Perfil de usuario en un directorio específico, que tiene nombres diferentes en versiones diferentes de Windows: "Documents and Settings" en Windows XP y "Users" en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="832c4-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="832c4-105">Para obtener la ruta de acceso del directorio de perfiles, utilice la función [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="832c4-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="832c4-106">El directorio de perfiles contiene los siguientes subdirectorios para los perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="832c4-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="832c4-107">Directorio</span><span class="sxs-lookup"><span data-stu-id="832c4-107">Directory</span></span>                                      | <span data-ttu-id="832c4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="832c4-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="832c4-109">ProgramData (Windows Vista o posterior)/all usuarios</span><span class="sxs-lookup"><span data-stu-id="832c4-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="832c4-110">Información del programa que se aplica a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="832c4-110">Program information that applies to all users.</span></span> <span data-ttu-id="832c4-111">El directorio todos los usuarios sigue existiendo en Windows Vista o posterior, por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="832c4-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="832c4-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="832c4-112">Default</span></span>                                        | <span data-ttu-id="832c4-113">Información de perfil que se aplica al usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="832c4-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="832c4-114">*User*</span><span class="sxs-lookup"><span data-stu-id="832c4-114">*User*</span></span>                                         | <span data-ttu-id="832c4-115">Información de perfil que se aplica al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="832c4-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="832c4-116">Cada usuario tiene su propio subdirectorio de perfil.</span><span class="sxs-lookup"><span data-stu-id="832c4-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="832c4-117">Para obtener la ubicación del directorio ProgramData/All Users, llame a la función [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="832c4-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="832c4-118">Este directorio raíz contiene los siguientes subdirectorios:</span><span class="sxs-lookup"><span data-stu-id="832c4-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="832c4-119">Directorio</span><span class="sxs-lookup"><span data-stu-id="832c4-119">Directory</span></span>  | <span data-ttu-id="832c4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="832c4-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="832c4-121">Escritorio</span><span class="sxs-lookup"><span data-stu-id="832c4-121">Desktop</span></span>    | <span data-ttu-id="832c4-122">Accesos directos que se van a mostrar en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="832c4-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="832c4-123">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="832c4-123">Start Menu</span></span> | <span data-ttu-id="832c4-124">Elementos de menú para el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="832c4-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="832c4-125">Para obtener la ubicación del directorio del usuario predeterminado, llame a la función [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="832c4-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="832c4-126">Para obtener la ubicación del directorio de un usuario determinado, llame a la función [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="832c4-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="832c4-127">El usuario predeterminado y los directorios de usuario específicos contienen los siguientes subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="832c4-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="832c4-128">Los directorios en cursiva indican directorios que están ocultos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="832c4-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="832c4-129">Puede ver estos directorios seleccionando la opción **Mostrar archivos, carpetas y unidades ocultos** en el elemento del panel de control **Opciones de carpeta** .</span><span class="sxs-lookup"><span data-stu-id="832c4-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="832c4-130">Directorio</span><span class="sxs-lookup"><span data-stu-id="832c4-130">Directory</span></span></th>
<th><span data-ttu-id="832c4-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="832c4-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="832c4-132">Datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="832c4-132">Application Data</span></span></td>
<td><span data-ttu-id="832c4-133">Datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="832c4-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-134">Cookies</span><span class="sxs-lookup"><span data-stu-id="832c4-134">Cookies</span></span></td>
<td><span data-ttu-id="832c4-135">Cookies de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="832c4-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="832c4-136">Escritorio</span><span class="sxs-lookup"><span data-stu-id="832c4-136">Desktop</span></span></td>
<td><span data-ttu-id="832c4-137">Accesos directos que se van a mostrar en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="832c4-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-138">Favoritos</span><span class="sxs-lookup"><span data-stu-id="832c4-138">Favorites</span></span></td>
<td><span data-ttu-id="832c4-139">Vínculos a sitios web favoritos.</span><span class="sxs-lookup"><span data-stu-id="832c4-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="832c4-140">Configuración local</span><span class="sxs-lookup"><span data-stu-id="832c4-140">Local Settings</span></span></td>
<td><span data-ttu-id="832c4-141">La configuración de la aplicación y los datos que no se mueven con el perfil.</span><span class="sxs-lookup"><span data-stu-id="832c4-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="832c4-142">Normalmente, la configuración o los datos de este directorio son específicos del equipo, o bien son demasiado grandes para moverse de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="832c4-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="832c4-143">Este directorio contiene las siguientes subcarpetas:</span><span class="sxs-lookup"><span data-stu-id="832c4-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="832c4-144">Datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="832c4-144">Application Data</span></span></li>
<li><span data-ttu-id="832c4-145">Historial</span><span class="sxs-lookup"><span data-stu-id="832c4-145">History</span></span></li>
<li><span data-ttu-id="832c4-146">Temp</span><span class="sxs-lookup"><span data-stu-id="832c4-146">Temp</span></span></li>
<li><span data-ttu-id="832c4-147">Archivos temporales de Internet</span><span class="sxs-lookup"><span data-stu-id="832c4-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-148">Mis documentos</span><span class="sxs-lookup"><span data-stu-id="832c4-148">My Documents</span></span></td>
<td><span data-ttu-id="832c4-149">La ubicación predeterminada de los documentos que el usuario crea.</span><span class="sxs-lookup"><span data-stu-id="832c4-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="832c4-150">De forma predeterminada, las aplicaciones deben guardar los archivos de documento en este directorio.</span><span class="sxs-lookup"><span data-stu-id="832c4-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="832c4-151"><em>NetHood</em></span><span class="sxs-lookup"><span data-stu-id="832c4-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="832c4-152">Accesos directos a elementos de entorno de red.</span><span class="sxs-lookup"><span data-stu-id="832c4-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-153"><em>PrintHood</em></span><span class="sxs-lookup"><span data-stu-id="832c4-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="832c4-154">Accesos directos a elementos de carpeta de impresora.</span><span class="sxs-lookup"><span data-stu-id="832c4-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="832c4-155"><em>Recientes</em></span><span class="sxs-lookup"><span data-stu-id="832c4-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="832c4-156">Accesos directos a los documentos usados más recientemente.</span><span class="sxs-lookup"><span data-stu-id="832c4-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="832c4-157">SendTo</span></span></td>
<td><span data-ttu-id="832c4-158">Accesos directos a ubicaciones a las que el usuario suele enviar archivos.</span><span class="sxs-lookup"><span data-stu-id="832c4-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="832c4-159">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="832c4-159">Start Menu</span></span></td>
<td><span data-ttu-id="832c4-160">Elementos de menú para el menú <strong>Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="832c4-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="832c4-161"><em>Templates</em> (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="832c4-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="832c4-162">Accesos directos a elementos de plantilla.</span><span class="sxs-lookup"><span data-stu-id="832c4-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="832c4-163">Para obtener la ubicación de los subdirectorios de estos directorios, use las funciones [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) o [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .</span><span class="sxs-lookup"><span data-stu-id="832c4-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



