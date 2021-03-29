---
title: Registro de un archivo DLL de seguridad RAS
description: El programa de instalación de una DLL de seguridad RAS debe registrar el archivo DLL con el servidor RAS de Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775396"
---
# <a name="registering-a-ras-security-dll"></a>Registro de un archivo DLL de seguridad RAS

El programa de instalación de una DLL de seguridad RAS debe registrar el archivo DLL con el servidor RAS de Windows NT/Windows 2000. Solo se puede registrar un archivo DLL de seguridad RAS porque no se proporciona compatibilidad con varios archivos dll de seguridad. Para registrar un archivo DLL de seguridad RAS, establezca el valor *DLLPath* bajo la clave siguiente en el registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nombre del valor | Datos del valor                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Una cadena **reg \_ SZ** que contiene la ruta de acceso del archivo dll. Esta cadena debe especificar la ruta de acceso completa a menos que el archivo DLL esté en un directorio que aparezca en la ruta de acceso del sistema. |



 

El programa de instalación de un archivo DLL de seguridad RAS también debe proporcionar la funcionalidad de quitar o desinstalar. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar el valor *DLLPath* del registro. El servicio RAS no se inicia si el valor *DLLPath* especifica un archivo DLL que no se puede encontrar.

Un archivo DLL de seguridad RAS debe exportar las funciones [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) y [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .

 

 




