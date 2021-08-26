---
title: Registro de un archivo DLL de seguridad ras
description: El programa de instalación de un archivo DLL de seguridad RAS debe registrar el archivo DLL con el Windows NT/Windows 2000 RAS.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5ca32aa687649c80917f9a072b9d4cbeb0f1f4e8ba61ce090e7781bb04cdefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028424"
---
# <a name="registering-a-ras-security-dll"></a>Registro de un archivo DLL de seguridad ras

El programa de instalación de un archivo DLL de seguridad RAS debe registrar el archivo DLL con el Windows NT/Windows 2000 RAS. Solo se puede registrar un archivo DLL de seguridad ras como compatibilidad con varios archivos DLL de seguridad. Para registrar un archivo DLL de seguridad RAS, establezca el *valor DLLPath* en la clave siguiente en el Registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nombre del valor | Datos del valor                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Cadena **REG \_ SZ** que contiene la ruta de acceso del archivo DLL. Esta cadena debe especificar la ruta de acceso completa a menos que el archivo DLL esté en un directorio enumerado en la ruta de acceso del sistema. |



 

El programa de instalación de un archivo DLL de seguridad ras también debe proporcionar la funcionalidad de eliminación o desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar el *valor DLLPath* del Registro. El servicio RAS no se inicia si el *valor DLLPath* especifica un archivo DLL que no se encuentra.

Un archivo DLL de seguridad de RAS debe exportar las [**funciones RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) [**y RasSecurityDialogEnd.**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend)

 

 




