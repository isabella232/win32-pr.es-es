---
title: Búsqueda y carga de recursos
description: En este tema se describe cómo cargar un recurso en la memoria.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252405"
---
# <a name="finding-and-loading-resources"></a>Búsqueda y carga de recursos

Antes de usar un recurso, una aplicación debe cargarlo en la memoria. Las [**funciones FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) encuentran un recurso en un módulo y devuelven un identificador a los datos de recursos binarios. **FindResource** busca un recurso por tipo y nombre. **FindResourceEx** busca el recurso por tipo, nombre e idioma. La información **sobre FindResource** de este tema también se aplica a **FindResourceEx.**

La [**función LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) usa el identificador de recursos devuelto por [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) para cargar el recurso en la memoria. Después de que una aplicación cargue un recurso mediante **LoadResource**, el sistema descargará la memoria asociada solo cuando todas las referencias a su módulo se liberan a través [**de FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Las aplicaciones que necesitan acceder repetidamente a los mismos recursos o a muchos dentro de un módulo determinado pueden incurrir en penalizaciones de rendimiento debido a la asignación de memoria que tiene lugar en llamadas [**repetidas a LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y **FreeLibrary.** Las aplicaciones deben almacenar un único identificador de módulo hasta que los recursos ya no sean necesarios y, a continuación, llamar **a FreeLibrary**. Después de descargar un módulo de la memoria, los identificadores de recursos no son válidos.

Una aplicación puede usar [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) para buscar y cargar cualquier tipo de recurso, pero estas funciones solo se deben usar en una de estas situaciones:

-   Cuando la aplicación no puede acceder al recurso mediante una función específica del recurso existente.
-   Cuando la aplicación debe tener acceso al recurso como datos binarios para las llamadas de función posteriores.

Siempre que sea posible, una aplicación debe usar en su lugar una de las siguientes funciones específicas del recurso para buscar y cargar recursos en una llamada:



| Función                                     | Acción                                   | Para quitar el recurso                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Carga y da formato a una entrada de tabla de mensajes. | No se requiere ninguna acción.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Carga una tabla de aceleradores.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Carga un recurso de mapa de bits.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Carga un recurso de cursor.                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Carga un recurso de icono.                  | [**Destroyicon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Carga un icono, cursor o mapa de bits.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Carga un recurso de menú.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Carga una entrada de tabla de cadenas.              | No se requiere ninguna acción.                                                                                                |



 

Tenga en cuenta las funciones de versión de la tabla anterior. Antes de finalizar, una aplicación debe liberar la memoria ocupada por tablas de aceleradores, mapas de bits, cursores, iconos y menús mediante las funciones adecuadas.

La memoria asociada a los recursos cargados a través de [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) se liberará una vez que el módulo se haya descargado mediante una llamada a [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). El sistema liberará automáticamente los recursos que permanezcan descargados durante la finalización de la aplicación.

 

 