---
title: Estado de caché en la raíz de virtualización
description: Describe los distintos Estados de la memoria caché que puede tener un archivo o directorio administrado por el proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "104420122"
---
# <a name="cache-state-in-the-virtualization-root"></a>Estado de caché en la raíz de virtualización

El proveedor usa el sistema de archivos local bajo la raíz de virtualización como una caché de los elementos que administra.  Un elemento (archivo o directorio) puede estar en uno de seis Estados en el sistema de archivos local:

* Las máquinas

  El elemento no existe localmente en el disco.  Se proyecta, es decir, sintetizado, durante las enumeraciones de su directorio principal.  Los elementos virtuales se combinan con los elementos que puedan existir en el disco para presentar todo el contenido del directorio principal.

* Marcador de posición

  En el caso de los archivos: el contenido del archivo (flujo de datos principal) no está presente en el disco.  Los metadatos del archivo (nombre, tamaño, marcas de tiempo, atributos, etc.) se almacenan en caché en el disco.
  
  En el caso de los directorios: algunos o todos los descendientes inmediatos del directorio (los archivos y directorios del directorio) no están presentes en el disco, es decir, siguen siendo virtuales.  Los metadatos del directorio (nombre, marcas de tiempo, atributos, etc.) se almacenan en caché en el disco.

* Marcador de posición hidratado

  En el caso de los archivos: el contenido y los metadatos del archivo se han almacenado en caché en el disco.  También se conoce como "archivo parcial".
  
  En el caso de los directorios: un directorio que se creó en el disco como un marcador de posición nunca se convierte en un directorio de marcador de posición hidratado.  Esto permite al proveedor agregar o quitar elementos del directorio de su memoria auxiliar y hacer que dichos cambios se reflejen en la caché local.

* Marcador de posición Dirty (hidratado o no)

  Los metadatos del elemento se han modificado localmente y ya no son una caché de su estado en el almacén del proveedor. Tenga en cuenta que la creación o eliminación de un archivo o un directorio en un directorio de marcadores de posición hace que ese directorio de marcadores de posición se convierta en sucio.

* Archivo/directorio completo

  En el caso de los archivos: se ha modificado el contenido del archivo (flujo de datos principal).  El archivo ya no es una memoria caché de su estado en el almacén del proveedor.  Los archivos que se han creado en el sistema de archivos local (es decir, que no existen en el almacén del proveedor) también se consideran archivos completos.
  
  En el caso de los directorios: los directorios que se han creado en el sistema de archivos local (es decir, que no existen en el almacén del proveedor en absoluto) se consideran directorios completos.  Un directorio que se creó en el disco como un marcador de posición nunca se convierte en un directorio completo.
  
* Exclusión

  Marcador de posición oculto especial que representa un elemento que se ha eliminado del sistema de archivos local.  Cuando se enumera un directorio ProjFS combina el conjunto de elementos locales (marcadores de posición, archivos completos, etc.) con el conjunto de elementos proyectados virtuales.  Si un elemento aparece en los conjuntos locales y proyectados, el elemento local tiene prioridad.  Si un archivo no existe en el sistema de archivos local, no hay ningún estado local, por lo que aparecería en la enumeración.  Sin embargo, si ese elemento se hubiera eliminado, si aparece en la enumeración sería inesperado.  Reemplazar un elemento eliminado con un objeto de desecho produce los siguientes efectos:

  * Enumeraciones para no revelar el elemento.
  * Se abre un archivo que espera que el elemento exista, por ejemplo, "archivo no encontrado".
  * El archivo crea que esperará que se realice correctamente solo si el elemento no existe correctamente; ProjFS quita el elemento de desecho como parte de la operación.

Para ilustrar los Estados anteriores, tenga en cuenta la siguiente secuencia, dado un proveedor ProjFS que tiene un único archivo "foo.txt" ubicado en la raíz de virtualización C:\root.

1. Una aplicación enumera C:\root.  Ve el archivo virtual "foo.txt".  Puesto que no se ha tenido acceso al archivo, el archivo no existe en el disco.
1. La aplicación abre un identificador para C:\root\foo.txt.  ProjFS indica al proveedor que cree un marcador de posición para él.
1. La aplicación lee el contenido del archivo.  El proveedor proporciona el contenido del archivo a ProjFS y se almacena en caché para C:\root\foo.txt.  El archivo es ahora un marcador de posición hidratado.
1. La aplicación actualiza la marca de tiempo de la última modificación.  El archivo es ahora un marcador de posición de modificado.
1. La aplicación abre un identificador para el acceso de escritura al archivo.  C:\root\foo.txt es ahora un archivo completo.
1. La aplicación elimina C:\root\foo.txt.  ProjFS reemplaza el archivo por un marcadores de exclusión.  Ahora, cuando la aplicación Enumere C:\root, no verá foo.txt.  Si intenta abrir el archivo, se produce un error al abrir con ERROR_FILE_NOT_FOUND.
