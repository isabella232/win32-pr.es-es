---
description: Un nombre de dispositivo de MS-DOS es una Unión que apunta a la ruta de acceso de un dispositivo de MS-DOS. Estas uniones componen el espacio de nombres del dispositivo de MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definir un nombre de dispositivo de MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687279"
---
# <a name="defining-an-ms-dos-device-name"></a>Definir un nombre de dispositivo de MS-DOS

Un nombre de dispositivo de MS-DOS es una Unión que apunta a la ruta de acceso de un dispositivo de MS-DOS. Estas uniones componen el espacio de nombres del dispositivo de MS-DOS. Llame a las funciones [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) y [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear y modificar estas uniones. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) elimina una unión creada por **SetVolumeMountPoint** y **DefineDosDevice** elimina las uniones que crea.

Una vez definido el nombre de un dispositivo MS-DOS, éste permanece visible para todos los procesos.

-   Todos los dispositivos de MS-DOS se identifican mediante Windows a través de un identificador de autenticación. Un identificador de autenticación es el LUID (identificador local único) asociado a cada sesión de inicio de sesión cuando se crea.
-   La visibilidad de un nombre de dispositivo de MS-DOS se clasifica como global o local, y se define como tal por su inclusión en el dispositivo de MS-DOS global y en los espacios de nombres de los dispositivos locales de MS-DOS. Todos los usuarios pueden acceder al contenido de los dispositivos MS-DOS del espacio de nombres global, y solo el usuario cuyo token de acceso contenga el AuthenticationID asociado a ese espacio de nombres de dispositivo MS-DOS local puede acceder al contenido de los dispositivos ms-dos del espacio de nombres local.

Varios espacios de nombres de dispositivos locales de MS-DOS y solo puede haber un espacio de nombres de dispositivo de MS-DOS global al mismo tiempo y en un equipo.

Tenga en cuenta que solo los procesos que se ejecutan en el contexto de LocalSystem pueden llamar a [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) para crear un dispositivo ms-dos en el espacio de nombres del dispositivo de ms-dos global. Además, el espacio de nombres del dispositivo MS-DOS local correspondiente a un AuthenticationID específico se elimina cuando se quita la última referencia a ese AuthenticationID.

Cuando el código consulta un nombre de dispositivo de MS-DOS existente mediante una llamada a [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew), busca primero en el espacio de nombres del dispositivo ms-dos local. Si no se encuentra allí, la función buscará en el espacio de nombres de dispositivo de MS-DOS global. Cuando el código consulta todos los nombres de dispositivos de MS-DOS existentes a través de esta función, la lista de nombres que se devuelve depende de si se está ejecutando en el contexto de LocalSystem. En ese caso, solo se devolverán los nombres de dispositivos de MS-DOS incluidos en el espacio de nombres del dispositivo de MS-DOS global. Si no es así, se devolverá una concatenación de los nombres de los dispositivos en los espacios de nombres de los dispositivos de MS-DOS globales y locales. Si existe un nombre de dispositivo en ambos espacios de nombres, **QueryDosDevice** devolverá la entrada en el espacio de nombres del dispositivo ms-dos local. Esto también se aplica a la lista de todos los nombres de dispositivos de MS-DOS devueltos por [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) y [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw).

Tenga en cuenta que puede producirse el siguiente escenario:

1.  El usuario A, que no se ejecuta en el contexto de LocalSystem, crea un nombre de dispositivo en el espacio de nombres de dispositivo de MS-DOS local correspondiente y el nombre del dispositivo no existe en el espacio de nombres del dispositivo de MS-DOS global.
2.  El usuario B, que se ejecuta en el contexto de LocalSystem, crea el mismo nombre de dispositivo en el espacio de nombres del dispositivo MS-DOS global.

En este escenario, el usuario A no tendrá acceso al nombre del dispositivo en el espacio de nombres global del dispositivo MS-DOS hasta que quite o cambie el nombre del dispositivo en su espacio de nombres de dispositivo de MS-DOS local. Para reducir la probabilidad de que se produzca este escenario, las letras de unidad de MS-DOS deben asignarse en el espacio de nombres del dispositivo MS-DOS global a partir de C: y terminar con Z:. Esta secuencia debe invertirse para la asignación de Letras de unidad de MS-DOS en el espacio de nombres del dispositivo MS-DOS local.

Si no está ejecutando en el contexto de LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) no le permitirá definir un nombre de dispositivo en el espacio de nombres del dispositivo ms-dos local si ese nombre de dispositivo ya existe en los espacios de nombres de dispositivo de ms-dos local o global. Llame a [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) antes de llamar a **DefineDosDevice** para determinar si el nombre del dispositivo que desea definir existe en los espacios de nombres de dispositivo de ms-dos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Nomenclatura de archivos, rutas de acceso y espacios de nombres](naming-a-file.md)
</dt> </dl>

 

 



