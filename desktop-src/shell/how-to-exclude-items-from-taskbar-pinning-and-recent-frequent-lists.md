---
description: Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para el anclaje en la barra de tareas o para su inclusión en la lista de uso más frecuente (MFU) del menú Inicio.
title: Cómo excluir elementos del anclaje de la barra de tareas y listas recientes/frecuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985442"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="942c2-103">Cómo excluir elementos del anclaje de la barra de tareas y listas recientes/frecuentes</span><span class="sxs-lookup"><span data-stu-id="942c2-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="942c2-104">Las aplicaciones, los procesos y las ventanas pueden optar por dejar de estar disponibles para el anclaje en la barra de tareas o para su inclusión en la lista de uso más frecuente (MFU) del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="942c2-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="942c2-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="942c2-105">Instructions</span></span>


<span data-ttu-id="942c2-106">Existen tres mecanismos para conseguir la exclusión de elementos del anclaje de la barra de tareas y listas recientes/frecuentes:</span><span class="sxs-lookup"><span data-stu-id="942c2-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="942c2-107">Agregue la entrada NoStartPage al registro de la aplicación como se muestra en este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="942c2-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="942c2-108">Se omiten los datos asociados a la entrada NoStartPage.</span><span class="sxs-lookup"><span data-stu-id="942c2-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="942c2-109">Solo se requiere la presencia de la entrada.</span><span class="sxs-lookup"><span data-stu-id="942c2-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="942c2-110">Por lo tanto, el tipo ideal para NoStartPage es **reg \_ None**.</span><span class="sxs-lookup"><span data-stu-id="942c2-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="942c2-111">Tenga en cuenta que cualquier uso de un identificador de modelo de usuario de aplicación explícito (AppUserModelID) reemplaza la entrada NoStartPage.</span><span class="sxs-lookup"><span data-stu-id="942c2-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="942c2-112">Si se aplica un AppUserModelID explícito a un acceso directo, proceso o ventana, se convierte en anclable y es válido para la lista de MFU del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="942c2-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="942c2-113">Establezca la propiedad [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) en Windows y los métodos abreviados.</span><span class="sxs-lookup"><span data-stu-id="942c2-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="942c2-114">Esta propiedad se debe establecer en una ventana antes de que se establezca la propiedad [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="942c2-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="942c2-115">Agregue un AppUserModelID explícito como valor en la subclave del Registro siguiente, tal como se muestra en este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="942c2-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="942c2-116">Cada entrada es un valor de **reg \_ null** con el nombre de AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="942c2-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="942c2-117">Cualquier AppUserModelID que se encuentre en esta lista no es anclable y no es válido para su inclusión en la lista de MFU del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="942c2-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="942c2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="942c2-118">Remarks</span></span>

<span data-ttu-id="942c2-119">Tenga en cuenta que determinados archivos ejecutables, así como accesos directos que contienen determinadas cadenas en sus nombres, se excluyen automáticamente del anclaje y la inclusión en la lista de MFU.</span><span class="sxs-lookup"><span data-stu-id="942c2-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="942c2-120">Esta exclusión automática se puede invalidar mediante la aplicación de un AppUserModelID explícito.</span><span class="sxs-lookup"><span data-stu-id="942c2-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="942c2-121">Si alguna de las siguientes cadenas, con independencia del caso, se incluye en el nombre de acceso directo, el programa no se muestra anclado y no se muestra en la lista de elementos usados con mayor frecuencia (no aplicable a Windows 10):</span><span class="sxs-lookup"><span data-stu-id="942c2-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="942c2-122">Documentación</span><span class="sxs-lookup"><span data-stu-id="942c2-122">Documentation</span></span>
-   <span data-ttu-id="942c2-123">Ayuda</span><span class="sxs-lookup"><span data-stu-id="942c2-123">Help</span></span>
-   <span data-ttu-id="942c2-124">Instalar</span><span class="sxs-lookup"><span data-stu-id="942c2-124">Install</span></span>
-   <span data-ttu-id="942c2-125">Más información</span><span class="sxs-lookup"><span data-stu-id="942c2-125">More Info</span></span>
-   <span data-ttu-id="942c2-126">Léame</span><span class="sxs-lookup"><span data-stu-id="942c2-126">Read me</span></span>
-   <span data-ttu-id="942c2-127">Leer primero</span><span class="sxs-lookup"><span data-stu-id="942c2-127">Read First</span></span>
-   <span data-ttu-id="942c2-128">Léame</span><span class="sxs-lookup"><span data-stu-id="942c2-128">Readme</span></span>
-   <span data-ttu-id="942c2-129">Quitar</span><span class="sxs-lookup"><span data-stu-id="942c2-129">Remove</span></span>
-   <span data-ttu-id="942c2-130">Configurar</span><span class="sxs-lookup"><span data-stu-id="942c2-130">Setup</span></span>
-   <span data-ttu-id="942c2-131">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="942c2-131">Support</span></span>
-   <span data-ttu-id="942c2-132">Novedades</span><span class="sxs-lookup"><span data-stu-id="942c2-132">What's New</span></span>

<span data-ttu-id="942c2-133">La siguiente lista de programas no es anclable y se excluyen de la lista de uso más frecuente:</span><span class="sxs-lookup"><span data-stu-id="942c2-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="942c2-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-134">Applaunch.exe</span></span>
-   <span data-ttu-id="942c2-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-135">Control.exe</span></span>
-   <span data-ttu-id="942c2-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="942c2-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-137">Dllhost.exe</span></span>
-   <span data-ttu-id="942c2-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="942c2-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-139">Hh.exe</span></span>
-   <span data-ttu-id="942c2-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-140">Install.exe</span></span>
-   <span data-ttu-id="942c2-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-141">Isuninst.exe</span></span>
-   <span data-ttu-id="942c2-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="942c2-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-143">Mmc.exe</span></span>
-   <span data-ttu-id="942c2-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-144">Mshta.exe</span></span>
-   <span data-ttu-id="942c2-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-145">Msiexec.exe</span></span>
-   <span data-ttu-id="942c2-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-146">Msoobe.exe</span></span>
-   <span data-ttu-id="942c2-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-147">Rundll32.exe</span></span>
-   <span data-ttu-id="942c2-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-148">Setup.exe</span></span>
-   <span data-ttu-id="942c2-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-149">St5unst.exe</span></span>
-   <span data-ttu-id="942c2-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-150">Unwise.exe</span></span>
-   <span data-ttu-id="942c2-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-151">Unwise32.exe</span></span>
-   <span data-ttu-id="942c2-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-152">Werfault.exe</span></span>
-   <span data-ttu-id="942c2-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="942c2-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="942c2-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="942c2-155">Wuapp.exe</span></span>

<span data-ttu-id="942c2-156">Las listas anteriores se almacenan en los siguientes valores del registro.</span><span class="sxs-lookup"><span data-stu-id="942c2-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="942c2-157">Las aplicaciones no deben modificar estas listas.</span><span class="sxs-lookup"><span data-stu-id="942c2-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="942c2-158">Use uno de los métodos de lista de exclusión descritos anteriormente en este tema para obtener la misma experiencia.</span><span class="sxs-lookup"><span data-stu-id="942c2-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="942c2-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="942c2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942c2-160">La barra de tareas</span><span class="sxs-lookup"><span data-stu-id="942c2-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="942c2-161">Extensiones de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="942c2-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
