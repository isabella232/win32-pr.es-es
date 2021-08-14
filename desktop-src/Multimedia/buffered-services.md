---
title: Servicios almacenados en búfer
description: Servicios almacenados en búfer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- E/S de archivos multimedia, servicios almacenados en búfer
- E/S de archivo, servicios almacenados en búfer
- entrada y salida (E/S), servicios almacenados en búfer
- E/S (entrada y salida), servicios almacenados en búfer
- E/S en búfer
- mmioOpen ( Función)
- búfer de E/S interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f8e7c11dbc90f7090bc8fcee114ebfac79f9bd54d834203f4b8e7bf893f591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989417"
---
# <a name="buffered-services"></a>Servicios almacenados en búfer

La mayor parte de la sobrecarga en la E/S de archivos se produce al acceder al dispositivo multimedia. Si está leyendo o escribiendo muchos bloques pequeños de información, el dispositivo puede dedicar mucho tiempo a moverse a la ubicación física en los medios para cada operación de lectura o escritura. En este caso, puede lograr un mejor rendimiento mediante el uso de servicios de E/S de archivos almacenados en búfer. Con la E/S en búfer, el administrador de E/S de archivos mantiene un búfer intermedio mayor que los bloques de información que está leyendo o escribiendo. Solo tiene acceso al dispositivo cuando el búfer debe rellenarse desde el disco o escribirse en él.

Antes de configurar y usar la E/S de archivos almacenados en búfer, debe decidir si desea que el administrador de E/S de archivos o la aplicación asignen el búfer. Es más sencillo dejar que el administrador de E/S de archivos asigne el búfer. Sin embargo, puede permitir que la aplicación asigne el búfer si desea acceder directamente al búfer o abrir un archivo de memoria. Para obtener más información sobre el uso de archivos de memoria, vea [Realizar E/S de archivos de memoria.](performing-memory-file-i-o.md) Para obtener un ejemplo de acceso directo a un búfer de E/S, consulte [Acceso a un búfer de E/S de archivo.](accessing-a-file-i-o-buffer.md)

Un búfer asignado por el administrador de E/S de archivo se denomina búfer de E/S interno. Para abrir un archivo para E/S en búfer mediante un búfer interno, especifique la marca MMIO ALLOCBUF al abrir el archivo con la \_ [**función mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) En la ilustración siguiente se muestra el estado inicial del búfer de E/S de archivo después de abrir un archivo para una operación de lectura en búfer. El almacenamiento en búfer es transparente: se lee y se busca como si estuviera usando E/S sin almacenamiento en búfer. La **función mmioOpen** ha establecido pchNext y *pchEndRead* para que apunten al principio del búfer de E/S de archivo.

![Captura de pantalla que muestra "pchEndRead" y "pchNext" que apuntan al principio del búfer de E/S de archivo.](images/mmio7.gif)

En la ilustración siguiente se muestra el estado inicial del búfer de E/S de archivo después de abrir un archivo para una operación de escritura en búfer. La **función mmioOpen** ha establecido **pchNext** para que apunte al principio del búfer de E/S de archivo y **pchEndWrite** para que apunte al final del búfer.

![Captura de pantalla que muestra "pchNext" al principio del búfer de E/S de archivo y "pchEndWrite" al final.](images/mmio11.gif)

El tamaño predeterminado del búfer de E/S interno es 8 K. Si este tamaño no es adecuado, puede usar la función [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) para cambiar el tamaño del búfer. También puede usar esta función para habilitar el almacenamiento en búfer en un archivo abierto para E/S sin búfer o para proporcionar su propio búfer para su uso como archivo de memoria.

Puede forzar que el contenido de un búfer de E/S se escriba en el disco mediante la [**función mmioFlush.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) Sin embargo, al cerrar un archivo mediante la función [**mmioClose,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) no es necesario llamar a **mmioFlush** para vaciar un búfer de E/S, ya que la función **mmioClose** lo vacía automáticamente. Si se queda sin espacio en disco, **mmioFlush** podría producir un error, incluso si las llamadas anteriores a la [**función mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) se realizaron correctamente. De forma similar, **mmioClose** podría producir un error cuando vacíe su búfer de E/S.

