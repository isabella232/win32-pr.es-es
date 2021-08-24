---
description: El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Usar el identificador del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483c171b69bcee0faf8df9f325d4ee8ffcb6e904f6aa0cd3c720b83df326e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015073"
---
# <a name="using-the-change-journal-identifier"></a>Usar el identificador del diario de cambios

El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios. El diario se marca con este identificador cuando se crea. El sistema de archivos marca el diario con un nuevo identificador donde los registros de número de secuencia de actualización (USN) existentes son o pueden ser inutilizables.

Por ejemplo, el sistema de archivos NTFS restampsa un diario de cambios con un nuevo identificador cuando un volumen se mueve de una versión de NTFS a otra y, a continuación, de vuelta. Este movimiento puede producirse en un entorno de arranque doble o cuando se trabaja con medios extraíbles.

Para obtener el identificador del diario de cambios actual en un volumen especificado, use el código de control [**FSCTL \_ QUERY \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) Para realizar esta y todas las demás operaciones del diario de cambios, debe tener privilegios de administrador del sistema. Es decir, debe ser miembro del grupo Administradores.

Cuando un administrador elimina y vuelve a crear el diario de cambios, por ejemplo, cuando el valor de USN actual se aproxima al valor máximo posible de USN, los valores de USN comienzan de nuevo desde cero. Cuando el sistema de archivos NTFS marca un diario con un nuevo identificador en lugar de volver a crear el diario, no restablece el USN a cero, pero continúa desde el USN actual. En cualquier caso, todos los USN existentes son menores que los USN futuros.

Cuando necesite información sobre un conjunto específico de registros, use el código de control [**FSCTL \_ QUERY \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) para obtener el identificador del diario de cambios. A continuación, use el código de control [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para leer los registros de diario de interés. El sistema de archivos NTFS solo devuelve los registros que son válidos para el diario especificado por el identificador.

La aplicación necesita los USN de los registros y el identificador para leer el diario. Este requisito proporciona una comprobación de integridad para los casos en los que la aplicación debe omitir los registros existentes en el archivo y en los que los registros se escribieron en instancias anteriores del diario para el mismo volumen.

Para obtener los registros en los que está interesado, debe empezar en el registro más antiguo (es decir, con el USN más bajo) y examinar hacia delante hasta que encuentre el primer registro de interés.

 

 
