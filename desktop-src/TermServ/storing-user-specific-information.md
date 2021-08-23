---
title: Almacenamiento de información específica del usuario
description: Las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, aparte de la información global que se aplica a todos los usuarios.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aa8e60ec89c3f9d161941d01e1aa241f0bb0245d0f5b57b1cc362dd836bdb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000435"
---
# <a name="storing-user-specific-information"></a>Almacenamiento de información específica del usuario

En un Servicios de Escritorio remoto, las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, independientemente de la información global que se aplica a todos los usuarios. Esta regla se aplica a la información almacenada en el Registro, así como a la información almacenada en archivos. En general, no suponga que un equipo es equivalente a un usuario.

Almacene la información del Registro específica del usuario en la clave del Registro **HKEY \_ CURRENT \_ USER.** Servicios de Escritorio remoto carga el subárbol del registro personal del usuario actual en **HKEY \_ CURRENT \_ USER** cuando el usuario inicia sesión. Por supuesto, Servicios de Escritorio remoto el Registro para asegurarse de que cada uno de los clientes que han iniciado sesión detecta el subárbol de usuario correcto en **HKEY \_ CURRENT \_ USER**. Para obtener más información sobre las claves del Registro, vea [Seguridad](/windows/desktop/SysInfo/registry-key-security-and-access-rights) y derechos de acceso de las claves del Registro y [Subárboles del Registro.](/windows/desktop/SysInfo/registry-hives)

Por el contrario, todos los usuarios comparten **el subárbol HKEY \_ LOCAL \_ MACHINE.** Use **HKEY \_ LOCAL MACHINE \_ para** almacenar información específica del equipo, no información específica del usuario.

Almacene los archivos de preferencias de usuario u otros archivos específicos del usuario en el directorio raíz del usuario o en un directorio especificado por el usuario. Esta consideración se aplica a los archivos temporales que se usan para almacenar información provisional (como datos almacenados en caché) o para pasar datos a otra aplicación. Los archivos temporales específicos del usuario también deben almacenarse por usuario.

Puede usar la función [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) con la marca PERSONAL de CSIDL para obtener la ubicación del directorio de archivos \_ personales del usuario. También puede usar la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para recuperar la ruta de acceso del Windows directorio. En un entorno Servicios de Escritorio remoto, se garantiza que Windows directorio sea privado para cada usuario. No almacene archivos específicos del usuario en el directorio del sistema, como WINDOWS, o en el directorio del programa, como Archivos de programa.

Para evitar conflictos entre la información y las preferencias de los usuarios, las aplicaciones deben almacenar información temporal por usuario en archivos temporales específicos del usuario. Los archivos temporales específicos del usuario también evitan errores de aplicación causados por conflictos de bloqueo de archivos. Para especificar la ruta de acceso para almacenar información temporal, use [**la función GetTempPath.**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha)

 

 