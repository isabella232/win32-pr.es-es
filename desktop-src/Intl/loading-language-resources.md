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
# <a name="loading-language-resources"></a>Cargando recursos de idioma

La aplicación carga todos los recursos de idioma de interfaz de usuario, excepto ciertas cadenas de registro redirigidas, mediante llamadas a funciones de carga de recursos estándar, por ejemplo, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)y [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea). Muchas funciones de carga de recursos se han modificado para cargar los recursos de los archivos de recursos específicos del idioma automáticamente, tratando los recursos como si estuvieran incluidos en el archivo LN. En el ejemplo siguiente se muestra el uso de **LoadString** para cargar cadenas de idioma para una aplicación que sigue la configuración de idioma del sistema.


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

[Ubicar recursos PE de Win32](locating-win32-pe-resources.md)
</dt> </dl>

 

 
