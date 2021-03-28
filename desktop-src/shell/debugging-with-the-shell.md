---
description: En este tema se explica cómo depurar los archivos dll de extensión de espacio de nombres y Shell.
title: Depuración con el shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540531"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="7115d-103">Depuración con el shell</span><span class="sxs-lookup"><span data-stu-id="7115d-103">Debugging with the Shell</span></span>

<span data-ttu-id="7115d-104">En este tema se explica cómo depurar los archivos dll de extensión de espacio de nombres y Shell.</span><span class="sxs-lookup"><span data-stu-id="7115d-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="7115d-105">Ejecutar el Shell en un depurador</span><span class="sxs-lookup"><span data-stu-id="7115d-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="7115d-106">Ejecutar y probar extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="7115d-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="7115d-107">Descargar el archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7115d-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="7115d-108">Ejecutar el Shell en un depurador</span><span class="sxs-lookup"><span data-stu-id="7115d-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="7115d-109">Para depurar la extensión, debe ejecutar el shell desde el depurador.</span><span class="sxs-lookup"><span data-stu-id="7115d-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="7115d-110">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="7115d-110">Follow these steps:</span></span>

1.  <span data-ttu-id="7115d-111">Cargue el proyecto de la extensión en el depurador, pero no lo ejecute.</span><span class="sxs-lookup"><span data-stu-id="7115d-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="7115d-112">Cierre el shell.</span><span class="sxs-lookup"><span data-stu-id="7115d-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="7115d-113">Para Windows Vista y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="7115d-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="7115d-114">Mostrar el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="7115d-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="7115d-115">Presione CTRL + MAYÚS y haga clic con el botón secundario en el fondo de la mitad derecha del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="7115d-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="7115d-116">En el menú que aparece, elija **salir del explorador**.</span><span class="sxs-lookup"><span data-stu-id="7115d-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="7115d-117">Para Windows XP:</span><span class="sxs-lookup"><span data-stu-id="7115d-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="7115d-118">En el menú **Inicio** , elija **apagar**.</span><span class="sxs-lookup"><span data-stu-id="7115d-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="7115d-119">Presione CTRL + ALT + MAYÚS y haga clic en **no** en el cuadro de diálogo **cerrar Windows** .</span><span class="sxs-lookup"><span data-stu-id="7115d-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="7115d-120">El Shell se ha cerrado, pero todas las demás aplicaciones todavía se están ejecutando, incluido el depurador.</span><span class="sxs-lookup"><span data-stu-id="7115d-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="7115d-121">Establezca el depurador para ejecutar el archivo DLL de extensión con Explorer.exe desde el directorio de **Windows** .</span><span class="sxs-lookup"><span data-stu-id="7115d-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="7115d-122">Ejecute el proyecto desde el depurador.</span><span class="sxs-lookup"><span data-stu-id="7115d-122">Run the project from the debugger.</span></span> <span data-ttu-id="7115d-123">El Shell se iniciará como de costumbre, pero el depurador se adjuntará al proceso del shell.</span><span class="sxs-lookup"><span data-stu-id="7115d-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="7115d-124">Ejecutar y probar extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="7115d-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="7115d-125">Puede ejecutar y probar las extensiones en un proceso independiente del explorador de Windows para evitar detener y reiniciar el escritorio y la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="7115d-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="7115d-126">El escritorio y la barra de tareas se pueden seguir usando mientras ejecuta y prueba las extensiones.</span><span class="sxs-lookup"><span data-stu-id="7115d-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="7115d-127">Para habilitar esta característica, agregue la siguiente \_ entrada REG DWORD al registro.</span><span class="sxs-lookup"><span data-stu-id="7115d-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="7115d-128">Para que esta entrada surta efecto, debe cerrar la sesión y volver a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="7115d-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="7115d-129">Esta configuración hace que las ventanas del escritorio y de la barra de tareas se creen en un proceso Explorer.exe y en el resto de las ventanas del explorador y de las carpetas que se van a abrir en otro proceso de Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="7115d-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="7115d-130">Además de hacer que la ejecución y las pruebas de las extensiones sean más cómodas, esta opción también hace que el escritorio sea más sólido en lo relacionado con las extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="7115d-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="7115d-131">Muchas de estas extensiones (por ejemplo, extensiones de menú contextual) se cargarán en el proceso de Explorer.exe de no escritorio.</span><span class="sxs-lookup"><span data-stu-id="7115d-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="7115d-132">Si finaliza este proceso, el escritorio y la barra de tareas no se verán afectados y la siguiente ventana explorador o carpeta volverá a crear el proceso terminado.</span><span class="sxs-lookup"><span data-stu-id="7115d-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="7115d-133">Descargar el archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7115d-133">Unloading the DLL</span></span>

<span data-ttu-id="7115d-134">El shell descarga automáticamente cualquier archivo DLL cuando su recuento de uso es cero, pero solo después de que el archivo DLL no se haya usado durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7115d-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="7115d-135">Este período inactivo puede ser inaceptablemente largo a veces, especialmente cuando se depura un archivo DLL de extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="7115d-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="7115d-136">Puede acortar el período inactivo agregando la siguiente información al registro.</span><span class="sxs-lookup"><span data-stu-id="7115d-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



