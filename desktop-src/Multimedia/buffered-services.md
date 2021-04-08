---
title: Servicios almacenados en búfer
description: Servicios almacenados en búfer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- e/s de archivos multimedia, servicios almacenados en búfer
- e/s de archivos, servicios almacenados en búfer
- entrada y salida (e/s), servicios almacenados en búfer
- E/s (entrada y salida), servicios almacenados en búfer
- e/s almacenada en búfer
- mmioOpen función)
- búfer de e/s interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104003261"
---
# <a name="buffered-services"></a>Servicios almacenados en búfer

La mayor parte de la sobrecarga en la e/s de archivos se produce al obtener acceso al dispositivo multimedia. Si está leyendo o escribiendo muchos bloques pequeños de información, el dispositivo puede dedicar mucho tiempo a la ubicación física del medio para cada operación de lectura o escritura. En este caso, puede lograr un mejor rendimiento mediante el uso de servicios de e/s de archivos almacenados en búfer. Con la e/s en búfer, el administrador de e/s de archivos mantiene un búfer intermedio mayor que los bloques de información que está leyendo o escribiendo. Solo tiene acceso al dispositivo cuando el búfer se debe rellenar o escribir en el disco.

Antes de configurar y usar e/s de archivos almacenados en búfer, debe decidir si desea que el administrador de e/s de archivos o la aplicación asignen el búfer. Es más sencillo permitir que el administrador de e/s de archivos asigne el búfer. Sin embargo, puede permitir que la aplicación asigne el búfer si desea tener acceso directo al búfer o abrir un archivo de memoria. Para obtener más información sobre el uso de archivos de memoria, vea [realizar e/s de archivos de memoria](performing-memory-file-i-o.md). Para obtener un ejemplo de acceso directo a un búfer de e/s, consulte [acceso a un búfer de e/s de archivos](accessing-a-file-i-o-buffer.md)

Un búfer asignado por el administrador de e/s de archivos se denomina búfer de e/s interno. Para abrir un archivo para e/s en búfer mediante un búfer interno, especifique la \_ marca ALLOCBUF MMIO al abrir el archivo con la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . En la ilustración siguiente se muestra el estado inicial del búfer de e/s de archivo después de abrir un archivo para una operación de lectura almacenada en búfer. El almacenamiento en búfer es transparente: Lee y busca como si estuviera usando e/s no almacenada en búfer. La función **mmioOpen** ha establecido PchNext y *pchEndRead* para que apunten al principio del búfer de e/s de archivo.

![Captura de pantalla que muestra "pchEndRead" y "pchNext" que apunta al principio del búfer de e/s de archivo.](images/mmio7.gif)

En la ilustración siguiente se muestra el estado inicial del búfer de e/s de archivo después de abrir un archivo para una operación de escritura almacenada en búfer. La función **mmioOpen** ha establecido **pchNext** para que apunte al principio del búfer de e/s de archivo y **pchEndWrite** para que apunten al final del búfer.

![Captura de pantalla que muestra "pchNext" al principio del búfer de e/s de archivo y "pchEndWrite" al final.](images/mmio11.gif)

El tamaño predeterminado del búfer de e/s interno es de 8 KB. Si este tamaño no es adecuado, puede usar la función [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) para cambiar el tamaño del búfer. También puede usar esta función para habilitar el almacenamiento en búfer en un archivo abierto para e/s sin almacenamiento en búfer, o para proporcionar su propio búfer para su uso como archivo de memoria.

Puede forzar el contenido de un búfer de e/s para que se escriba en el disco mediante la función [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) . Sin embargo, cuando se cierra un archivo mediante la función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , no es necesario llamar a **mmioFlush** para vaciar un búfer de e/s; la función **mmioClose** lo vacía automáticamente. Si se queda sin espacio en disco, se puede producir un error en **mmioFlush** , incluso si las llamadas anteriores a la función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) se realizaron correctamente. Del mismo modo, **mmioClose** podría producir un error al vaciar su búfer de e/s.

