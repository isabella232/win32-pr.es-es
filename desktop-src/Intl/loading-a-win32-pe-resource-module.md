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
# <a name="loading-a-win32-pe-resource-module"></a>Carga de un módulo de recursos de Win32 PE

En este tema se describe cómo la aplicación carga un módulo de recursos de Win32 PE en Windows Vista y versiones posteriores, o en un sistema operativo anterior. Se incluyen llamadas para liberar el módulo de recursos.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Cargar el módulo de recursos en Windows Vista y versiones posteriores

En Windows Vista y versiones posteriores, la aplicación carga el módulo de recursos mediante una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa). La operación recomendada es llamar a esta función con las dos marcas especificadas. El siguiente es un ejemplo de código de aplicación que carga un módulo basado en la configuración de idioma del sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Cargar el módulo de recursos en sistemas operativos anteriores a Windows Vista

En los sistemas operativos anteriores a Windows Vista, la aplicación carga un módulo de recursos basado en una configuración de idioma que es compatible con el sistema operativo de destino, así como con Windows Vista y versiones posteriores. Para este tipo de carga de módulos, la aplicación debe llamar a las funciones de MUI [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) y [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ubicar recursos PE de Win32](locating-win32-pe-resources.md)
</dt> <dt>

[MUI: ejemplo de configuración de Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: ejemplo de configuración de Application-Specific (anterior a Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
