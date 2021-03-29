---
title: Almacenar información específica del usuario
description: Las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, aparte de la información global que se aplica a todos los usuarios.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077916"
---
# <a name="storing-user-specific-information"></a>Almacenar información específica del usuario

En un entorno de Servicios de Escritorio remoto, las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, independientemente de la información global que se aplica a todos los usuarios. Esta regla se aplica a la información almacenada en el registro, así como a la información almacenada en los archivos. En general, no suponga que un equipo es equivalente a un usuario.

Almacene la información del registro específica del usuario en la clave del registro **HKEY \_ Current \_ User** . Servicios de Escritorio remoto carga el subárbol del registro personal del usuario actual en **HKEY \_ Current \_ User** cuando el usuario inicia sesión. Por supuesto, Servicios de Escritorio remoto administra el registro para asegurarse de que cada uno de los clientes conectados detecta el subárbol de usuario correcto en **HKEY \_ Current \_ User**. Para obtener más información sobre las claves del registro, consulte [derechos de acceso y seguridad de la clave del registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights) y [subárboles del registro](/windows/desktop/SysInfo/registry-hives).

En cambio, todos los usuarios comparten el subárbol del **\_ \_ equipo local HKEY** . Use **la \_ \_ máquina local HKEY** para almacenar información específica del equipo, no información específica del usuario.

Almacenar archivos de preferencias de usuario u otros archivos específicos del usuario en el directorio raíz del usuario o en un directorio especificado por el usuario. Esta consideración se aplica a los archivos temporales que se usan para almacenar información provisional (como los datos en caché) o para pasar datos a otra aplicación. Los archivos temporales específicos del usuario también se deben almacenar por usuario.

Puede usar la función [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) con la \_ marca personal de CSIDL para obtener la ubicación del directorio de archivos personales del usuario. También puede usar la función [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para recuperar la ruta de acceso del directorio de Windows. En un entorno de Servicios de Escritorio remoto, se garantiza que el directorio de Windows es privado para cada usuario. No almacene archivos específicos del usuario en el directorio del sistema, como WINDOWS o el directorio de programas, como archivos de programa.

Para evitar conflictos entre la información y las preferencias de los usuarios, las aplicaciones deben almacenar información temporal por usuario en archivos temporales específicos del usuario. Los archivos temporales específicos del usuario también impiden errores de aplicación causados por conflictos de bloqueo de archivos. Para especificar la ruta de acceso para almacenar información temporal, use la función [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) .

 

 