Las aplicaciones que tienen en cuenta el rendimiento, como las que transmiten datos en tiempo real desde un CD-ROM, pueden optimizar el rendimiento de E/S de archivos accediendo directamente al búfer de E/S. Debe tener cuidado si decide hacerlo, ya que omite algunas de las medidas de seguridad y comprobación de errores proporcionadas por el administrador de E/S de archivos.

El administrador de E/S de archivos multimedia usa la [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para mantener información de estado sobre un archivo abierto. En esta estructura se usan tres miembros para leer y escribir el búfer de E/S: **pchNext**, **pchEndRead** y **pchEndWrite**. El **miembro pchNext** apunta a la siguiente ubicación del búfer que se leerá o escribirá. Debe incrementar este miembro a medida que lee y escribe el búfer. El **miembro pchEndRead** identifica el último carácter válido que puede leer del búfer. Del mismo modo, este miembro identifica la última ubicación en el búfer que puede escribir. Más concretamente, **tanto pchEndRead** como **pchEndWrite** apuntan a la ubicación de memoria que sigue a los últimos datos válidos en el búfer. Use las [**funciones mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) y [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) para recuperar y establecer información de estado sobre el búfer de E/S de archivo. En la ilustración siguiente se muestra el estado del búfer de E/S después de que la aplicación llame a **mmioAdvance** durante una operación de lectura. La **función mmioAdvance** rellena el búfer y establece el **puntero pchEndRead** al final del búfer.

![Captura de pantalla que muestra "pchNext" al principio del búfer de E/S de archivo y "pchEndRead" al final.](images/mmio8.gif)

En la ilustración siguiente, la aplicación lee desde el búfer de E/S en la ubicación especificada por **pchNext** y avanza el puntero.

![Captura de pantalla que muestra "pchNext" en medio del búfer de E/S de archivo y "pchEndRead" al final.](images/mmio9.gif)

De forma similar, para una operación de escritura, la aplicación escribe en el búfer de E/S y avanza el **puntero pchNext,** como se muestra en la ilustración siguiente.

![Captura de pantalla que muestra "pchNext" en medio del búfer de E/S de archivo y "pchEndWrite" al final.](images/mmio12.gif)

Una vez que la aplicación rellena el búfer, llama a **mmioAdvance** para vaciar el búfer en el disco. La **función mmioAdvance** restablece **pchNext** para que apunte al principio del búfer, como se muestra en la ilustración siguiente.

![Captura de pantalla que muestra "pchNext" al principio del búfer de E/S de archivo, el búfer en medio de E O F y "pchEndWrite" al final del búfer.](images/mmio13.gif)

Cuando llegue al final del búfer de E/S, debe avanzar el búfer para rellenarlo desde el disco, si está leyendo o vaciarlo en el disco, si está escribiendo. Use la [**función mmioAdvance para**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) avanzar en un búfer de E/S. Para rellenar un búfer de E/S desde el disco, use **mmioAdvance con** la marca MMIO \_ READ. Si no hay suficientes datos restantes en el archivo para rellenar el búfer, el **miembro pchEndRead** de la estructura **MMIOINFO** apunta a la ubicación que sigue al último byte válido del búfer. Para vaciar un búfer en el disco, establezca la marca MMIO DIRTY en el miembro dwFlags de la estructura MMIOINFO y, a continuación, llame a \_ **mmioAdvance** con la marca MMIO   \_ WRITE.

Por ejemplo, durante una operación de lectura, la función **mmioAdvance** establece **pchEndRead** para que apunte al final de los datos válidos en el búfer, como se muestra en la ilustración siguiente.

![Captura de pantalla que muestra "pchNext" al principio del búfer de E/S de archivo, el búfer al final de E O F y "pchEndRead" al final del búfer.](images/mmio10.gif)

De forma similar, durante una operación de escritura, la aplicación llama a **mmioAdvance** para vaciar el búfer y avanzar **pchNext** hasta el final de los datos válidos en el búfer, como se muestra en la ilustración siguiente.

![imagen de búfer de E/S de archivo](images/mmio14.gif)

 

 