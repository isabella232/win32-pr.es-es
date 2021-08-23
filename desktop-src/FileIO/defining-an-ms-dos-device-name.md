---
description: Un nombre de dispositivo MS-DOS es una unión que apunta a la ruta de acceso de un dispositivo MS-DOS. Estas uniones son el espacio de nombres del dispositivo MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definición de un nombre de dispositivo MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77331c1d3b3cc7566f118fa19fbb13c84e82af634f1098193bdf3dcb6270ef7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638935"
---
# <a name="defining-an-ms-dos-device-name"></a>Definición de un nombre de dispositivo MS-DOS

Un nombre de dispositivo MS-DOS es una unión que apunta a la ruta de acceso de un dispositivo MS-DOS. Estas uniones son el espacio de nombres del dispositivo MS-DOS. Llame a [**las funciones DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) [**y SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear y modificar estas uniones. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) elimina una unión creada por **SetVolumeMountPoint** y **DefineDosDevice** elimina las uniones que crea.

Después de definir un nombre de dispositivo MS-DOS, permanece visible para todos los procesos.

-   Todos los dispositivos MS-DOS se identifican mediante Windows un identificador de autenticación. Un identificador de autenticación es el LUID (identificador único local) asociado a cada sesión de inicio de sesión cuando se crea.
-   La visibilidad de un nombre de dispositivo MS-DOS se clasifica como global o local, y se define como tal mediante su inclusión en los espacios de nombres Global MS-DOS Device y Local MS-DOS Device. Todos los usuarios pueden acceder al contenido de los dispositivos MS-DOS en el espacio de nombres global, y el contenido de los dispositivos MS-DOS del espacio de nombres Local solo puede acceder al usuario cuyo token de acceso contiene el AuthenticationID asociado a ese espacio de nombres de dispositivo MS-DOS local.

Pueden existir varios espacios de nombres de dispositivos MS-DOS locales y solo un espacio de nombres de dispositivo MS-DOS global a la vez y en un equipo.

Tenga en cuenta que solo los procesos que se ejecutan en el contexto LocalSystem pueden llamar a [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) para crear un dispositivo MS-DOS en el espacio de nombres global del dispositivo MS-DOS. Además, el espacio de nombres del dispositivo MS-DOS local correspondiente a un AuthenticationID específico se elimina cuando se quita la última referencia a ese AuthenticationID.

Cuando el código consulta un nombre de dispositivo MS-DOS existente mediante una llamada a [**QueryDosDevice,**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)primero busca en el espacio de nombres local del dispositivo MS-DOS. Si no se encuentra allí, la función buscará en el espacio de nombres global del dispositivo MS-DOS. Cuando el código consulta todos los nombres de dispositivo MS-DOS existentes a través de esta función, la lista de nombres devueltos depende de si se ejecuta en el contexto LocalSystem. Si es así, solo se devolverán los nombres de dispositivo MS-DOS incluidos en el espacio de nombres global del dispositivo MS-DOS. Si no es así, se devolverá una concatenación de los nombres de dispositivo en los espacios de nombres global y local del dispositivo MS-DOS. Si existe un nombre de dispositivo en ambos espacios de nombres, **QueryDosDevice** devolverá la entrada en el espacio de nombres local del dispositivo MS-DOS. Esto también se aplica a la lista de todos los nombres de dispositivo MS-DOS devueltos por [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) y [**GetLogicalDriveStrings.**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)

Tenga en cuenta que puede producirse el siguiente escenario:

1.  El usuario A, que no se ejecuta en el contexto LocalSystem, crea un nombre de dispositivo en el espacio de nombres del dispositivo MS-DOS local correspondiente y ese nombre de dispositivo no existe en el espacio de nombres global del dispositivo MS-DOS.
2.  El usuario B, que se ejecuta en el contexto LocalSystem, crea el mismo nombre de dispositivo en el espacio de nombres global del dispositivo MS-DOS.

En este escenario, el usuario A no tendrá acceso al nombre del dispositivo en el espacio de nombres Global MS-DOS Device hasta que quite o cambie el nombre del dispositivo en su espacio de nombres local de dispositivo MS-DOS. Para reducir la probabilidad de que se produzca este escenario, se deben asignar letras de unidad MS-DOS en el espacio de nombres global del dispositivo MS-DOS a partir de C: y terminar con Z:. Esta secuencia se debe invertir para la asignación de letras de unidad MS-DOS en el espacio de nombres local del dispositivo MS-DOS.

Si no está ejecutando en el contexto LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) no le permitirá definir un nombre de dispositivo en el espacio de nombres Local MS-DOS Device si ese nombre de dispositivo ya existe en los espacios de nombres local o global del dispositivo MS-DOS. Llame [**a QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) antes de llamar a **DefineDosDevice** para determinar si el nombre de dispositivo que pretende definir existe en los espacios de nombres del dispositivo MS-DOS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignar nombres a archivos, rutas de acceso y espacios de nombres](naming-a-file.md)
</dt> </dl>

 

 



