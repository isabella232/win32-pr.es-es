---
title: Acerca de la instalación del Registro DLL de administración de RAS
description: Comprenda los requisitos para registrar un archivo DLL de administración del servicio de acceso remoto (RAS) de terceros con RAS. RAS admite varios archivos DLL de administración de RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS Administration RRAS , dll registry setup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406668"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Acerca de la instalación del Registro DLL de administración de RAS

El programa de instalación de un archivo DLL de administración de RAS de terceros debe registrar el archivo DLL con RAS proporcionando información con la siguiente clave en el Registro.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar el archivo DLL, establezca los siguientes valores en esta clave.



| Nombre del valor    | Datos del valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Cadena **REG \_ SZ** que contiene el nombre para mostrar descriptivo del archivo DLL. |
| *DLLPath*     | Cadena **REG \_ SZ** que contiene la ruta de acceso completa del archivo DLL.                  |



 

Dado que RAS admite varios archivos DLL de administración de RAS, el valor del Registro **DLLPath** puede contener una lista delimitada por punto y coma de rutas de acceso. Por ejemplo, la entrada del Registro para un archivo DLL de administración de RAS de una empresa ficticia denominada ProElectrón, Inc., podría ser la siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : DLL de administración de RAS de ProElectrón

*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS llama a los archivos DLL en el orden en que aparecen en este valor del Registro. El valor del Registro *DisplayName* todavía contiene solo un nombre para mostrar.

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación y desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro para el archivo DLL.

**Windows 2000/NT:** RAS solo admite un archivo DLL de administración de RAS, por lo que el valor del Registro **DLLPath** no puede contener una lista delimitada por punto y coma de rutas de acceso.

 

 




