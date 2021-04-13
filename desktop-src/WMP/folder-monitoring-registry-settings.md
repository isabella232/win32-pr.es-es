---
title: Configuración del registro de supervisión de carpetas
description: Configuración del registro de supervisión de carpetas
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, configuración del registro de supervisión de carpetas
- Windows Media Player, configuración del registro de supervisión de carpetas de archivos
- Media Player de Windows, registro
- registro, configuración de supervisión de carpetas
- configuración de supervisión de carpeta de archivos, registro
- registro, configuración para Windows Media Player
- configuración del registro de supervisión de carpetas
- configuración del registro de supervisión de carpeta de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421526"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="90dc4-111">Configuración del registro de supervisión de carpetas</span><span class="sxs-lookup"><span data-stu-id="90dc4-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="90dc4-112">Windows Media Player 9 series o posterior pueden supervisar las carpetas de archivos para los nuevos archivos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="90dc4-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="90dc4-113">Cuando el reproductor detecta un nuevo archivo en una carpeta supervisada, agrega automáticamente el archivo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="90dc4-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="90dc4-114">En el caso de Windows Media Player 9 a Windows Media Player 11, los usuarios pueden cambiar la lista de carpetas supervisadas haciendo clic en **supervisar carpetas** en la pestaña biblioteca del cuadro de diálogo **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="90dc4-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="90dc4-115">En Windows Media Player 12, un usuario puede cambiar la lista de carpetas supervisadas siguiendo las instrucciones del tema [Agregar elementos a la biblioteca de Windows Media Player](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span><span class="sxs-lookup"><span data-stu-id="90dc4-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="90dc4-116">En Windows Media Player 9 a Windows Media Player 11, puede agregar mediante programación una carpeta para su supervisión agregando un valor al registro.</span><span class="sxs-lookup"><span data-stu-id="90dc4-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="90dc4-117">En Windows Media Player 12, no puede usar el registro para agregar o quitar mediante programación las carpetas que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="90dc4-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="90dc4-118">En Windows Media Player 9 a Windows Media Player 11, para agregar una carpeta que se va a supervisar, primero debe crear o modificar dos valores en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="90dc4-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="90dc4-119">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Preferences\\**</span><span class="sxs-lookup"><span data-stu-id="90dc4-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="90dc4-120">Los valores nuevos deben tener el nombre siguiente.</span><span class="sxs-lookup"><span data-stu-id="90dc4-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="90dc4-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="90dc4-121">Name</span></span>                           | <span data-ttu-id="90dc4-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="90dc4-122">Type</span></span>           | <span data-ttu-id="90dc4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="90dc4-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dc4-124">**TrackFoldersDirectories**</span><span class="sxs-lookup"><span data-stu-id="90dc4-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="90dc4-125">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="90dc4-125">**REG\_DWORD**</span></span> | <span data-ttu-id="90dc4-126">Valor **DWORD** que representa el recuento de carpetas que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="90dc4-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="90dc4-127">Debe coincidir con el número de valores \*\*TrackFoldersDirectories \*\* \* \* X.</span><span class="sxs-lookup"><span data-stu-id="90dc4-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="90dc4-128">\**TrackFoldersDirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="90dc4-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="90dc4-129">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="90dc4-129">**REG\_SZ**</span></span>    | <span data-ttu-id="90dc4-130">Valor de cadena que representa la ruta de acceso de la carpeta que se va a supervisar.</span><span class="sxs-lookup"><span data-stu-id="90dc4-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="90dc4-131">Cada carpeta que se va a supervisar requiere un valor independiente.</span><span class="sxs-lookup"><span data-stu-id="90dc4-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="90dc4-132">El sufijo *X* es un entero que siempre debe comenzar en 0 y, a continuación, incrementar en 1.</span><span class="sxs-lookup"><span data-stu-id="90dc4-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="90dc4-133">Windows Media Player también supervisa las subcarpetas de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="90dc4-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="90dc4-134">Por ejemplo, para agregar la primera carpeta que se va a supervisar, agregue el valor siguiente:</span><span class="sxs-lookup"><span data-stu-id="90dc4-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="90dc4-135">A continuación, cree el valor de recuento:</span><span class="sxs-lookup"><span data-stu-id="90dc4-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="90dc4-136">Para agregar una segunda carpeta para supervisar, agregue el valor siguiente:</span><span class="sxs-lookup"><span data-stu-id="90dc4-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="90dc4-137">A continuación, incremente el valor de recuento:</span><span class="sxs-lookup"><span data-stu-id="90dc4-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="90dc4-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90dc4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90dc4-139">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="90dc4-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




