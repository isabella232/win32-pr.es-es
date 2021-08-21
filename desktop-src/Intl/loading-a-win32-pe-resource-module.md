---
description: En este tema se describe cómo la aplicación carga un módulo de recursos de Win32 PE en Windows Vista y versiones posteriores o en un sistema operativo anterior. Se incluyen llamadas para liberar el módulo de recursos.
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: Carga de un módulo de recursos de Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: affcd1cf582d81aafd70f208531e03723ea44b314f92848f35dfd391f950b0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145847"
---
# <a name="loading-a-win32-pe-resource-module"></a>Carga de un módulo de recursos de Win32 PE

En este tema se describe cómo la aplicación carga un módulo de recursos de Win32 PE en Windows Vista y versiones posteriores o en un sistema operativo anterior. Se incluyen llamadas para liberar el módulo de recursos.

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>Carga del módulo de recursos en Windows Vista y versiones posteriores

En Windows Vista y versiones posteriores, la aplicación carga el módulo de recursos mediante una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa) La operación recomendada es llamar a esta función con ambas marcas especificadas. A continuación se muestra un ejemplo de código de aplicación que carga un módulo en función de la configuración del lenguaje del sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>Carga del módulo de recursos en sistemas operativos Windows Vista

En sistemas operativos Windows Vista, la aplicación carga un módulo de recursos basado en una configuración de idioma compatible con el sistema operativo de destino, así como con Windows Vista y versiones posteriores. Para este tipo de carga de módulos, la aplicación debe llamar a las funciones DE LAN [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) [**y FreeMUILibrary.**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda de recursos de Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[MUI: Application-Specific Configuración de ejemplo (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: Application-Specific Configuración de ejemplo (Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
