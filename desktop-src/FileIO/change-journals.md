---
description: Cuando se realiza algún cambio en un archivo o directorio de un volumen, el diario de cambios de USN de ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Cambiar diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7556a080e0e85a428a502bb77afcbffc3975b5255d2efed5158c008f30d928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534105"
---
# <a name="change-journals"></a>Cambiar diario

Una aplicación de copia de seguridad automática es un ejemplo de un programa que debe comprobar si hay cambios en el estado de un volumen para realizar su tarea. El método por fuerza bruta para comprobar los cambios en directorios o archivos consiste en examinar todo el volumen. Sin embargo, esto no suele ser un enfoque aceptable debido a la disminución del rendimiento del sistema que provocaría. Otro método consiste en que la aplicación registre una notificación de directorio (mediante una llamada a las funciones [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) o [**ReadDirectoryChangesW)**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) de los directorios de los que se va a realizar una copia de seguridad. Esto es más eficaz que el primer método; sin embargo, requiere que una aplicación se ejecute en todo momento. Además, si se debe hacer una copia de seguridad de un gran número de directorios y archivos, la cantidad de procesamiento y la sobrecarga de memoria de dicha aplicación también puede hacer que el rendimiento del sistema operativo disminuya.

Para evitar estas desventajas, el sistema de archivos NTFS mantiene un diario de cambios de número de secuencia de actualización (USN). Cuando se realiza algún cambio en un archivo o directorio de un volumen, el diario de cambios de USN de ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.

Los diarios de cambios también son necesarios para recuperar la indexación del sistema de archivos, por ejemplo, después de un error de equipo o volumen. La capacidad de recuperar la indexación significa que el sistema de archivos puede evitar el proceso lento de volver a indexar todo el volumen en tales casos.

En los temas siguientes se tratan los diarios de cambios.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                             | Descripción                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cambiar registros de diario](change-journal-records.md)<br/>                                                                   | A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe registros de diario de cambios en secuencias, uno para cada volumen del equipo.<br/>                                           |
| [Usar el identificador del diario de cambios](using-the-change-journal-identifier.md)<br/>                                         | El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios.<br/>                                                                                                                                                   |
| [Crear, modificar y eliminar un diario de cambios](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Los administradores pueden crear, eliminar y volver a crear los diarios de cambios.<br/>                                                                                                                                                                         |
| [Obtener un identificador de volumen para las operaciones del diario de cambios](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Para obtener un identificador para un volumen para su uso con operaciones de diario de cambio de número de secuencia de actualización (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena con el formato siguiente: \\ \\ . \\ *X*.<br/> |
| [Operaciones de diario de cambios](change-journal-operations.md)<br/>                                                             | Códigos de control y estructuras que se usan con el diario de cambio de número de secuencia de actualización del sistema de archivos NTFS (USN).<br/>                                                                                                                                |



 

 

 




