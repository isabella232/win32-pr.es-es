---
description: Windows almacena en caché los datos de archivos que se leen de los discos y se escriben en los discos.
ms.assetid: 0865c741-63e3-4246-ba69-801b02153e4a
title: Almacenamiento en caché de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14fb668af16cfb8a4e42b59b25b73ecefbb7cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912866"
---
# <a name="file-caching"></a>Almacenamiento en caché de archivos

De forma predeterminada, Windows almacena en caché los datos de archivo que se leen de discos y se escriben en discos. Esto implica que las operaciones de lectura leen los datos de archivo de un área de la memoria del sistema conocida como caché de archivos del sistema, en lugar de desde el disco físico. En consecuencia, las operaciones de escritura escriben datos de archivo en la memoria caché de archivos, en lugar de en el disco. Este tipo de caché se conoce como caché de reescritura. El almacenamiento en caché se administra por objeto de archivo.

El almacenamiento en caché se produce bajo la dirección del *Administrador de caché*, que funciona continuamente mientras se ejecuta Windows. Los datos de archivo de la memoria caché de archivos del sistema se escriben en el disco a intervalos determinados por el sistema operativo y se libera la memoria usada previamente por los datos de archivo, lo que se conoce como *vaciar* la memoria caché. La Directiva de retrasar la escritura de los datos en el archivo y mantenerlo en la memoria caché hasta que se vacíe la memoria caché se denomina escritura diferida y se desencadena mediante el administrador de caché en un intervalo de tiempo de desterminación. La hora a la que se vacía un bloque de datos de archivo se basa, parcialmente, en la cantidad de tiempo que ha estado almacenado en la memoria caché y la cantidad de tiempo desde la última vez que se accedió a los datos en una operación de lectura. Esto garantiza que los datos de archivo que se suelen leer con frecuencia seguirán accesibles en la caché de archivos del sistema durante la cantidad máxima de tiempo.

Este proceso de almacenamiento en caché de datos de archivo se muestra en la ilustración siguiente.

![proceso de almacenamiento en caché de datos de archivos](images/fig3.png)

Como se muestra en las flechas sólidas de la ilustración anterior, una región de datos de 256 KB se lee en una memoria caché de 256 KB en el espacio de direcciones del sistema cuando lo solicita primero el administrador de caché durante una operación de lectura de archivo. A continuación, un proceso en modo de usuario copia los datos de esta ranura en su propio espacio de direcciones. Cuando el proceso ha finalizado su acceso a los datos, escribe los datos modificados en la misma ranura de la memoria caché del sistema, como se muestra mediante la flecha de puntos entre el espacio de direcciones del proceso y la memoria caché del sistema. Cuando el administrador de caché ha determinado que los datos ya no serán necesarios durante un período de tiempo determinado, vuelve a escribir los datos modificados en el archivo en el disco, tal como se muestra en la flecha de puntos entre la caché del sistema y el disco.

La cantidad de mejoras de rendimiento de e/s que ofrece el almacenamiento en caché de datos de archivos depende del tamaño del bloque de datos de archivo que se lee o se escribe. Cuando se leen y escriben bloques grandes de datos de archivos, es más probable que se necesiten lecturas y escrituras en el disco para finalizar la operación de e/s. El rendimiento de e/s se verá cada vez mayor, ya que se produce más de este tipo de operación de e/s.

En estas situaciones, se puede desactivar el almacenamiento en caché. Esto se hace en el momento en que se abre el archivo pasando el **indicador de archivo \_ \_ sin \_ almacenamiento en búfer** como un valor para el parámetro *dwFlagsAndAttributes* de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Cuando el almacenamiento en caché está deshabilitado, todas las operaciones de lectura y escritura acceden directamente al disco físico. Sin embargo, los metadatos del archivo se pueden almacenar en caché. Para vaciar los metadatos en el disco, use la función [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

La frecuencia con la que se produce el vaciado es una consideración importante que equilibra el rendimiento del sistema con la confiabilidad del sistema. Si el sistema vacía la caché con demasiada frecuencia, el número de operaciones de escritura de gran tamaño que se incurren en el vaciado reducirá significativamente el rendimiento del sistema. Si el sistema no se vacía con la frecuencia suficiente, la probabilidad es mayor que la memoria del sistema se agotará en la caché, o bien se producirá un error repentino del sistema (por ejemplo, una pérdida de energía en el equipo) antes del vaciado. En la última instancia, se perderán los datos almacenados en caché.

Para asegurarse de que se produce la cantidad correcta de vaciado, el administrador de caché genera un proceso cada segundo llamado escritor diferido. El proceso de escritura diferida pone en cola una octava parte de las páginas que no se han vaciado recientemente para que se escriban en el disco. Vuelve a evaluar constantemente la cantidad de datos que se vacían para obtener un rendimiento óptimo del sistema y, si es necesario escribir más datos, pone en cola más datos. Los escritores diferidos no vacían los archivos temporales, ya que se supone que se eliminarán por la aplicación o el sistema.

Algunas aplicaciones, como software de comprobación de virus, requieren que las operaciones de escritura se vacíen en el disco inmediatamente; Windows proporciona esta capacidad a través del almacenamiento en caché de escritura a través. Un proceso permite el almacenamiento en caché de escritura a través de una operación de e/s específica pasando el indicador de escritura de la **marca de archivo \_ \_ \_ a través** de la marca en la llamada a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Con el almacenamiento en caché de escritura a través habilitado, los datos se siguen escribiendo en la memoria caché, pero el administrador de caché escribe los datos inmediatamente en el disco en lugar de incurrir en un retraso mediante el uso de la escritura diferida. Un proceso también puede forzar un vaciado de un archivo que se ha abierto mediante una llamada a la función [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

Los metadatos del sistema de archivos siempre se almacenan en caché. Por lo tanto, para almacenar los cambios de metadatos en el disco, el archivo se debe vaciar o abrir con **escritura de marcador de archivo \_ \_ \_ a través** de.

 

 



