---
description: El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Usar el identificador del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687209"
---
# <a name="using-the-change-journal-identifier"></a>Usar el identificador del diario de cambios

El sistema de archivos NTFS asocia un identificador de 64 bits sin signo a cada diario de cambios. El diario se marca con este identificador cuando se crea. El sistema de archivos marca el diario con un nuevo identificador en el que los registros del número de secuencia de actualización (USN) existente están o no se pueden usar.

Por ejemplo, el sistema de archivos NTFS vuelve a marcar un diario de cambios con un identificador nuevo cuando se mueve un volumen de una versión de NTFS a otra y, a continuación, se vuelve a realizar. Este tipo de movimiento puede producirse en un entorno de arranque dual o cuando se trabaja con medios extraíbles.

Para obtener el identificador del diario de cambios actual en un volumen especificado, use el código de control del [**diario de USN de consulta de FSCTL \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) . Para realizar esta operación y todas las demás operaciones del diario de cambios, debe tener privilegios de administrador del sistema. Es decir, debe ser miembro del grupo administradores.

Cuando un administrador elimina y vuelve a crear el diario de cambios, por ejemplo, cuando el valor USN actual se aproxima al valor USN máximo posible, los valores USN comienzan de nuevo desde cero. Cuando el sistema de archivos NTFS marca un diario con un nuevo identificador en lugar de volver a crear el diario, no restablece el USN a cero pero continúa desde el USN actual. En cualquier caso, todos los USN existentes son menores que los USN futuros.

Cuando necesite información sobre un conjunto específico de registros, use el código de control del diario de USN de consulta de FSCTL para obtener el identificador del diario de cambios. [**\_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) A continuación, use el código de control de [**\_ \_ \_ diario FSCTL Read USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para leer los registros de diario de interés. El sistema de archivos NTFS solo devuelve los registros que son válidos para el diario especificado por el identificador.

La aplicación necesita los USN de los registros y el identificador para leer el diario. Este requisito proporciona una comprobación de integridad para los casos en los que la aplicación debe omitir los registros existentes en el archivo y en los que se escribieron los registros en las instancias anteriores del diario para el mismo volumen.

Para obtener los registros en los que está interesado, debe comenzar en el registro más antiguo (es decir, con el USN más bajo) y examinar hacia delante hasta encontrar el primer registro de interés.

 

 
