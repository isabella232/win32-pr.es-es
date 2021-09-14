---
description: Carga de recursos de lenguaje
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Carga de recursos de lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063084"
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

 

 
