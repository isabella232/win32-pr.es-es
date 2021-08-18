---
description: Carga de recursos de lenguaje
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Carga de recursos de lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106935"
---
# <a name="loading-language-resources"></a>Carga de recursos de lenguaje

La aplicación carga todos los recursos de lenguaje de la interfaz de usuario, aparte de ciertas cadenas del Registro redirigidas, mediante llamadas a funciones de carga de recursos estándar, por ejemplo, [**FormatMessage,**](/windows/win32/api/winbase/nf-winbase-formatmessage) [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)y [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Muchas funciones de carga de recursos se han modificado para cargar recursos de archivos de recursos específicos del lenguaje automáticamente, tratando los recursos como si se encuentran en el archivo LN. En el ejemplo siguiente se muestra el uso de **LoadString para** cargar cadenas de idioma para una aplicación que sigue la configuración del idioma del sistema.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda de recursos de Win32 PE](locating-win32-pe-resources.md)
</dt> </dl>

 

 
