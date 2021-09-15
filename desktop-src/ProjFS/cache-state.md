---
title: Estado de caché en la raíz de virtualización
description: Describe los distintos estados de caché que puede tener un archivo o directorio administrado por el proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580221"
---
# <a name="cache-state-in-the-virtualization-root"></a>Estado de caché en la raíz de virtualización

El proveedor usa el sistema de archivos local en la raíz de virtualización como caché de los elementos que administra.  Un elemento (archivo o directorio) puede estar en uno de los seis estados del sistema de archivos local:

* Las máquinas

  El elemento no existe localmente en el disco.  Se proyecta, es decir, sintetizado, durante las enumeraciones de su directorio primario.  Los elementos virtuales se combinan con los elementos que pueden existir en el disco para presentar el contenido completo del directorio primario.

* Marcador de posición

  Para archivos: el contenido del archivo (flujo de datos principal) no está presente en el disco.  Los metadatos del archivo (nombre, tamaño, marcas de tiempo, atributos, etc.) se almacenan en caché en el disco.
  
  Para directorios: algunos o todos los descendientes inmediatos del directorio (los archivos y directorios del directorio) no están presentes en el disco, es decir, siguen siendo virtuales.  Los metadatos del directorio (nombre, marcas de tiempo, atributos, etc.) se almacenan en caché en el disco.

* Marcador de posición hidratado

  Para archivos: el contenido y los metadatos del archivo se han almacenado en caché en el disco.  También se conoce como "archivo parcial".
  
  Para directorios: un directorio que se creó en el disco como marcador de posición nunca se convierte en un directorio de marcador de posición hidratado.  Esto permite al proveedor agregar o quitar elementos del directorio en su memoria base y hacer que esos cambios se reflejen en la memoria caché local.

* Marcador de posición desasistido (hidratado o no)

  Los metadatos del elemento se han modificado localmente y ya no es una memoria caché de su estado en el almacén del proveedor. Tenga en cuenta que la creación o eliminación de un archivo o directorio en un directorio de marcador de posición hace que ese directorio de marcador de posición se dessvía.

* Archivo o directorio completos

  Para archivos: se ha modificado el contenido del archivo (flujo de datos principal).  El archivo ya no es una memoria caché de su estado en el almacén del proveedor.  Los archivos que se han creado en el sistema de archivos local (es decir, que no existen en el almacén del proveedor) también se consideran archivos completos.
  
  Para directorios: los directorios creados en el sistema de archivos local (es decir, que no existen en el almacén del proveedor) se consideran directorios completos.  Un directorio que se creó en el disco como marcador de posición nunca se convierte en un directorio completo.
  
* Lápida

  Marcador de posición oculto especial que representa un elemento que se ha eliminado del sistema de archivos local.  Cuando se enumera un directorio, ProjFS combina el conjunto de elementos locales (marcadores de posición, archivos completos, etc.) con el conjunto de elementos proyectados virtuales.  Si un elemento aparece en los conjuntos locales y proyectados, el elemento local tiene prioridad.  Si un archivo no existe en el sistema de archivos local, no hay ningún estado local, por lo que aparecería en la enumeración .  Sin embargo, si ese elemento se hubiera eliminado, su aparición en la enumeración sería inesperada.  Al reemplazar un elemento eliminado por un elemento de desecho, se produce el siguiente efecto:

  * Enumeraciones para no revelar el elemento.
  * Se abre el archivo que espera que el elemento exista, por ejemplo, "archivo no encontrado".
  * Crea archivos que esperan ser correctas solo si el elemento no existe correctamente; ProjFS quita el lápido como parte de la operación.

Para ilustrar los estados anteriores, considere la siguiente secuencia, dado un proveedor ProjFS que tiene un único archivo "foo.txt" ubicado en la raíz de virtualización C:\root.

1. Una aplicación enumera C:\root.  Ve el archivo virtual "foo.txt".  Puesto que aún no se ha accedido al archivo, el archivo no existe en el disco.
1. La aplicación abre un identificador para C:\root\foo.txt.  ProjFS indica al proveedor que cree un marcador de posición para él.
1. La aplicación lee el contenido del archivo.  El proveedor proporciona el contenido del archivo a ProjFS y se almacena en caché C:\root\foo.txt.  El archivo es ahora un marcador de posición hidratado.
1. La aplicación actualiza la marca de tiempo Última modificación.  El archivo es ahora un marcador de posición hidratado desnuciado.
1. La aplicación abre un identificador para el acceso de escritura al archivo.  C:\root\foo.txt es ahora un archivo completo.
1. La aplicación elimina C:\root\foo.txt.  ProjFS reemplaza el archivo por un lápido.  Ahora, cuando la aplicación enumera C:\root, no ve foo.txt.  Si intenta abrir el archivo, se produce un error al abrir ERROR_FILE_NOT_FOUND.