Las aplicaciones que tienen en cuenta el rendimiento, como las que transmiten datos en tiempo real desde un CD-ROM, pueden optimizar el rendimiento de e/s de archivos mediante el acceso directo al búfer de e/s. Tenga cuidado si decide hacerlo, porque omite algunas de las medidas de seguridad y la comprobación de errores que proporciona el administrador de e/s de archivos.

El administrador de e/s de archivos multimedia utiliza la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para mantener la información de estado de un archivo abierto. Se usan tres miembros en esta estructura para leer y escribir el búfer de e/s: **pchNext**, **pchEndRead** y **pchEndWrite**. El miembro **pchNext** apunta a la siguiente ubicación del búfer que se va a leer o escribir. Debe incrementar este miembro a medida que lee y escribe el búfer. El miembro **pchEndRead** identifica el último carácter válido que se puede leer en el búfer. Del mismo modo, este miembro identifica la última ubicación en el búfer que se puede escribir. Más concretamente, **pchEndRead** y **pchEndWrite** apuntan a la ubicación de memoria que sigue los últimos datos válidos en el búfer. Use las funciones [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) y [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) para recuperar y establecer información de estado sobre el búfer de e/s de archivos. En la ilustración siguiente se muestra el estado del búfer de e/s después de que la aplicación llame a **mmioAdvance** durante una operación de lectura. La función **mmioAdvance** rellena el búfer y establece el puntero **pchEndRead** al final del búfer.

![Captura de pantalla que muestra "pchNext" al principio del búfer de e/s de archivo y "pchEndRead" al final.](images/mmio8.gif)

En la ilustración siguiente, la aplicación Lee del búfer de e/s en la ubicación especificada por **pchNext** y hace avanzar el puntero.

![Captura de pantalla que muestra "pchNext" en medio del búfer de e/s de archivo y "pchEndRead" al final.](images/mmio9.gif)

Del mismo modo, para una operación de escritura, la aplicación escribe en el búfer de e/s y avanza el puntero **pchNext** , como se muestra en la siguiente ilustración.

![Captura de pantalla que muestra "pchNext" en medio del búfer de e/s de archivo y "pchEndWrite" al final.](images/mmio12.gif)

Una vez que la aplicación rellena el búfer, llama a **mmioAdvance** para vaciar el búfer en el disco. La función **mmioAdvance** restablece **pchNext** para que apunte al principio del búfer, tal y como se muestra en la siguiente ilustración.

![Captura de pantalla que muestra "pchNext" al principio del búfer de e/s de archivo, el búfer en medio de E O F y "pchEndWrite" al final del búfer.](images/mmio13.gif)

Cuando llegue al final del búfer de e/s, debe avanzar el búfer para rellenarlo desde el disco, si está leyendo o vaciarlo en el disco, si está escribiendo. Use la función [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) para avanzar un búfer de e/s. Para rellenar un búfer de e/s desde el disco, use **mmioAdvance** con la marca de lectura de MMIO \_ . Si no quedan suficientes datos en el archivo para rellenar el búfer, el miembro **pchEndRead** de la estructura **MMIOINFO** apunta a la ubicación siguiente al último byte válido del búfer. Para vaciar un búfer en el disco, establezca la \_ marca MMIO Dirty en el miembro **dwFlags** de la estructura **MMIOINFO** y, a continuación, llame a **MMIOADVANCE** con la marca de \_ escritura mmio.

Por ejemplo, durante una operación de lectura, la función **mmioAdvance** establece **pchEndRead** para que señale al final de los datos válidos en el búfer, tal como se muestra en la siguiente ilustración.

![Captura de pantalla que muestra "pchNext" al principio del búfer de e/s de archivo, el búfer al final de E O F y "pchEndRead" al final del búfer.](images/mmio10.gif)

Del mismo modo, durante una operación de escritura, la aplicación llama a **mmioAdvance** para vaciar el búfer y avanzar **pchNext** hasta el final de los datos válidos en el búfer, tal y como se muestra en la siguiente ilustración.

![imagen de búfer de e/s de archivo](images/mmio14.gif)

 

 