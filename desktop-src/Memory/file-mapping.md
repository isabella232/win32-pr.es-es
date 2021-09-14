---
description: La asignación de archivos es la asociación del contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Asignación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159864"
---
# <a name="file-mapping"></a>Asignación de archivos

*La asignación* de archivos es la asociación del contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso. El sistema crea un objeto *de asignación de archivos* (también conocido como objeto de *sección)* para mantener esta asociación. Una *vista de archivo* es la parte del espacio de direcciones virtuales que un proceso usa para acceder al contenido del archivo. La asignación de archivos permite que el proceso use entradas y salidas aleatorias (E/S) y E/S secuenciales. También permite que el proceso funcione de forma eficaz con un archivo de datos grande, como una base de datos, sin tener que asignar todo el archivo a la memoria. Varios procesos también pueden usar archivos asignados a memoria para compartir datos.

Procesa la lectura y escritura en la vista de archivo mediante punteros, como lo harían con memoria asignada dinámicamente. El uso de la asignación de archivos mejora la eficacia porque el archivo reside en el disco, pero la vista de archivo reside en memoria. Los procesos también pueden manipular la vista de archivo con la [**función VirtualProtect.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)

En la ilustración siguiente se muestra la relación entre el archivo en disco, un objeto de asignación de archivos y una vista de archivo.

![relación entre el archivo en disco, un objeto de asignación de archivos y una vista de archivo.](images/fmap.png)

El archivo del disco puede ser cualquier archivo que desee asignar a la memoria o puede ser el archivo de página del sistema. El objeto de asignación de archivos puede constar de toda o solo una parte del archivo. El archivo del disco lo copia. Esto significa que cuando el sistema intercambia páginas del objeto de asignación de archivos, los cambios realizados en el objeto de asignación de archivos se escriben en el archivo. Cuando las páginas del objeto de asignación de archivos se intercambian de nuevo, se restauran desde el archivo .

Una vista de archivo puede constar de toda o solo una parte del objeto de asignación de archivos. Un proceso manipula el archivo a través de las vistas de archivo. Un proceso puede crear varias vistas para un objeto de asignación de archivos. Las vistas de archivo creadas por cada proceso residen en el espacio de direcciones virtuales de ese proceso. Cuando el proceso necesita datos de una parte del archivo que no sea la que se encuentra en la vista de archivo actual, puede desa asignar la vista de archivo actual y, a continuación, crear una nueva vista de archivo.

Cuando varios procesos usan el mismo objeto de asignación de archivos para crear vistas para un archivo local, los datos son coherentes. Es decir, las vistas contienen copias idénticas del archivo en disco. El archivo no puede residir en un equipo remoto si desea compartir memoria entre varios procesos.

Para obtener más información, vea los temas siguientes:

-   [Crear un objeto de asignación de archivos](creating-a-file-mapping-object.md)
-   [Crear una vista de archivo](creating-a-file-view.md)
-   [Uso compartido de archivos y memoria](sharing-files-and-memory.md)
-   [Lectura y escritura desde una vista de archivo](reading-and-writing-from-a-file-view.md)
-   [Cerrar un objeto de asignación de archivos](closing-a-file-mapping-object.md)
-   [Derechos de acceso y seguridad de asignación de archivos](file-mapping-security-and-access-rights.md)
-   [Uso de la asignación de archivos](using-file-mapping.md)

 

 
