---
title: Buscar y cargar recursos
description: En este tema se describe cómo cargar un recurso en la memoria.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487575"
---
# <a name="finding-and-loading-resources"></a>Buscar y cargar recursos

Antes de utilizar un recurso, una aplicación debe cargarlo en la memoria. Las funciones [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) buscan un recurso en un módulo y devuelven un identificador a los datos de recursos binarios. **FindResource** busca un recurso por tipo y nombre. **FindResourceEx** busca el recurso por tipo, nombre y lenguaje. La información sobre **FindResource** en este tema también se aplica a **FindResourceEx**.

La función [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) usa el identificador de recursos devuelto por [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) para cargar el recurso en la memoria. Después de que una aplicación carga un recurso mediante **LoadResource**, el sistema descargará la memoria asociada solo cuando todas las referencias a su módulo se liberen a través de [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Las aplicaciones que necesitan tener acceso repetidamente a los mismos o a muchos recursos dentro de un módulo determinado pueden incurrir en penalizaciones de rendimiento debido a que la asignación de memoria se realiza en llamadas [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y **FreeLibrary** repetidas. Las aplicaciones deben almacenar un único identificador de módulo hasta que ya no se necesiten los recursos y, a continuación, llamar a **FreeLibrary**. Una vez que un módulo se descarga de la memoria, los identificadores de recursos dejan de ser válidos.

Una aplicación puede usar [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) para buscar y cargar cualquier tipo de recurso, pero estas funciones solo deben usarse en una de estas situaciones:

-   Cuando la aplicación no puede tener acceso al recurso mediante una función específica del recurso existente.
-   Cuando la aplicación debe tener acceso al recurso como datos binarios para las siguientes llamadas de función.

Siempre que sea posible, en su lugar, una aplicación debe usar una de las siguientes funciones específicas de recursos para buscar y cargar recursos en una llamada:



| Función                                     | Acción                                   | Para quitar el recurso                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Carga y da formato a una entrada de la tabla de mensajes. | No se requiere ninguna acción.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Carga una tabla de aceleradores.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Carga un recurso de mapa de bits.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Carga un recurso de cursor.                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Carga un recurso de icono.                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Carga un icono, un cursor o un mapa de bits.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Carga un recurso de menú.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**Fall**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Carga una entrada de tabla de cadenas.              | No se requiere ninguna acción.                                                                                                |



 

Tenga en cuenta las funciones de versión de la tabla anterior. Antes de finalizar, una aplicación debe liberar la memoria ocupada por las tablas de aceleradores, mapas de bits, cursores, iconos y menús mediante las funciones apropiadas.

La memoria asociada a los recursos cargados a través de [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) y [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) se liberará una vez que una llamada a [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)haya descargado el módulo. El sistema liberará automáticamente todos los recursos que permanezcan descargados en la terminación de la aplicación.

 

 