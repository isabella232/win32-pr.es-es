---
description: A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe registros de diario de cambios en secuencias, uno para cada volumen del equipo.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Cambiar registros de diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313dde6a71b36ed046a7086d39ce8e1a86b909cc7c815f295bb8a45c82ab92f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765995"
---
# <a name="change-journal-records"></a>Cambiar registros de diario

A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe registros de diario de cambios en secuencias, uno para cada volumen del equipo. Cada registro indica el tipo de cambio y el objeto cambiado. El desplazamiento desde el principio de la secuencia de un registro determinado se denomina número de secuencia de actualización (USN) para el registro determinado. Los nuevos registros se anexan al final de la secuencia.

El sistema de archivos NTFS puede eliminar registros antiguos para ahorrar espacio. Si se han eliminado los registros necesarios, el servicio de indexación se recupera mediante la indexación del volumen, como ocurre cuando no existe ningún diario de cambios.

El diario de cambios solo registra el hecho de un cambio en un archivo y el motivo del cambio (por ejemplo, operaciones de escritura, truncamiento, longitud, eliminación, entre otros). No registra suficiente información para permitir revertir el cambio.

Además, varios cambios en el mismo archivo pueden dar lugar a que solo se agrega una marca de motivo al registro actual. Si se produce el mismo tipo de cambio más de una vez, el sistema de archivos NTFS no escribe un nuevo registro para los cambios después del primero. Por ejemplo, varias operaciones de escritura sin operaciones de cierre y de apertura que intervenga darán como resultado un único registro de cambio con la marca de motivo USN \_ REASON \_ DATA OVERWRITE \_ establecida.

Para ilustrar cómo funciona el diario de cambios, suponga que un usuario accede a un archivo en el orden siguiente:

1.  Escribe en el archivo.
2.  Establece la marca de tiempo para el archivo.
3.  Escribe en el archivo.
4.  Trunca el archivo.
5.  Escribe en el archivo.
6.  Cierra el archivo.

En este caso, el sistema de archivos NTFS realiza las siguientes acciones en el diario de cambios (donde \| indica una operación OR bit a bit).



| Evento                                 | Acción del sistema de archivos NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operación de escritura inicial<br/>    | El sistema de archivos NTFS escribe un nuevo registro USN con la marca de motivo USN \_ REASON \_ DATA OVERWRITE \_ establecida. Para obtener más información sobre las posibles marcas de motivo, vea la [**estructura RECORD \_ de USN.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)<br/>                                                     |
| Configuración de la marca de tiempo del archivo<br/> | El sistema de archivos NTFS escribe un nuevo registro USN con la marca que establece USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC \_ INFO \_ \_ \_ CHANGE.<br/>                                                                                                                            |
| Segunda operación de escritura<br/>     | El sistema de archivos NTFS no escribe un nuevo registro USN. Dado que USN REASON DATA OVERWRITE ya está establecido para el registro \_ \_ \_ existente, no se realiza ningún cambio en el registro.<br/>                                                                                           |
| Truncamiento de archivos<br/>            | El sistema de archivos NTFS escribe un nuevo registro USN con la marca que establece USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC \_ INFO CHANGE \_ \_ \_ \| USN REASON DATA \_ \_ \_ TRUNCATION.<br/>                                                                                           |
| Tercera operación de escritura<br/>      | El sistema de archivos NTFS no escribe un nuevo registro USN. Dado que USN REASON DATA OVERWRITE ya está establecido para el registro \_ \_ \_ existente, no se realiza ningún cambio en el registro.<br/>                                                                                           |
| Operación de cierre<br/>            | Si el usuario que realiza cambios es el único usuario del archivo, el sistema de archivos NTFS escribe un nuevo registro USN con la siguiente configuración de marca: USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC INFO \_ \_ CHANGE \_ \_ \| USN REASON DATA \_ \_ \_ TRUNCATION \| USN REASON \_ \_ CLOSE.<br/> |



 

El diario de cambios acumula una serie de registros entre la primera apertura y el último cierre de un archivo. Cada registro tiene una nueva marca de motivo establecida, que indica que se ha producido un nuevo tipo de cambio. La secuencia de registros proporciona un historial parcial del archivo. El registro final, creado cuando se cierra el archivo, agrega la marca USN \_ REASON \_ CLOSE. Este registro representa un resumen de los cambios en el archivo, pero, a diferencia de los registros anteriores, no proporciona ninguna indicación del orden de los cambios.

El siguiente usuario que accede y cambia el archivo genera un nuevo registro USN con una marca de motivo único.

 

 




