---
title: Configuración del registro del archivo DLL de administración de RAS
description: El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532409"
---
# <a name="ras-administration-dll-registry-setup"></a>Configuración del registro del archivo DLL de administración de RAS

El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar el archivo DLL, establezca los siguientes valores bajo esta clave.



| Nombre del valor    | Datos del valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Una cadena **reg \_ SZ** que contiene el nombre descriptivo para mostrar del archivo dll. |
| *DLLPath*     | Una cadena **reg \_ SZ** que contiene la ruta de acceso completa del archivo dll.                  |



 

Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **reg \_ SZ** : dll de administrador de ras de proelectrones

*DLLPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de quitar o desinstalar. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro del archivo DLL.

 

 




