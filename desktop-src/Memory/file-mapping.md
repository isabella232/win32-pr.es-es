---
description: La asignación de archivos es la Asociación del contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541851"
---
# <a name="file-mapping"></a>Asignación de archivos

La *asignación de archivos* es la Asociación del contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso. El sistema crea un *objeto de asignación de archivos* (también conocido como *objeto de sección*) para mantener esta asociación. Una *vista de archivo* es la parte del espacio de direcciones virtuales que utiliza un proceso para tener acceso al contenido del archivo. La asignación de archivos permite que el proceso utilice la entrada y salida aleatorias (e/s) y la e/s secuencial. También permite que el proceso funcione de forma eficaz con un archivo de datos de gran tamaño, como una base de datos, sin tener que asignar el archivo completo en la memoria. Varios procesos también pueden usar archivos asignados a memoria para compartir datos.

Los procesos leen y escriben en la vista de archivo mediante punteros, tal como lo harían con memoria asignada dinámicamente. El uso de la asignación de archivos mejora la eficacia porque el archivo reside en el disco, pero la vista de archivo reside en la memoria. Los procesos también pueden manipular la vista de archivo con la función [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) .

En la ilustración siguiente se muestra la relación entre el archivo en el disco, un objeto de asignación de archivos y una vista de archivo.

![relación entre el archivo en el disco, un objeto de asignación de archivos y una vista de archivo.](images/fmap.png)

El archivo en disco puede ser cualquier archivo que desee asignar a la memoria o puede ser el archivo de paginación del sistema. El objeto de asignación de archivos puede constar de todo o solo parte del archivo. Está respaldado por el archivo en disco. Esto significa que cuando el sistema intercambia páginas del objeto de asignación de archivos, los cambios realizados en el objeto de asignación de archivos se escriben en el archivo. Cuando las páginas del objeto de asignación de archivos se vuelven a intercambiar en, se restauran desde el archivo.

Una vista de archivo puede constar de todo o solo parte del objeto de asignación de archivos. Un proceso manipula el archivo a través de las vistas de archivo. Un proceso puede crear varias vistas para un objeto de asignación de archivos. Las vistas de archivo creadas por cada proceso residen en el espacio de direcciones virtuales de ese proceso. Cuando el proceso necesita datos de una parte del archivo que no sea la que se encuentra en la vista de archivo actual, puede anular la asignación de la vista de archivo actual y, después, crear una nueva vista de archivos.

Cuando varios procesos usan el mismo objeto de asignación de archivos para crear vistas para un archivo local, los datos son coherentes. Es decir, las vistas contienen copias idénticas del archivo en el disco. El archivo no puede residir en un equipo remoto si desea compartir memoria entre varios procesos.

Para obtener más información, vea los temas siguientes:

-   [Crear un objeto de asignación de archivos](creating-a-file-mapping-object.md)
-   [Crear una vista de archivo](creating-a-file-view.md)
-   [Compartir archivos y memoria](sharing-files-and-memory.md)
-   [Leer y escribir en una vista de archivo](reading-and-writing-from-a-file-view.md)
-   [Cerrar un objeto de asignación de archivos](closing-a-file-mapping-object.md)
-   [Derechos de acceso y seguridad de asignación de archivos](file-mapping-security-and-access-rights.md)
-   [Usar la asignación de archivos](using-file-mapping.md)

 

 
