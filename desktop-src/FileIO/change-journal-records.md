---
description: A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe en secuencias los registros del diario de cambios, uno para cada volumen del equipo.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Cambiar registros de diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688474"
---
# <a name="change-journal-records"></a>Cambiar registros de diario

A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe en secuencias los registros del diario de cambios, uno para cada volumen del equipo. Cada registro indica el tipo de cambio y el objeto cambiado. El desplazamiento desde el principio de la secuencia para un registro determinado se denomina número de secuencia de actualización (USN) para el registro en particular. Los nuevos registros se anexan al final de la secuencia.

El sistema de archivos NTFS puede eliminar los registros antiguos para ahorrar espacio. Si se han eliminado registros necesarios, el servicio de indexación se recupera al volver a indexar el volumen, como cuando no existe ningún diario de cambios.

El diario de cambios solo registra el hecho de un cambio en un archivo y el motivo del cambio (por ejemplo, operaciones de escritura, truncamiento, prolongación, eliminación, etc.). No registra suficiente información para permitir invertir el cambio.

Además, varios cambios en el mismo archivo pueden dar lugar a que solo se agregue una marca de motivo al registro actual. Si el mismo tipo de cambio se produce más de una vez, el sistema de archivos NTFS no escribe un nuevo registro para los cambios después de la primera. Por ejemplo, varias operaciones de escritura que no intervienen en operaciones de cierre y de reapertura, dan como resultado un solo registro de cambios con la marca de razón USN \_ motivo de \_ sobrescritura de datos \_ .

Para ilustrar el funcionamiento del diario de cambios, supongamos que un usuario tiene acceso a un archivo en el siguiente orden:

1.  Escribe en el archivo.
2.  Establece la marca de tiempo para el archivo.
3.  Escribe en el archivo.
4.  Trunca el archivo.
5.  Escribe en el archivo.
6.  Cierra el archivo.

En este caso, el sistema de archivos NTFS realiza las siguientes acciones en el diario de cambios (donde \| indica una operación OR bit a bit).



| Evento                                 | Acción del sistema de archivos NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operación de escritura inicial<br/>    | El sistema de archivos NTFS escribe un nuevo registro USN con el \_ valor de la marca de motivo de sobrescritura de datos de razón USN \_ \_ . Para obtener más información sobre las posibles marcas de motivo, consulte la estructura de [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) .<br/>                                                     |
| Configuración de la marca de tiempo de archivo<br/> | El sistema de archivos NTFS escribe un nuevo registro USN con la opción de marca USN \_ razón USN \_ \_ sobrescribir datos \| USN \_ motivo \_ \_ información básica \_ cambiar.<br/>                                                                                                                            |
| Segunda operación de escritura<br/>     | El sistema de archivos NTFS no escribe un nuevo registro USN. Dado \_ \_ \_ que ya se ha establecido el valor de USN Reason Data overwrite para el registro existente, no se realiza ningún cambio en el registro.<br/>                                                                                           |
| Truncamiento de archivo<br/>            | El sistema de archivos NTFS escribe un nuevo registro USN con la configuración de la marca USN motivo de \_ \_ sobrescritura de datos \_ sobrescribir USN motivo de la \| \_ \_ información básica cambiar el valor del \_ \_ truncamiento de \| \_ \_ datos \_ .<br/>                                                                                           |
| Tercera operación de escritura<br/>      | El sistema de archivos NTFS no escribe un nuevo registro USN. Dado \_ \_ \_ que ya se ha establecido el valor de USN Reason Data overwrite para el registro existente, no se realiza ningún cambio en el registro.<br/>                                                                                           |
| Operación de cierre<br/>            | Si el usuario que realiza cambios es el único usuario del archivo, el sistema de archivos NTFS escribe un nuevo registro USN con la siguiente configuración de marca: USN \_ Reason \_ datos sobrescribir USN motivo de la \_ \| \_ \_ información básica cambiar el valor de \_ \_ \| USN motivo de \_ truncamiento de \_ datos \_ \| \_ \_ el valor de USN razón de USN.<br/> |



 

El diario de cambios acumula una serie de registros entre la primera apertura y el último cierre de un archivo. Cada registro tiene un nuevo marcador de motivo establecido, que indica que se ha producido un nuevo tipo de cambio. La secuencia de registros proporciona un historial parcial del archivo. El registro final, creado cuando se cierra el archivo, agrega la \_ marca de cierre de motivo USN \_ . Este registro representa un resumen de los cambios en el archivo, pero a diferencia de los registros anteriores, no proporciona ninguna indicación del orden de los cambios.

El siguiente usuario para tener acceso y cambiar el archivo genera un nuevo registro USN con una marca de motivo único.

 

 




