---
description: Los administradores pueden crear, eliminar y volver a crear diarios de cambios.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Creación, modificación y eliminación de un diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c8cf7296f93549e7d9ec05f5d614131cc342ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668381"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Creación, modificación y eliminación de un diario de cambios

Los administradores pueden crear, eliminar y volver a crear diarios de cambios a su vez. Un administrador debe eliminar un diario cuando el valor de número de secuencia actualizada (USN) actual se aproxime al valor USN máximo posible, como indica el miembro **MaxUsn** de la estructura de [**\_ \_ datos del diario USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) . Un administrador también puede eliminar y volver a crear un diario de cambios para recuperar espacio en disco. Para realizar esta y todas las demás operaciones del diario de cambios no programáticos, debe tener privilegios de administrador del sistema. Es decir, debe ser miembro del grupo administradores.

Para crear o modificar un diario de cambios en un volumen especificado mediante programación, use el código de control de [**\_ \_ \_ diario FSCTL Create USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) .

Cuando se crea un diario de cambios nuevo o se modifica uno existente, el sistema de archivos NTFS establece la información de ese diario de cambios a partir de la información de la estructura de [**datos del diario de creación de \_ USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) , que usa el [**diario de FSCTL para \_ crear \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) como entrada. **Crear \_ Los \_ \_ datos del diario USN** tienen los miembros **tamañomáximo** y **AllocationDelta**.

**Tamañomáximo** es el tamaño máximo de destino para el diario de cambios en bytes. El diario de cambios puede aumentar el tamaño de este valor, pero en los puntos de control del sistema de archivos NTFS, el sistema de archivos NTFS examina el diario y lo recorta cuando su tamaño supera el valor de **tamañomáximo** más el valor de **AllocationDelta**. (En los puntos de control del sistema de archivos NTFS, el sistema operativo escribe los registros en el archivo de registro del sistema de archivos NTFS que permiten al sistema de archivos NTFS determinar qué procesamiento es necesario para recuperarse de un error).

**AllocationDelta** es el número de bytes que se agregan al final y se quitan del principio del diario de cambios cada vez que se asigna o se cancela la asignación de memoria. En otras palabras, la asignación y desasignación tienen lugar en unidades de este tamaño. Un número entero múltiplo de un tamaño de clúster es un valor razonable para este miembro.

Si un administrador modifica un diario de cambios existente para que tenga un valor de **MaximumSize** mayor, por ejemplo, si un volumen se está reindexando con demasiada frecuencia, el diario de cambios solo recibirá nuevas entradas hasta que supere el nuevo tamaño máximo.

Para eliminar un diario de cambios, use el código de control de [**\_ diario de eliminación de \_ USN \_ de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) . Cuando se usa esta operación, se recorren todos los archivos del volumen y se restablece el USN de cada archivo a cero. A continuación, la operación elimina el diario de cambios existente. Esta operación persiste a través de los reinicios del sistema hasta que se complete. Si se intenta leer, crear o modificar el diario de cambios durante este proceso, se producirá un error de código **\_ de error \_ \_ de eliminación en \_ curso**.

También puede usar el código de control de [**\_ \_ \_ diario FSCTL eliminar USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) para determinar si está en curso una eliminación iniciada por otro proceso. Por ejemplo, la aplicación, cuando se inicia, puede determinar si hay una eliminación en curso. Dado que las eliminaciones del diario se conservan a través de reinicios del sistema, los servicios y las aplicaciones que se inician al reiniciar el sistema deben comprobar si hay una eliminación en curso.

Los diarios de cambios no se crean necesariamente en el inicio. Para crear un diario de cambios, un administrador puede hacerlo explícitamente o iniciar otro servicio que requiera un diario de cambios.

 

 
