---
description: Cargando recursos de idioma
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Cargando recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361660"
---
# <a name="loading-language-resources"></a><span data-ttu-id="6b4f0-103">Cargando recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="6b4f0-103">Loading Language Resources</span></span>

<span data-ttu-id="6b4f0-104">La aplicación carga todos los recursos de idioma de interfaz de usuario, excepto ciertas cadenas de registro redirigidas, mediante llamadas a funciones de carga de recursos estándar, por ejemplo, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)y [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span><span class="sxs-lookup"><span data-stu-id="6b4f0-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="6b4f0-105">Muchas funciones de carga de recursos se han modificado para cargar los recursos de los archivos de recursos específicos del idioma automáticamente, tratando los recursos como si estuvieran incluidos en el archivo LN.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="6b4f0-106">En el ejemplo siguiente se muestra el uso de **LoadString** para cargar cadenas de idioma para una aplicación que sigue la configuración de idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="6b4f0-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b4f0-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4f0-108">Ubicar recursos PE de Win32</span><span class="sxs-lookup"><span data-stu-id="6b4f0-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
