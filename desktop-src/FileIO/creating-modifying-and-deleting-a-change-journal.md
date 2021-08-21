---
description: Los administradores pueden crear, eliminar y volver a crear diarios de cambios.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Crear, modificar y eliminar un diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d4cf9a597baa14fc929028eab262479da30797a2e423b779083f028927ce50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150871"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Crear, modificar y eliminar un diario de cambios

Los administradores pueden crear, eliminar y volver a crear los diarios de cambios a su vez. Un administrador debe eliminar un diario cuando el valor actual del número de secuencia de actualización (USN) se aproxigue al valor máximo de USN posible, tal como lo indica el miembro **MaxUsn** de la estructura [**\_ USN JOURNAL \_ DATA.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) Un administrador también puede eliminar y volver a crear un diario de cambios para reclamar espacio en disco. Para realizar esta operación y todas las demás operaciones de diario de cambios que no son de programación, debe tener privilegios de administrador del sistema. Es decir, debe ser miembro del grupo Administradores.

Para crear o modificar un diario de cambios en un volumen especificado mediante programación, use el código de control [**FSCTL \_ CREATE \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)

Al crear un nuevo diario de cambios o modificar uno existente, el sistema de archivos NTFS establece la información de ese diario de cambios a partir de la información de la estructura [**CREATE \_ USN \_ JOURNAL \_ DATA,**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) que [**FSCTL CREATE \_ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) toma como entrada. **CREATE \_ USN \_ JOURNAL \_ DATA tiene** los miembros **MaximumSize** **y AllocationDelta**.

**MaximumSize** es el tamaño máximo de destino para el diario de cambios en bytes. El diario de cambios puede crecer más que este valor, pero en los puntos de comprobación del sistema de archivos NTFS, el sistema de archivos NTFS examina el diario y lo recorta cuando su tamaño supera el valor de **MaximumSize** más el valor **de AllocationDelta**. (En los puntos de control del sistema de archivos NTFS, el sistema operativo escribe registros en el archivo de registro del sistema de archivos NTFS que permiten al sistema de archivos NTFS determinar qué procesamiento es necesario para recuperarse de un error).

**AllocationDelta es** el número de bytes agregados al final y quitados del principio del diario de cambios cada vez que se asigna o desasigna memoria. En otras palabras, la asignación y desasignación tienen lugar en unidades de este tamaño. Un número entero múltiplo de un tamaño de clúster es un valor razonable para este miembro.

Si un administrador modifica un diario de cambios existente para que tenga un valor **MaximumSize** mayor, por ejemplo, si un volumen se vuelve a indexar con demasiada frecuencia, el diario de cambios simplemente recibe nuevas entradas hasta que supera el nuevo tamaño máximo.

Para eliminar un diario de cambios, use el código de control [**FSCTL \_ DELETE \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) Cuando se usa esta operación, se recorren todos los archivos del volumen y se restablece el USN de cada archivo a cero. A continuación, la operación elimina el diario de cambios existente. Esta operación persiste entre reinicios del sistema hasta que se completa. Cualquier intento de leer, crear o modificar el diario de cambios durante este proceso produce un error con el código de error **ERROR JOURNAL DELETE IN \_ \_ \_ \_ PROGRESS**.

También puede usar el código de control [**FSCTL \_ DELETE \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) para determinar si hay una eliminación iniciada por algún otro proceso en curso. Por ejemplo, la aplicación, cuando se inicia, puede determinar si una eliminación está en curso. Dado que las eliminaciones de diario persisten en los reinicios del sistema, los servicios y las aplicaciones iniciados al reiniciar el sistema deben comprobar si hay una eliminación en curso.

Los diarios de cambios no se crean necesariamente en el inicio. Para crear un diario de cambios, un administrador puede hacerlo explícitamente o iniciar otro servicio que requiera un diario de cambios.

 

 
