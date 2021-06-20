---
title: Instalación del Registro DLL de administración de RAS
description: Comprenda los requisitos para registrar un archivo DLL de administración del servicio de acceso remoto (RAS) de terceros con RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406718"
---
# <a name="ras-administration-dll-registry-setup"></a>Instalación del Registro DLL de administración de RAS

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



 

Por ejemplo, la entrada del Registro para un archivo DLL de administración de RAS de una empresa ficticia denominada ProElectrón, Inc. podría ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **REG \_ SZ** : DLL de administración de RAS de ProElectrón

*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de eliminación o desinstalación. Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del Registro del archivo DLL.

 

 




