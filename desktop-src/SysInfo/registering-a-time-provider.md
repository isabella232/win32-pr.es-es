---
description: El sistema carga un proveedor de hora en función de su información de configuración almacenada en el registro.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Registrar un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910325"
---
# <a name="registering-a-time-provider"></a>Registrar un proveedor de hora

El sistema carga un proveedor de hora en función de su información de configuración almacenada en el registro. Cada proveedor de hora debe crear la siguiente clave del registro:

**HKEY \_ \_Equipo local \\ sistema** \\ **CurrentControlSet** \\ **servicios** \\ **W32Time** \\ **TimeProviders** \\ *providerName*

En la tabla siguiente se describen los valores que deben existir en la clave de cada proveedor.



| Value             | Descripción                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Nombre del archivo DLL que contiene el proveedor. Este valor tiene el tipo **reg \_ SZ**.                                                                                                                                     |
| **Enabled**       | Indica si se debe iniciar el proveedor. Si este valor es 1, se inicia el proveedor. De lo contrario, el proveedor no se inicia. Este valor tiene el tipo **reg \_ DWORD**.                                           |
| **InputProvider** | Indica si el proveedor es un proveedor de entrada o un proveedor de salida. Si este valor es 1, el proveedor es un proveedor de entrada. De lo contrario, el proveedor es un proveedor de salida. Este valor tiene el tipo **reg \_ DWORD**. |



 

El administrador de proveedores de hora enumera las claves en la clave **TimeProviders** e inicia cada proveedor habilitado. Los proveedores se inician en el inicio del sistema y cada vez que hay cambios en los parámetros.

Cada proveedor de hora también puede almacenar información de configuración específica de la aplicación en el registro.

 

 



