---
title: Acerca de la instalación del Registro dll de administración de RAS
description: Comprenda los requisitos para registrar un archivo DLL de administración del servicio de acceso remoto (RAS) de terceros con RAS. RAS admite varios archivos DLL de administración de RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS Administration RRAS, dll registry setup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dbabc7a667455bce2cffbd3d04591076f820efa755c0f512f27130a82fde4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909915"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Acerca de la instalación del Registro dll de administración de RAS

El programa de instalación de un archivo DLL de administración ras de terceros debe registrar el archivo DLL con RAS proporcionando información con la siguiente clave en el Registro.

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



 

Dado que RAS admite varios archivos DLL de administración de RAS, el valor del Registro **DLLPath** puede contener una lista delimitada por punto y coma de rutas de acceso. Por ejemplo, la entrada del Registro para un archivo DLL de administración RAS de una empresa ficticia denominada ProElectrón, Inc., podría ser la siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : DLL de administrador ras de ProElectrón

*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS llama a los archivos DLL en el orden en que aparecen en este valor del Registro. El valor del Registro *DisplayName* todavía contiene un solo nombre para mostrar.

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación y desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro para el archivo DLL.

**Windows 2000/NT:** RAS solo admite un archivo DLL de administración de RAS, por lo que el valor del Registro **DLLPath** no puede contener una lista delimitada por punto y coma de rutas de acceso.

 

 




