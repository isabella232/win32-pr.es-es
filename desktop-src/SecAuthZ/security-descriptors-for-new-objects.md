---
description: Al crear un objeto protegible, puede asignar un descriptor de seguridad al nuevo objeto.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descriptores de seguridad para nuevos objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666657"
---
# <a name="security-descriptors-for-new-objects"></a>Descriptores de seguridad para nuevos objetos

Al crear un objeto protegible, puede asignar un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) al nuevo objeto. Las funciones para crear objetos protegibles, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), tienen un parámetro que apunta a la estructura [**de \_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) que puede contener un puntero al descriptor de seguridad del nuevo objeto. Para ver el código de ejemplo que crea un descriptor de seguridad y, a continuación, llama a **RegCreateKeyEx** para asignar el descriptor de seguridad a una nueva clave del registro, vea [crear un descriptor de seguridad para un nuevo objeto en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).

El componente del sistema o el servidor que administra el objeto puede almacenar el descriptor de seguridad especificado o predeterminado para convertirlo en un atributo persistente del objeto. Si el creador de un objeto no especifica un descriptor de seguridad, el sistema utiliza información de seguridad heredada o predeterminada para crear un descriptor de seguridad. Puede usar funciones para cambiar la información del descriptor de seguridad de un objeto.

Los objetos de servicio de directorio, archivos, directorios, claves del registro y equipos de escritorio son objetos protegibles que pueden tener un objeto primario. Al crear uno de estos objetos, el sistema comprueba las ACE heredables en el descriptor de seguridad del objeto primario. Normalmente, el sistema combina cualquier ACE heredable en las ACL del descriptor de seguridad del nuevo objeto. Puede evitar que una DACL o SACL herede las ACE mediante el establecimiento de los \_ bits protegidos de la DACL de se \_ protegido o \_ SACL \_ protegida en los bits de control del descriptor de seguridad. Para obtener más información, vea [herencia de ACE](ace-inheritance.md).

 

 
