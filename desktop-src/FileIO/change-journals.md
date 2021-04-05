---
description: Cuando se realiza cualquier cambio en un archivo o directorio de un volumen, el diario de cambios USN para ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Cambiar diarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912873"
---
# <a name="change-journals"></a>Cambiar diarios

Una aplicación de copia de seguridad automática es un ejemplo de un programa que debe comprobar si hay cambios en el estado de un volumen para realizar su tarea. El método de fuerza bruta para comprobar los cambios en los directorios o archivos es examinar todo el volumen. Sin embargo, esto no suele ser un enfoque aceptable debido a la disminución del rendimiento del sistema que podría provocar. Otro método es que la aplicación registre una notificación de directorio (llamando a las funciones [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) o [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ) de los directorios de los que se va a realizar una copia de seguridad. Esto es más eficaz que el primer método, sin embargo, requiere que una aplicación se esté ejecutando en todo momento. Además, si se debe realizar una copia de seguridad de un gran número de directorios y archivos, la cantidad de procesamiento y sobrecarga de memoria para este tipo de aplicación también podría hacer que el rendimiento del sistema operativo disminuya.

Para evitar estas desventajas, el sistema de archivos NTFS mantiene un diario de cambios de números de secuencias actualizadas (USN). Cuando se realiza cualquier cambio en un archivo o directorio de un volumen, el diario de cambios USN para ese volumen se actualiza con una descripción del cambio y el nombre del archivo o directorio.

Los diarios de cambios también son necesarios para recuperar la indexación del sistema de archivos, por ejemplo después de un error de equipo o de volumen. La capacidad de recuperar la indexación significa que el sistema de archivos puede evitar el proceso lento de volver a indexar todo el volumen en estos casos.

En los temas siguientes se describen los diarios de cambios.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                             | Descripción                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cambiar registros de diario](change-journal-records.md)<br/>                                                                   | A medida que se agregan, eliminan y modifican archivos, directorios y otros objetos del sistema de archivos NTFS, el sistema de archivos NTFS escribe en secuencias los registros del diario de cambios, uno para cada volumen del equipo.<br/>                                           |
| [Usar el identificador del diario de cambios](using-the-change-journal-identifier.md)<br/>                                         | El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios.<br/>                                                                                                                                                   |
| [Creación, modificación y eliminación de un diario de cambios](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Los administradores pueden crear, eliminar y volver a crear diarios de cambios.<br/>                                                                                                                                                                         |
| [Obtención de un identificador de volumen para las operaciones del diario de cambios](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Para obtener un identificador de un volumen para su uso con las operaciones del diario de cambios del número de secuencias actualizadas (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena de la siguiente forma: \\ \\ . \\ *X*.<br/> |
| [Cambiar operaciones de diario](change-journal-operations.md)<br/>                                                             | Códigos y estructuras de control que se usarán con el diario de cambios del número de secuencias actualizadas (USN) del sistema de archivos NTFS.<br/>                                                                                                                                |



 

 

 




