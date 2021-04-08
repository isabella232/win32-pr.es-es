---
title: Acerca de la configuración del registro del archivo DLL de administración RAS
description: El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RRAS de administración de RAS, configuración del registro de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103904314"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Acerca de la configuración del registro del archivo DLL de administración RAS

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



 

Como RAS admite varios archivos dll de administración de RAS, el valor de registro **DLLPath** puede contener una lista delimitada por punto y coma de rutas de acceso. Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser la siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : dll de administrador de ras de proelectrones

*DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll

RAS llama a los archivos dll en el orden en que aparecen en este valor del registro. El valor de *displayName* del valor del registro todavía contiene un solo nombre para mostrar.

El programa de instalación de una DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación y desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro para el archivo DLL.

**Windows 2000/NT:** RAS solo admite un archivo DLL de administración RAS, por lo que el valor de registro **DLLPath** no puede contener una lista de rutas de acceso delimitada por punto y coma.

 

 




