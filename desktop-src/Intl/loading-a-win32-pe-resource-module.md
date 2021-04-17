---
description: En este tema se describe cómo la aplicación carga un módulo de recursos de Win32 PE en Windows Vista y versiones posteriores, o en un sistema operativo anterior. Se incluyen llamadas para liberar el módulo de recursos.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Carga de un módulo de recursos de Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669937"
---
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="df09b-104">Carga de un módulo de recursos de Win32 PE</span><span class="sxs-lookup"><span data-stu-id="df09b-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="df09b-105">En este tema se describe cómo la aplicación carga un módulo de recursos de Win32 PE en Windows Vista y versiones posteriores, o en un sistema operativo anterior.</span><span class="sxs-lookup"><span data-stu-id="df09b-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="df09b-106">Se incluyen llamadas para liberar el módulo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df09b-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="df09b-107">Cargar el módulo de recursos en Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="df09b-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="df09b-108">En Windows Vista y versiones posteriores, la aplicación carga el módulo de recursos mediante una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="df09b-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="df09b-109">La operación recomendada es llamar a esta función con las dos marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="df09b-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="df09b-110">El siguiente es un ejemplo de código de aplicación que carga un módulo basado en la configuración de idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="df09b-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="df09b-111">Cargar el módulo de recursos en sistemas operativos anteriores a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df09b-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="df09b-112">En los sistemas operativos anteriores a Windows Vista, la aplicación carga un módulo de recursos basado en una configuración de idioma que es compatible con el sistema operativo de destino, así como con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="df09b-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="df09b-113">Para este tipo de carga de módulos, la aplicación debe llamar a las funciones de MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span><span class="sxs-lookup"><span data-stu-id="df09b-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="df09b-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df09b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df09b-115">Ubicar recursos PE de Win32</span><span class="sxs-lookup"><span data-stu-id="df09b-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="df09b-116">MUI: ejemplo de configuración de Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="df09b-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="df09b-117">MUI: ejemplo de configuración de Application-Specific (anterior a Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="df09b-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
