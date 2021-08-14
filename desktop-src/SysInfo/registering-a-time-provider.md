---
description: El sistema carga un proveedor de hora en función de su información de configuración almacenada en el Registro.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registro de un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eeb7bce1370e443eaf3eb42d78cdfd058cf2c38147da038de1e921d85e957f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763930"
---
# <a name="registering-a-time-provider"></a>Registro de un proveedor de hora

El sistema carga un proveedor de hora en función de su información de configuración almacenada en el Registro. Cada proveedor de tiempo debe crear la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *ProviderName*

En la tabla siguiente se describen los valores que deben existir en la clave de cada proveedor.



| Valor             | Descripción                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Nombre del archivo DLL que contiene el proveedor. Este valor tiene el tipo **REG \_ SZ**.                                                                                                                                     |
| **Habilitado**       | Indica si se debe iniciar el proveedor. Si este valor es 1, se inicia el proveedor. De lo contrario, no se inicia el proveedor. Este valor tiene el tipo **REG \_ DWORD**.                                           |
| **InputProvider** | Indica si el proveedor es un proveedor de entrada o un proveedor de salida. Si este valor es 1, el proveedor es un proveedor de entrada. De lo contrario, el proveedor es un proveedor de salida. Este valor tiene el tipo **REG \_ DWORD**. |



 

El administrador del proveedor de hora enumera las claves bajo la clave **TimeProviders** e inicia cada proveedor habilitado. Los proveedores se inician al iniciar el sistema y cada vez que hay cambios en los parámetros.

Cada proveedor de hora también puede almacenar información de configuración específica de la aplicación en el Registro.

 

 



